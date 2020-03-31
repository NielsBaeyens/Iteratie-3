package domein;

import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class Spel {
	private Deck deck;
	private List<Speler> spelers;
	private List<Stapel> stapels;
	private List<Rij> rijen;

	public Spel(List<Speler> spelers) {
		this.deck = new Deck();
		this.spelers = spelers;
		this.stapels = new ArrayList<Stapel>();

		for (int i=0;i<spelers.size();i++) {
			stapels.add(new Stapel());
		}

		this.rijen = new ArrayList<Rij>();
		int aantalRijKaarten = 5;
		if (spelers.size() == 4) {
			aantalRijKaarten = 4;
		}
		for (int i = 0; i < aantalRijKaarten; i++) {
			rijen.add(new Rij(i+1));
		}

	}

	public void legKaartOpStapel(int stapelIndex) {
		Kaart kaart = deck.geefKaart();
		Stapel stapel = stapels.get(stapelIndex);
		stapel.legKaartOpStapel(kaart);
	}

	public Kaart neemKaartenVanStapel(int stapelIndex) {
		Stapel stapel = stapels.get(stapelIndex);
		Kaart kaart = stapel.getKaartenVanStapel();
		return kaart;
	}

	public void toonRijen() {
		System.out.println("Dit zijn de rijen: ");
		for (Rij rij : rijen) {
			System.out.println("   "+rij);
		}
	}
	
	public void toonSpelersKaarten() {
		System.out.println("Dit zijn de kaarten van de spelers: ");
		for (Speler speler : spelers) {
			System.out.println("  "+speler.getNaam()+" : ");
			speler.toonSpelerKaarten();
		}
	}
	
	public int telNietLegeRijen() {
		int aantal = 0;
		for (Rij rij : rijen) {
			if (!rij.isLeeg()) {
				aantal++;
			}
		}
		return aantal;
	}
	
	public void sorteerRondeRijen() {
		Collections.sort(rijen);
	}

	public Deck getDeck() {
		return deck;
	}

	public void setDeck(Deck deck) {
		this.deck = deck;
	}

	public List<Speler> getSpelers() {
		return spelers;
	}

	public void setSpelers(List<Speler> spelers) {
		this.spelers = spelers;
	}

	public List<Stapel> getStapels() {
		return stapels;
	}

	public void setStapels(List<Stapel> stapels) {
		this.stapels = stapels;
	}

	public List<Rij> getRijen() {
		return rijen;
	}

	public void setRijen(List<Rij> rijen) {
		this.rijen = rijen;
	}

	

	
}
