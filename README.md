# IT-Sicherheit---Implementierung-eines-symmetrischen-Verschl-sselungsverfahrens
Es ist mit einer Programmier-/Skriptsprache nach Wahl (vorzugsweise Perl) ein primitiver symmetrischer Blockalgorithmus zu entwickeln, der die grundlegenden Elemente symmetrischer Verfahren anwendet (Aufteilung in Blöcke, Transposition, Substitution, Schlüsselintegration). Im Zuge der Präsentation ist die Funktionsweise durch die Verschlüsselung- bzw. Entschlüsselung eines Textes live vorzuführen.

Geplante Herangehensweise an die Aufgabenstellung:

Die Aufgabenstellung bestand darin, einen symmetrischen Blockalgorithmus zu implementieren, der die Grundlagen der Blockverschlüsselung nutzt. Der Klartext sollte in Blöcke unterteilt, permutiert und mithilfe der XOR-Operation mit einem festgelegten Schlüssel verschlüsselt werden. Die geplante Herangehensweise umfasste die Entwicklung eines modularen Java-Programms, das diese Schritte abbildet und eine sichere Verschlüsselung von Texten ermöglicht. Parallel wurde eine Evaluierung durchgeführt, um die Funktionalität der Verschlüsselung zu testen.

Theoretische Grundlagen:
Die theoretischen Grundlagen basieren auf den Konzepten der symmetrischen Verschlüsselung. 
Dazu gehört die Verwendung desselben Schlüssels für die Ver- und Entschlüsselung, das Aufteilen des Klartexts in Blöcke und die Anwendung von Substitution und Permutation zur Verwirrung und Verschleierung der Daten. 
Weitere zentrale Konzepte sind Padding (Auffüllen des Klartexts auf Blockgröße) und die XOR-Operation, die zur sicheren Verknüpfung des Textes mit dem Schlüssel dient. 
Diese Methoden werden in mehreren Runden wiederholt, um die Sicherheit zu erhöhen.

Plattform (OS, Software, Technologie,…):

Betriebssystem: Lokales System (Windows)

Software: IntelliJ IDEA als Entwicklungsumgebung, Java SDK zur Implementierung des Algorithmus.

Technologie: Programmiersprache Java, genutzt mit Java-Klassen wie Base64 zur sicheren Codierung der verschlüsselten Daten.

Erfahrungen (Vorbereitung u. Installation):
Die Vorbereitung und Installation waren relativ einfach, da Java als plattformunabhängige Programmiersprache gut unterstützt wird. Die Einrichtung der Entwicklungsumgebung IntelliJ verlief problemlos. 
Die Konfiguration erforderte die Installation des Java Development Kit (JDK) und die Integrierung von Base64 zur Verarbeitung von verschlüsselten Daten.

Erfahrungen (laufender Betrieb):
Im laufenden Betrieb hat sich der Algorithmus als stabil und zuverlässig erwiesen. Der Debugging-Modus in IntelliJ ermöglichte eine detaillierte Überprüfung jedes einzelnen Schritts, was die Fehlersuche und das Verständnis des Verschlüsselungsprozesses erleichterte. 
Die Ausführung des Algorithmus zeigte sich performant, auch bei größeren Datenmengen.


Evaluierungsergebnis bzw. Schutzmaßnahmen (bei Darstellung von Angriffen):
Das Evaluierungsergebnis bestätigte die Korrektheit der Verschlüsselung und Entschlüsselung. Der Algorithmus ist für den vorgesehenen Zweck sicher, jedoch könnten Angriffe wie das Erraten des Schlüssels bei kurzen Schlüsseln (Brute-Force-Angriffe) ein potenzielles Risiko darstellen. 
Zur Verbesserung der Sicherheit wäre es ratsam, für jede Runde einen anderen Teilschlüssel zu verwenden, wie es bei moderneren Algorithmen der Fall ist (z.B. AES). Darüber hinaus könnten komplexere Permutations- und Substitutionsmethoden implementiert werden, um die Resistenz gegen Kryptoanalysen zu erhöhen.

Stärken: 
•	Leicht verständliche Implementierung, die die Grundlagen der Blockverschlüsselung gut veranschaulicht.
•	Modulare und flexible Struktur des Codes, die Erweiterungen und Anpassungen ermöglicht.
•	Gutes Testresultat, das eine korrekte Funktionsweise der Verschlüsselung und Entschlüsselung bestätigt.

Schwächen: 
•	Der gleiche Schlüssel wird für alle Runden verwendet, was die Sicherheit im Vergleich zu modernen Verschlüsselungsverfahren verringert.
•	Die Anzahl der Runden ist mit 4 relativ gering, was bei sicherheitskritischen Anwendungen nicht ausreicht.
•	Keine Implementierung von Best Practices wie Key Scheduling oder fortgeschrittenen Padding-Methoden (z.B. PKCS#7).

