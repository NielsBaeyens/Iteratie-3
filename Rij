package domein;

import java.util.ArrayList;
import java.util.List;

public class Rij implements Comparable<Rij>{
	private int nr;
	private List<Kaart> kaarten;

	public Rij(int nr) {
		this.nr = nr;
		kaarten = new ArrayList<Kaart>();
	}

	@Override
	public String toString() {
		String s = "Rij nr "+nr+" : ";
		for (Kaart kaart : kaarten) {
			s+=kaart.toString()+" ";
		}
		return s;
	}

	@Override
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (getClass() != obj.getClass())
			return false;
		Rij other = (Rij) obj;
		if (nr != other.nr)
			return false;
		return true;
	}
	
	@Override
	public int compareTo(Rij rij) {
		return nr-rij.nr;
	}

	public boolean isLeeg() {
		return kaarten.isEmpty();
	}
	
	public boolean isVol() {
		return kaarten.size() == 3;
	}

	public int getNr() {
		return nr;
	}

	public void setNr(int nr) {
		this.nr = nr;
	}

	public List<Kaart> getKaarten() {
		return kaarten;
	}

	public void setKaarten(List<Kaart> kaarten) {
		this.kaarten = kaarten;
	}

	
	
}
