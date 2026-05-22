# maxence
import { useState } from "react";

const chapters = [
  {
    id: 0,
    title: "Introduction générale",
    subtitle: "Droit spécial des contrats",
    color: "#1a1a2e",
    accent: "#e94560",
    icon: "⚖️",
    sections: [
      {
title: "Qu'est-ce que le droit des contrats spéciaux ?",
        content: [
          { type: "def", label: "Définition", text: "Ensemble des règles particulières qui s'appliquent à chaque contrat en fonction de sa qualification (vente, bail, mandat…). S'oppose au droit commun des contrats (L2)." },
          { type: "info", label: "Attention !", text: "\"Contrats spéciaux\" ne signifie pas contrats rares : ce sont les contrats du quotidien (vente, bail…). On devrait dire \"droit spécial des contrats\"." },
          { type: "list", label: "Contrats civils vs commerciaux", items: [
            "Un contrat peut être civil ou commercial selon la qualité des parties",
            "Vente entre professionnels = vente commerciale",
            "Vente entre particuliers = vente civile",
            "Vente pro → particulier = vente mixte"
          ]},
          { type: "rule", label: "3 règles propres aux actes de commerce", items: [
            "Compétence des tribunaux de commerce",
            "Preuve libre contre le commerçant (art. L.110-3 C.com)",
            "Solidarité présumée entre co-débiteurs commerciaux (art. 1310 C.civ.)"
          ]}
        ]
      },
      {
        title: "Évolution & Domaine",
        content: [
          { type: "list", label: "Phénomènes d'évolution", items: [
            "Innovation : liberté contractuelle → contrats innommés / sui generis",
            "Spécialisation : apparition de sous-catégories (bail d'habitation, commercial, rural)",
            "Morcellement : certains contrats s'autonomisent (contrat de travail → droit du travail ; transport → droit des transports)"
          ]},
          { type: "info", label: "Domaine étudié (Livre III C.civ.)", text: "Vente (T.VI) • Échange (T.VII) • Bail (T.VIII, Ch.II) • Entreprise (T.VIII, Ch.III) • Prêt (T.X) • Dépôt (T.XI) • Mandat (T.XIII)" },
          { type: "def", label: "3 catégories de contrats spéciaux", text: "① Translatifs de propriété (vente, échange) | ② Portant sur un service personnel (entreprise, mandat, dépôt) | ③ De mise à disposition d'une chose (bail, prêt)" }
        ]
      },
      {
        title: "Qualification des contrats",
        content: [
          { type: "rule", label: "Critères de qualification", items: [
            "Objet du contrat (negotium) : opération économique réalisée",
            "Critère principal/accessoire : si contrat complexe, on retient la qualification de l'élément principal",
            "Qualification distributive : si impossible de distinguer principal/accessoire, on applique plusieurs qualifications",
            "Contrat sui generis : aucun rattachement possible → droit commun + interprétation"
          ]},
          { type: "info", label: "Important", text: "La qualification est une opération de droit : le juge n'est pas lié par celle des parties. La Cour de cassation contrôle la qualification retenue par les juges du fond." }
        ]
      }
    ]
  },
  {
    id: 1,
    title: "La Vente — Définition & Qualification",
    subtitle: "Chapitre 1 : Contrats translatifs de propriété",
    color: "#16213e",
    accent: "#0f3460",
    icon: "🏷️",
    sections: [
      {
        title: "Définition légale de la vente",
        content: [
          { type: "def", label: "Art. 1582 & 1583 C.civ.", text: "La vente est le contrat par lequel le vendeur transmet la propriété à l'acheteur en contrepartie du paiement d'un prix. La PPT est acquise dès accord sur la chose et le prix." },
          { type: "list", label: "Éléments essentiels", items: ["Chose vendue", "Prix (contrepartie monétaire)"] }
        ]
      },
      {
      title: "Vente vs Contrat d'entreprise",
        content: [
          { type: "def", label: "Problème", text: "Quand un professionnel s'oblige à fabriquer une chose, est-ce une vente ou un contrat d'entreprise ?" },
          { type: "rule", label: "Immeubles", items: [
            "Sol fourni par le fabricant → VENTE d'immeuble à construire (art. 1601-1 C.civ.)",
            "Sol fourni par le client → CONTRAT D'ENTREPRISE (acquisition par accession immobilière)"
          ]},
          { type: "rule", label: "Meubles — Critère de la Cour de cassation : Standard vs Sur-mesure", items: [
            "SUR MESURE (travail original, capacités spéciales) → CONTRAT D'ENTREPRISE",
            "STANDARD (produit en série, normes définies à l'avance) → VENTE"
          ]},
          { type: "info", label: "Ancien critère (abandonné)", text: "Critère économique : valeur du travail > valeur des matériaux → entreprise (encore applicable en droit international, Convention de Vienne)" }
        ]
      }
    ]
  },
  {
    id: 2,
    title: "Formation de la Vente",
    subtitle: "Chapitre 2 : Capacité, consentement, avant-contrats",
    color: "#0d2137",
    accent: "#00b4d8",
    icon: "📝",
    sections: [
      {
        title: "Droit de vendre et d'acheter",
        content: [
          { type: "rule", label: "Principe (art. 1594)", text: "Liberté de vendre et d'acheter pour tous ceux que la loi n'interdit pas." },
          { type: "list", label: "Restrictions côté vendeur", items: [
            "Clause d'inaliénabilité (art. 900-1 : temporaire + intérêt légitime)",
            "Clause d'exclusivité de vente (contrats de distribution)",
            "Obligation de vendre : refus interdit si anti-concurrentiel ou vs consommateur (art. L.121-11 C.conso)"
          ]},
          { type: "list", label: "Restrictions côté acheteur", items: [
            "Incapacités spéciales : tuteur (art. 1596), mandataire ne peut acheter les biens qu'il vend, salariés d'établissements psychiatriques…",
            "Droits de préemption (légaux ou conventionnels) et de retrait",
            "Clauses d'approvisionnement exclusif (durée plafonnée)"
          ]}
        ]
      },
      {
        title: "La Vente Conditionnelle",
        content: [
          { type: "comparison", rows: [
            { label: "Condition suspensive", a: "Naissance de l'obligation subordonnée à la réalisation de l'évènement", b: "" },
            { label: "Condition résolutoire", a: "Survie de l'obligation subordonnée à la NON-réalisation de l'évènement", b: "" },
          ]},
          { type: "rule", label: "Condition potestative (art. 1304-2)", text: "Nulle si elle dépend de la seule volonté arbitraire du débiteur. Admise si la volonté peut être contrôlée sur base de critères objectifs (condition « mixte »)." },
          { type: "def", label: "Sanction (art. 1304-3)", text: "Si le débiteur a empêché l'accomplissement de la condition de mauvaise foi → la condition est réputée accomplie." },
          { type: "info", label: "Conditions légales (Loi Scrivener)", text: "Art. L.313-41 : vente subordonnée de plein droit à l'obtention du prêt. Art. L.313-36 : prêt soumis de plein droit à la condition résolutoire de non-conclusion de la vente." }
        ]
      },
      {
        title: "Les Avant-contrats",
        content: [
          { type: "def", label: "1. Promesse Unilatérale de Vente (PUV) — art. 1124", text: "Contrat par lequel le promettant s'engage irrévocablement à vendre ; le bénéficiaire dispose d'un droit d'option (droit potestatif). Il ne manque que le consentement du bénéficiaire." },
          { type: "rule", label: "Effets essentiels de la PUV", items: [
            "Rétractation du promettant INEFFICACE (art. 1124 al.2) : la révocation n'empêche pas la formation du contrat",
            "Cession du bien à un tiers de MF → nullité de la vente (art. 1124 al.3)",
            "Forme : acte authentique OU SSP enregistré dans 10 jours (art. 1589-2), à peine de nullité",
            "Indemnité d'immobilisation = prix de l'option, ≠ clause pénale"
          ]},
          { type: "def", label: "2. Promesse Synallagmatique de Vente (PSV) — art. 1589", text: "Les deux parties consentent à la vente. Principe : vaut vente dès accord sur la chose et le prix. Tempérament JP : peut valoir vente à terme ou PSV autonome si la formation est subordonnée à la signature de l'acte notarié." },
          { type: "def", label: "3. Pacte de Préférence — art. 1123", text: "Le promettant s'engage à proposer par priorité au bénéficiaire s'il décide de vendre. ≠ PUV : aucune obligation de vendre. Sanctions en cas de violation : D&I + nullité/substitution si le tiers connaissait l'existence du pacte ET l'intention du bénéficiaire de s'en prévaloir." }
        ]
      },
      {
        title: "Faculté de Repentir & Droit de Rétractation",
        content: [
          { type: "rule", label: "Repentir de l'acheteur", items: [
            "Art. L.221-18 C.conso : 14 jours (vente à distance, démarchage, hors établissement)",
            "Art. L.271-1 CCH : 10 jours (acheteur non-professionnel, immeuble à usage d'habitation)"
          ]},
          { type: "def", label: "Clause de dédit (art. 1590 — Vente avec arrhes)", text: "Arrhes = faculté de dédit réciproque. L'acheteur perd les arrhes s'il se rétracte ; le vendeur rend le double s'il se rétracte. ≠ acompte (vente ferme, aucun dédit). Présomption arrhes dans les contrats B2C (art. L.214-1 C.conso) sauf clause contraire." },
          { type: "info", label: "Repentir du seul vendeur", text: "Vente avec faculté de rachat (art. 1659) : vendeur peut reprendre la chose moyennant restitution du prix + frais. Durée max : 5 ans (art. 1660). Publicité obligatoire si vente immobilière." }
        ]
      }
    ]
  },
  {
    id: 3,
    title: "Effets de la Vente",
    subtitle: "Transfert de propriété, risques, obligations des parties",
    color: "#1b2838",
    accent: "#66c0f4",
    icon: "🔄",
    sections: [
      {
        title: "La Chose Vendue",
        content: [
          { type: "rule", label: "Conditions sur la chose", items: [
            "Doit être dans le commerce juridique (art. 1598)",
            "Doit exister (ou être future — art. 1163)",
            "Doit être déterminée ou déterminable",
            "Doit appartenir au vendeur (nemo plus juris)"
          ]},
          { type: "def", label: "Vente de la chose d'autrui (art. 1599)", text: "Nulle, mais nullité RELATIVE (en faveur de l'acheteur seulement). Rarement invoquée car l'action en revendication du véritable propriétaire est souvent irrecevable." }
        ]
      },
      {
        title: "Le Prix",
        content: [
          { type: "rule", label: "Exigences du prix", items: [
            "DÉTERMINÉ ou déterminable (art. 1591) — condition de validité ← différence avec le contrat d'entreprise",
            "RÉEL et SÉRIEUX (non simulé, non dérisoire)",
            "Sanction de l'indétermination : nullité RELATIVE (partie lésée)"
          ]},
          { type: "list", label: "Modes de détermination", items: [
            "Clause à dire d'expert (art. 1592) : mandataire commun des parties",
            "Clause de tarif en vigueur au jour de la livraison (si critères objectifs)",
            "Clause de rentabilité (cessions de parts sociales)"
          ]},
          { type: "info", label: "Contrats-cadres (art. 1164)", text: "L'art. 1591 NE s'applique PLUS aux ventes d'application d'un contrat-cadre. Le fournisseur peut fixer le prix unilatéralement, mais doit le justifier en cas de contestation. Abus → D&I + résolution du contrat-cadre." },
          { type: "def", label: "La Lésion (art. 1674)", text: "Exception au principe de non-prise en compte du défaut d'équivalence (art. 1168). Applicable uniquement au vendeur d'immeuble lésé de plus des 7/12èmes. Action en rescision dans les 2 ans. L'acheteur peut exercer la faculté de rachat de la lésion (art. 1681) en payant le supplément du juste prix - 1/10ème du prix total." }
        ]
      },
      {
        title: "Transfert de Propriété & des Risques",
        content: [
          { type: "def", label: "Principe du transfert immédiat (art. 1583 & 1196)", text: "La PPT est transférée solo consensu (par le seul accord des volontés), indépendamment de la livraison et du paiement du prix." },
          { type: "rule", label: "Exceptions au transfert immédiat", items: [
            "Choses de genre : transfert différé jusqu'à l'individualisation",
            "Choses futures : transfert à l'achèvement + individualisation",
            "Clause de réserve de propriété : transfert différé jusqu'au complet paiement du prix",
            "Ventes en libre-service (JP pénale) : PPT transférée au paiement en caisse"
          ]},
          { type: "rule", label: "Transfert des risques (res perit domino — art. 1196 al.3)", items: [
            "Les risques suivent la PPT",
            "Exception légale : mise en demeure renverse les risques sur le vendeur (art. 1193 al.3)",
            "Exception B2C (art. L.216-2 C.conso) : risques transférés au consommateur uniquement à la prise de possession physique (règle d'OP)"
          ]}
        ]
      },
      {
        title: "Obligations du Vendeur — Délivrance",
        content: [
          { type: "def", label: "Obligation de délivrance (art. 1604)", text: "Transport de la chose en la puissance et possession de l'acheteur. ≠ livraison (pas d'obligation d'apporter la chose jusqu'à l'acheteur sauf convention contraire)." },
          { type: "rule", label: "Conformité de la chose délivrée", items: [
            "Identique à ce qui est prévu au contrat",
            "En quantité et qualité (si chose de genre)",
            "Réception sans réserve couvre les défauts APPARENTS uniquement",
            "Règles spéciales immobilières : contenance (art. 1616 ss.) ; Loi Carrez (art. 46 L.1965) pour lots de copropriété"
          ]},
          { type: "info", label: "Accessoires de la chose (art. 1615)", text: "La délivrance comprend les accessoires matériels, administratifs et juridiques. L'acheteur recueille toutes les actions attachées à la chose (ex: garantie des vices cachés du vendeur précédent)." }
        ]
      },
      {
        title: "Garantie d'Éviction",
        content: [
          { type: "comparison", rows: [
            { label: "Garantie du fait personnel (art. 1628)", a: "D'OP — couvre troubles de fait ET de droit — adage : \"qui doit garantie ne peut évincer\"", b: "" },
            { label: "Garantie du fait des tiers (art. 1626)", a: "Non d'OP — couvre uniquement troubles de DROIT imputables au vendeur (cause antérieure à la vente) — exclut troubles de fait", b: "" }
          ]},
          { type: "rule", label: "Effets de la garantie d'éviction", items: [
            "Éviction totale : restitution du prix + éventuelle plus-value (art. 1633) + D&I (art. 1630)",
            "Éviction partielle : résolution si l'acheteur ne l'aurait pas conclue + remboursement valeur parcelle",
            "Charges non déclarées : résolution possible + D&I"
          ]},
          { type: "info", label: "Mise en oeuvre", text: "Incidente (appel en garantie pendant le procès avec le tiers) ou Principale (action après avoir perdu le procès — risque de décharge du vendeur si défense insuffisante, art. 1640)." }
        ]
      },
      {
        title: "Garantie des Vices Cachés",
        content: [
          { type: "def", label: "Conditions de fond (art. 1641)", text: "Vice rendant la chose inutilisable (rédhibitoire) OU diminuant tellement son usage que l'acheteur ne l'aurait pas achetée au même prix. Vice apprécié in abstracto par rapport à l'usage normal." },
          { type: "rule", label: "Caractères du vice", items: [
            "CACHÉ : non apparent lors de la réception (art. 1642) — apprécié selon la qualité de l'acheteur",
            "ANTÉRIEUR à la vente (existait en germe au jour du transfert de PPT)"
          ]},
          { type: "rule", label: "Délais (art. 1648)", items: [
            "2 ans à compter de la DÉCOUVERTE du vice",
            "20 ans maximum à compter de la vente (délai butoir — art. 2232)"
          ]},
          { type: "comparison", rows: [
            { label: "Action rédhibitoire", a: "Résolution de la vente + restitution du prix" },
            { label: "Action estimatoire", a: "Conservation de la chose + réduction du prix" },
            { label: "D&I vendeur MF (art. 1645)", a: "Tous D&I — présomption irréfragable de MF pour tout vendeur PROFESSIONNEL" },
            { label: "D&I vendeur BF (art. 1646)", a: "Restitution du prix uniquement (s'applique aux vendeurs profanes)" }
          ]},
          { type: "info", label: "Action directe du sous-acquéreur", text: "Le sous-acquéreur peut agir directement en garantie contre le vendeur initial (accessoire transmis avec la chose). Limite nemo plus juris : pas plus de droits que le revendeur." }
        ]
      },
      {
        title: "Garantie de Conformité (Droit conso)",
        content: [
          { type: "def", label: "Champ d'application (art. L.217-1 ss. C.conso)", text: "Ventes de meubles corporels entre vendeur professionnel et consommateur. Conception UNITAIRE : conformité = identité + aptitude à l'usage normal (vices cachés inclus)." },
          { type: "rule", label: "Délais", items: [
            "Délai de garantie : 2 ans à compter de la délivrance (1 an pour occasion)",
            "Présomption d'antériorité du défaut : 2 ans (1 an pour occasion)",
            "Délai de prescription pour agir : 5 ans à compter de la découverte"
          ]},
          { type: "rule", label: "Effets — hiérarchie des remèdes", items: [
            "1er : Mise en conformité (réparation ou remplacement) sous 30 jours",
            "2ème (si impossible/disproportionné/délai dépassé) : Résolution ou réduction du prix"
          ]},
          { type: "info", label: "Caractères", text: "Régime d'OP. Garantie FACULTATIVE : le consommateur peut choisir la garantie des vices cachés à la place." }
        ]
      }
    ]
  },
  {
    id: 4,
    title: "Le Contrat d'Entreprise",
    subtitle: "Titre I — Service personnel",
    color: "#1a2744",
    accent: "#f5a623",
    icon: "🔧",
    sections: [
      {
        title: "Définition & Qualification",
        content: [
          { type: "def", label: "Définition", text: "Contrat par lequel un prestataire (entrepreneur) s'engage envers un client à accomplir une prestation de manière indépendante, moyennant un prix (art. 1710)." },
          { type: "rule", label: "3 éléments de qualification", items: [
            "Obligation de FAIRE (actes matériels ou intellectuels, ≠ actes juridiques du mandat)",
            "Exécution à titre INDÉPENDANT (≠ subordination juridique du contrat de travail)",
            "Rémunération (à titre ONÉREUX)"
          ]},
          { type: "comparison", rows: [
            { label: "vs Bail", a: "Entrepreneur déploie une activité (service)", b: "Bailleur met une chose à disposition" },
            { label: "vs Mandat", a: "Actes matériels", b: "Actes juridiques au nom d'autrui" },
            { label: "vs Travail", a: "Indépendant (faisceau d'indices)", b: "Subordination juridique à l'employeur" },
            { label: "vs Dépôt", a: "Activité positive", b: "Attitude passive (garde)" }
          ]}
        ]
      },
      {
        title: "Formation — Prix",
        content: [
          { type: "def", label: "Différence fondamentale avec la vente", text: "Le PRIX n'est PAS un élément essentiel du contrat d'entreprise. Le contrat est valable même si le prix est indéterminé (art. 1165 C.civ.)." },
          { type: "rule", label: "Conséquences de l'art. 1165", items: [
            "Le prestataire peut fixer le prix après l'exécution",
            "Le débiteur peut contester → le prestataire doit justifier le montant",
            "En cas d'ABUS : le juge peut accorder des D&I (qui se compensent avec le prix)"
          ]},
          { type: "comparison", rows: [
            { label: "Marché sur facture", a: "Prix convenu à l'avance. Si forfaitaire : aucune augmentation pour difficultés imprévues (art. 1793 pour construction sur terrain du MO)." },
            { label: "Marché sur séries de prix", a: "Prix déterminé au fur et à mesure selon critères convenus (heures, matériaux, surfaces)." }
          ]}
        ]
      },
      {
        title: "Effets — Propriété & Risques",
        content: [
          { type: "rule", label: "Acquisition de la propriété", items: [
            "Matériaux fournis par le MO : le MO est continuellement propriétaire",
            "Matériaux fournis par l'entrepreneur (meuble) : PPT transférée à la RÉCEPTION",
            "Immeuble : acquisition par ACCESSION IMMOBILIÈRE au fur et à mesure"
          ]},
          { type: "rule", label: "Charge des risques (art. 1788 & 1789)", items: [
            "Matériaux fournis par l'entrepreneur : risques à sa charge jusqu'à réception. Exception : si chose achevée + MO mis en demeure de recevoir → risques sur MO",
            "Matériaux fournis par le MO (art. 1789) : entrepreneur tenu de sa faute seulement → perte fortuite supportée par le MO (res perit domino). Mais pas de rémunération pour le travail effectué avant la perte."
          ]}
        ]
      },
      {
        title: "Responsabilité du Prestataire",
        content: [
          { type: "rule", label: "Nature des obligations selon le type de prestation", items: [
            "Tâche intellectuelle → Obligation de MOYENS (aléa dans le résultat)",
            "Fabrication d'un meuble → Obligation de RÉSULTAT quant à l'achèvement",
            "Autres prestations matérielles → variable : résultat (installateur d'alarme), résultat atténuée (garagiste, teinturier, blanchisseur), moyens (entretien/maintenance)",
            "Chose confiée au prestataire → Obligation de RÉSULTAT ATTÉNUÉE"
          ]},
          { type: "info", label: "Art. 1787", text: "Le prestataire répond du fait de ses salariés ET de ses sous-traitants comme de ses propres faits." }
        ]
      },
      {
        title: "Garanties des Constructeurs d'Immeubles",
        content: [
          { type: "comparison", rows: [
            { label: "Garantie décennale (art. 1792)", a: "10 ans depuis réception. Compromission de la solidité ou impropriété à la destination. Obligation de résultat (exonération : cause étrangère seulement). Exception : faute dolosive → garantie perpétuelle." },
            { label: "Garantie biennale (art. 1792-3)", a: "2 ans depuis réception. Bon fonctionnement des équipements dissociables. Obligation de garantie (plus sévère : aucune exonération par FM)." },
            { label: "Garantie de parfait achèvement (art. 1792-6)", a: "1 an depuis réception. Désordres signalés à la réception ou dans l'année. Seul l'entrepreneur auteur des travaux est tenu." }
          ]},
          { type: "info", label: "Règles d'OP", text: "Toutes les garanties constructeurs sont d'OP (toute clause contraire = non écrite). CR : maître de l'ouvrage + acquéreurs successifs." }
        ]
      },
      {
        title: "Obligations du Maître de l'Ouvrage & Sous-traitance",
        content: [
          { type: "list", label: "Obligations du MO", items: [
            "Payer le prix (exigible après exécution sauf convention contraire)",
            "Devoir de coopération (fournir les informations nécessaires)",
            "Prendre livraison de l'ouvrage / Réception (acte juridique — ≠ prise de livraison)"
          ]},
          { type: "rule", label: "Effets de la réception", items: [
            "Transfert des risques au client",
            "Fait courir les délais de garantie décennale et biennale",
            "Prix exigible",
            "Couvre les défauts apparents (sans réserve)"
          ]},
          { type: "def", label: "Sous-traitance (Loi 31/12/1975)", text: "L'entrepreneur principal se substitue un sous-traitant dans l'exécution de son obligation. Le sous-traité est un contrat d'entreprise. Le contrat principal continue à produire ses effets." },
          { type: "rule", label: "Protection du sous-traitant", items: [
            "Procédure d'acceptation et d'agrément par le MO (art. 3 L.1975) — sinon pas d'action directe",
            "Cautionnement bancaire ou délégation (art. 14) — à peine de nullité relative",
            "Action directe en paiement contre le MO (art. 11 ss) — sous double plafond"
          ]}
        ]
      }
    ]
  },
  {
    id: 5,
    title: "Le Contrat de Mandat",
    subtitle: "Titre II — Service personnel",
    color: "#1d2d44",
    accent: "#4ecdc4",
    icon: "🤝",
    sections: [
      {
        title: "Définition & Qualification",
        content: [
          { type: "def", label: "Définition (art. 1984)", text: "Contrat par lequel le mandant charge le mandataire d'accomplir des actes juridiques en son nom et pour son compte." },
          { type: "rule", label: "Éléments de qualification", items: [
            "Accomplissement d'ACTES JURIDIQUES (≠ actes matériels du contrat d'entreprise)",
            "Action AU NOM ET POUR LE COMPTE du mandant (représentation parfaite)",
            "Absence de subordination (mandataire indépendant)"
          ]},
          { type: "comparison", rows: [
            { label: "Représentation parfaite (mandat)", a: "Actes produits dans le patrimoine du mandant. Mandataire transparent." },
            { label: "Représentation imparfaite (commission)", a: "Commissionnaire agit en son nom propre pour le compte du commettant (art. L.132-1 C.com). Fait écran entre commettant et tiers." },
            { label: "Représentation occulte (prête-nom)", a: "Le prête-nom dissimule sa qualité de représentant. Application de la simulation. PPT acquise par le prête-nom." }
          ]}
        ]
      },
      {
        title: "Formation du Mandat",
        content: [
          { type: "rule", label: "Conditions de fond", items: [
            "Mandat spécial (actes déterminés) ou général (tous actes d'administration — art. 1988)",
            "Interprétation STRICTE du mandat (art. 1989)",
            "Capacité du mandant = capacité requise pour l'acte à conclure",
            "Aucune capacité spéciale requise pour le mandataire (art. 1990)"
          ]},
          { type: "rule", label: "Conditions de forme", items: [
            "Principe : contrat consensuel",
            "Exception : parallélisme des formes (mandat pour acte solennel → mandat solennel)",
            "Mandat spécial exprès requis pour les actes graves (art. 1988)"
          ]},
          { type: "def", label: "Rémunération (art. 1986)", text: "Présumé GRATUIT (service d'amis — conception désuète). Exception : mandat professionnel présumé ONÉREUX. Art. 1165 : le mandataire peut fixer le prix après exécution, mais doit le justifier. Le juge peut réviser les honoraires excessifs." }
        ]
      },
      {
        title: "Effets — Obligations du Mandataire",
        content: [
          { type: "list", label: "Obligations du mandataire", items: [
            "Exécuter la mission (conformément aux instructions, dans les délais)",
            "Procéder aux vérifications nécessaires",
            "Obligation d'information et de conseil (mandataire professionnel)",
            "Obligation de loyauté : ne peut contracter avec le mandant (art. 1161) ni se porter acquéreur des biens à vendre (art. 1596)",
            "Rendre compte de la mission et restituer ce reçu pour le compte du mandant (art. 1993)"
          ]},
          { type: "rule", label: "Responsabilité du mandataire", items: [
            "Inexécution → obligation de RÉSULTAT (art. 1991 — exonération par FM seulement)",
            "Mauvaise exécution → obligation de MOYENS (art. 1992 — mandant prouve la faute)",
            "Faute appréciée moins rigoureusement si mandat gratuit (art. 1992 al.2)"
          ]},
          { type: "def", label: "Sous-mandat (art. 1994)", text: "Admis même sans autorisation du mandant. Responsabilité du mandataire principal limitée : il répond du sous-mandataire si substitution non autorisée OU choix d'un sous-mandataire notoi rement incapable/insolvable." }
        ]
      },
      {
        title: "Effets — Rapports Externes & Extinction",
        content: [
          { type: "rule", label: "Représentation parfaite : effets", items: [
            "Mandataire transparent : les actes produisent leurs effets mandant/tiers",
            "Dépassement de pouvoirs → actes inopposables au mandant (art. 1156 al.1)",
            "Mandat apparent (art. 1156 al.1) : engage le mandant si le tiers pouvait légitimement croire aux pouvoirs"
          ]},
          { type: "rule", label: "Causes d'extinction", items: [
            "Révocation par le mandant (libre, même sans motif — art. 2004) sauf abus de droit",
            "Renonciation du mandataire (avec indemnisation si préjudice — art. 2007)",
            "Décès, tutelle, déconfiture de l'un ou l'autre (art. 2003)"
          ]},
          { type: "info", label: "Protection des tiers", text: "Si le mandataire ignore la cause d'extinction → actes accomplis valables et engagent le mandant (ou ses ayants-droits). Tiers de bonne foi protégés (art. 2005)." }
        ]
      }
    ]
  },
  {
    id: 6,
    title: "Le Contrat de Dépôt",
    subtitle: "Titre III — Service personnel",
    color: "#1a2035",
    accent: "#a8dadc",
    icon: "📦",
    sections: [
      {
        title: "Qualification",
        content: [
          { type: "def", label: "Définition (art. 1915)", text: "Contrat par lequel le dépositaire est tenu de garder la chose mobilière du déposant pour la lui restituer en nature au terme du contrat." },
          { type: "rule", label: "Éléments de qualification", items: [
            "GARDE = prestation PRINCIPALE du dépositaire",
            "TRANSFERT DE LA GARDE du déposant au dépositaire",
            "Choses MOBILIÈRES uniquement (art. 1918) — immeubles → contrat de gardiennage = entreprise",
            "Le dépositaire ne peut PAS utiliser les choses déposées (art. 1930) → sinon prêt à usage"
          ]},
          { type: "info", label: "Contrat réel (art. 1919)", text: "Le dépôt ne se forme que par la REMISE de la chose. Principe du consensualisme écarté." }
        ]
      },
      {
        title: "Obligations du Dépositaire",
        content: [
          { type: "def", label: "Obligation de garde", text: "Obligation de RÉSULTAT ATTÉNUÉE : le dépositaire est responsable des pertes/détériorations, sauf s'il prouve l'absence de faute. La charge de la preuve est sur lui car il est le mieux à même d'expliquer les circonstances." },
          { type: "rule", label: "Appréciation de la faute", items: [
            "Dépôt À TITRE ONÉREUX → faute in abstracto (comportement d'un dépositaire raisonnable)",
            "Dépôt À TITRE GRATUIT → faute in concreto (comparaison avec ses propres habitudes)"
          ]},
          { type: "rule", label: "Obligation de restitution (art. 1932 & 1944)", items: [
            "Restitution À L'IDENTIQUE (≠ dépôt irrégulier de choses fongibles → par équivalent)",
            "Restitution dès que le déposant la réclame, même avant le terme (terme = intérêt du déposant)",
            "Restitution dans l'état dans lequel elle se trouve (art. 1933)"
          ]}
        ]
      },
      {
        title: "Régimes Spéciaux",
        content: [
          { type: "comparison", rows: [
            { label: "Dépôt hôtelier (art. 1953-1954)", a: "Obligation de RÉSULTAT pour l'hôtelier, mais responsabilité PLAFONNÉE pour les objets laissés en chambre (non confiés spécialement)." },
            { label: "Dépôt hospitalier", a: "Règles spéciales dans le Code de la santé publique." },
            { label: "Dépôt nécessaire (art. 1949)", a: "Dépôt contraint par un évènement accidentel → preuve libre (dérogation au droit commun)." }
          ]},
          { type: "def", label: "Dépôt irrégulier", text: "Porte sur des choses fongibles (ex : dépôt bancaire). Le dépositaire peut disposer des choses → devient propriétaire. Restitution par équivalent. Controverse : cette analyse est critiquée (le dépôt bancaire pourrait être un contrat sui generis)." }
        ]
      }
    ]
  },
  {
    id: 7,
    title: "Le Contrat de Bail",
    subtitle: "Partie III — Mise à disposition d'une chose",
    color: "#1e1e2e",
    accent: "#cba6f7",
    icon: "🏠",
    sections: [
      {
        title: "Définition & Qualification",
        content: [
          { type: "def", label: "Définition (art. 1709)", text: "Contrat par lequel le bailleur s'oblige à procurer la jouissance d'une chose au locataire pendant un certain temps, moyennant un loyer." },
          { type: "rule", label: "Distinctions", items: [
            "vs Prêt à usage : le bail est ONÉREUX (loyer) ; le prêt est gratuit",
            "vs Droits réels (usufruit) : le locataire a un droit PERSONNEL (créance) ≠ droit réel",
            "vs Convention d'occupation précaire (COP) : la COP doit être justifiée par des circonstances exceptionnelles légitimes (ex: mise en vente de l'immeuble)"
          ]}
        ]
      },
      {
        title: "Droit Commun du Bail — Formation",
        content: [
          { type: "rule", label: "Règles de fond", items: [
            "Durée : déterminée ou indéterminée (pas perpétuelle — art. 1210 : requalifié en CDI)",
            "Loyer : déterminé ou déterminable à peine de nullité",
            "Bailleur : doit être propriétaire (bail de la chose d'autrui = inopposable au vrai propriétaire, mais valable entre les parties)"
          ]},
          { type: "info", label: "Forme & Publicité", text: "Bail consensuel (art. 1714). Exception : bail rural et bail d'habitation → écrit requis. Publicité foncière obligatoire pour bail > 12 ans (diminue fortement la valeur de l'immeuble)." }
        ]
      },
      {
        title: "Obligations du Bailleur",
        content: [
          { type: "rule", label: "1. Délivrance (art. 1719-1°)", items: [
            "Mettre la chose à disposition du locataire",
            "En BON ÉTAT de réparation (art. 1720)",
            "Si logement : obligation de décence (art. 1719-1° et Loi 1989 art. 6)"
          ]},
          { type: "rule", label: "2. Entretien (art. 1719-2°)", items: [
            "Faire toutes les réparations NON locatives en cours de bail",
            "Sanctions : exception d'inexécution (suspension loyers) — mais JP exige impossibilité TOTALE de jouissance"
          ]},
          { type: "rule", label: "3. Jouissance paisible (art. 1719-3°)", items: [
            "Garantie des vices : obligation de résultat, couvre les vices APPARUS en cours de bail (≠ vices cachés limités à l'antériorité)",
            "Garantie contre les troubles de droit des tiers (≠ troubles de fait : locataire se défend seul)",
            "Interdiction de modifier la chose (art. 1723)"
          ]}
        ]
      },
      {
        title: "Obligations du Locataire & Sous-location",
        content: [
          { type: "list", label: "Obligations du locataire", items: [
            "Payer les loyers (colocation → division par tête sauf clause de solidarité)",
            "User de la chose conformément à sa destination (art. 1728) → résiliation possible (art. 1729)",
            "Effectuer les réparations locatives",
            "Ne pas modifier la chose sans autorisation",
            "Restituer la chose en fin de bail"
          ]},
          { type: "rule", label: "Sous-location", items: [
            "Autorisée sauf clause contraire (art. 1717)",
            "Irrégulière : résiliation + sous-loyers acquis au bailleur par accession",
            "Régulière : action directe du bailleur contre le sous-locataire (art. 1753 — double plafond)"
          ]}
        ]
      },
      {
        title: "Extinction du Bail",
        content: [
          { type: "rule", label: "Causes", items: [
            "Expiration de la durée (CDI : congé ; CDD : terme extinctif)",
            "Tacite reconduction (art. 1738) : si locataire laissé en possession à l'expiration → nouveau bail à durée INDÉTERMINÉE",
            "Résolution/résiliation pour inexécution",
            "Destruction totale fortuite (art. 1722)"
          ]},
          { type: "rule", label: "Événements sans incidence", items: [
            "Décès du bailleur ou du locataire (art. 1742) → bail transmis aux héritiers",
            "Vente de la chose louée (art. 1743) → l'acheteur devient le nouveau bailleur (cession légale de contrat). Conditions : bail immobilier + date certaine OU connaissance de l'acquéreur"
          ]}
        ]
      },
      {
        title: "Statuts Spéciaux du Bail",
        content: [
          { type: "comparison", rows: [
            { label: "Bail d'habitation (Loi 1989)", a: "Résidence principale. Durée min : 3 ans (PP) ou 6 ans (PM). Locataire : congé à tout moment (préavis 3 mois ou 1 mois dans certains cas). Bailleur : congé à l'échéance pour motif légitime, vente ou reprise (préavis 6 mois). Droit de préemption du locataire en cas de vente. Sur-protection des + 65 ans sous plafond de ressources." },
            { label: "Location meublée (art. 25-3 ss.)", a: "Durée min : 1 an (9 mois pour étudiants). Bail mobilité : 1 à 10 mois, non renouvelable." },
            { label: "Bail commercial (L.145-1 C.com)", a: "Durée min : 9 ans. Droit au renouvellement. Refus de renouveler → indemnité d'éviction (valeur du FC). Commerçants, artisans, établissements d'enseignement." },
            { label: "Bail rural (Code rural)", a: "Durée min : 9 ans. Droit de préemption du preneur. Droit au renouvellement (reprise limitée au bailleur et proches)." }
          ]}
        ]
      }
    ]
  },
  {
    id: 8,
    title: "Le Contrat de Prêt",
    subtitle: "Partie III — Mise à disposition d'une chose",
    color: "#12212d",
    accent: "#52b788",
    icon: "💰",
    sections: [
      {
        title: "Les deux variétés de prêt",
        content: [
          { type: "comparison", rows: [
            { label: "Prêt à usage (commodat)", a: "Chose non consomptible. Gratuit par essence (art. 1876). Prêteur reste propriétaire (art. 1877). Restitution à l'IDENTIQUE." },
            { label: "Prêt de consommation (mutuum)", a: "Chose consomptible (fongible). Peut être onéreux (avec intérêts — art. 1905). TRANSLATIF de propriété (art. 1893). Restitution par ÉQUIVALENT." }
          ]},
          { type: "info", label: "Contrats réels", text: "Les deux types de prêt sont des CONTRATS RÉELS : ils ne se forment que par la REMISE de la chose. Une promesse de prêt non exécutée ne donne droit qu'à des D&I (pas d'exécution forcée)." }
        ]
      },
      {
        title: "Prêt à Usage — Régime",
        content: [
          { type: "rule", label: "Obligations de l'emprunteur", items: [
            "Usage conforme à la destination normale (art. 1880) — usage personnel (contrat intuitu personae) — pas de sous-location sans accord",
            "Conservation de la chose : obligation de RÉSULTAT ATTÉNUÉE",
            "3 cas de responsabilité même en cas de FM : abus d'usage / retard de restitution / préférence à sa propre chose",
            "Restitution à l'identique à l'expiration du prêt"
          ]},
          { type: "rule", label: "Obligations du prêteur", items: [
            "Remboursement des frais de conservation (art. 1890)",
            "Information sur les vices connus (art. 1891) — ≠ garantie des vices cachés (prêt gratuit)"
          ]},
          { type: "def", label: "Restitution anticipée (art. 1889)", text: "Par faveur pour le prêteur (contrat gratuit) : le prêteur peut réclamer la chose avant le terme en cas de BESOIN PRESSANT ET IMPRÉVU." },
          { type: "info", label: "Extinction", text: "Décès de l'emprunteur éteint le prêt (présomption intuitu personae due à la gratuité — art. 1879). Si prêteur décède → contrat transmis aux héritiers." }
        ]
      },
      {
        title: "Prêt de Consommation — Régime",
        content: [
          { type: "rule", label: "Effet translatif de propriété", items: [
            "L'emprunteur devient PROPRIÉTAIRE des choses prêtées (art. 1893)",
            "Il supporte les risques (res perit domino)",
            "Reste tenu de restituer par équivalent même si la chose a péri par FM"
          ]},
          { type: "rule", label: "Extinction", items: [
            "Durée déterminée : prêteur NE PEUT PAS réclamer avant le terme (≠ prêt à usage) — art. 1899",
            "Durée indéterminée : prêteur peut demander la restitution à tout moment (préavis raisonnable). Le juge peut accorder un délai à l'emprunteur (art. 1900)"
          ]},
          { type: "info", label: "Garantie des vices", text: "Pas de garantie des vices cachés (même régime que prêt à usage — art. 1898 renvoie à art. 1891) : obligation d'information sur les vices connus seulement." }
        ]
      }
    ]
  }
];

const typeColors = {
  def: { bg: "rgba(255,200,100,0.12)", border: "#f5a623", icon: "📌" },
  rule: { bg: "rgba(100,200,255,0.10)", border: "#66c0f4", icon: "📋" },
  info: { bg: "rgba(100,255,150,0.10)", border: "#52b788", icon: "💡" },
  list: { bg: "rgba(200,150,255,0.10)", border: "#cba6f7", icon: "📎" },
  comparison: { bg: "rgba(255,100,100,0.08)", border: "#e94560", icon: "⚡" },
};

function ContentBlock({ block }) {
  const style = typeColors[block.type] || typeColors.info;
  return (
    <div style={{
      background: style.bg,
      borderLeft: `3px solid ${style.border}`,
      borderRadius: "8px",
      padding: "14px 16px",
      marginBottom: "12px",
    }}>
      {block.label && (
        <div style={{ display: "flex", alignItems: "center", gap: "6px", marginBottom: "8px" }}>
          <span style={{ fontSize: "14px" }}>{style.icon}</span>
          <span style={{ fontSize: "11px", fontWeight: "700", letterSpacing: "0.08em", color: style.border, textTransform: "uppercase" }}>
            {block.label}
          </span>
        </div>
      )}
      {block.type === "def" || block.type === "info" ? (
        <p style={{ margin: 0, fontSize: "13.5px", lineHeight: "1.65", color: "#e0e0e0" }}>{block.text}</p>
      ) : block.type === "rule" || block.type === "list" ? (
        Array.isArray(block.items) ? (
          <ul style={{ margin: 0, paddingLeft: "18px" }}>
            {block.items.map((item, i) => (
              <li key={i} style={{ fontSize: "13px", lineHeight: "1.7", color: "#d0d0d0", marginBottom: "4px" }}>{item}</li>
            ))}
          </ul>
        ) : (
          <p style={{ margin: 0, fontSize: "13.5px", lineHeight: "1.65", color: "#e0e0e0" }}>{block.items}</p>
        )
      ) : block.type === "comparison" ? (
        <div>
          {block.rows.map((row, i) => (
            <div key={i} style={{
              display: "grid",
              gridTemplateColumns: "180px 1fr",
              gap: "10px",
              marginBottom: "8px",
              paddingBottom: "8px",
              borderBottom: i < block.rows.length - 1 ? "1px solid rgba(255,255,255,0.07)" : "none"
            }}>
              <div style={{ fontSize: "11.5px", fontWeight: "700", color: style.border, paddingTop: "2px" }}>{row.label}</div>
              <div style={{ fontSize: "13px", lineHeight: "1.6", color: "#d0d0d0" }}>{row.a}</div>
            </div>
          ))}
        </div>
      ) : null}
    </div>
  );
}

function SectionCard({ section }) {
  const [open, setOpen] = useState(false);
  return (
    <div style={{
      background: "rgba(255,255,255,0.04)",
      borderRadius: "12px",
      border: "1px solid rgba(255,255,255,0.08)",
      marginBottom: "10px",
      overflow: "hidden",
      transition: "border-color 0.2s",
    }}>
      <button
        onClick={() => setOpen(!open)}
        style={{
          width: "100%",
          background: "none",
          border: "none",
          padding: "14px 18px",
          display: "flex",
          justifyContent: "space-between",
          alignItems: "center",
          cursor: "pointer",
          textAlign: "left",
          gap: "10px",
        }}
      >
        <span style={{ fontSize: "14px", fontWeight: "600", color: "#f0f0f0", lineHeight: "1.4" }}>{section.title}</span>
        <span style={{
          fontSize: "18px",
          color: "#888",
          transform: open ? "rotate(180deg)" : "rotate(0deg)",
          transition: "transform 0.25s",
          flexShrink: 0
        }}>▾</span>
      </button>
      {open && (
        <div style={{ padding: "0 18px 16px" }}>
          {section.content.map((block, i) => <ContentBlock key={i} block={block} />)}
        </div>
      )}
    </div>
  );
}

export default function App() {
  const [activeChapter, setActiveChapter] = useState(null);
  const [searchQuery, setSearchQuery] = useState("");

  const filtered = chapters.filter(c =>
    !searchQuery ||
    c.title.toLowerCase().includes(searchQuery.toLowerCase()) ||
    c.subtitle.toLowerCase().includes(searchQuery.toLowerCase())
  );

  return (
    <div style={{
      minHeight: "100vh",
      background: "#0d0d14",
      fontFamily: "'Georgia', 'Times New Roman', serif",
      color: "#f0f0f0",
    }}>
      {/* Header */}
      <div style={{
        background: "linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%)",
        padding: "40px 24px 32px",
        textAlign: "center",
        borderBottom: "1px solid rgba(255,255,255,0.08)",
        position: "relative",
        overflow: "hidden",
      }}>
        <div style={{
          position: "absolute", inset: 0,
          background: "radial-gradient(ellipse at 50% 0%, rgba(233,69,96,0.15) 0%, transparent 60%)",
          pointerEvents: "none"
        }} />
        <div style={{ fontSize: "13px", letterSpacing: "0.2em", color: "#e94560", marginBottom: "10px", fontFamily: "monospace", textTransform: "uppercase" }}>
          Fiches de Révision
        </div>
        <h1 style={{ margin: "0 0 8px", fontSize: "clamp(22px,4vw,32px)", fontWeight: "700", letterSpacing: "-0.02em", color: "#fff" }}>
          Droit des Contrats Civils<br/>& Commerciaux
        </h1>
        <p style={{ margin: "0 0 24px", color: "#888", fontSize: "14px" }}>
          Cours complet • {chapters.length} thèmes • {chapters.reduce((a, c) => a + c.sections.length, 0)} sections
        </p>
        {/* Search */}
        <div style={{ maxWidth: "400px", margin: "0 auto", position: "relative" }}>
          <span style={{ position: "absolute", left: "14px", top: "50%", transform: "translateY(-50%)", fontSize: "16px" }}>🔍</span>
          <input
            type="text"
            placeholder="Rechercher un thème..."
            value={searchQuery}
            onChange={e => { setSearchQuery(e.target.value); setActiveChapter(null); }}
            style={{
              width: "100%",
              padding: "10px 14px 10px 40px",
              background: "rgba(255,255,255,0.08)",
              border: "1px solid rgba(255,255,255,0.15)",
              borderRadius: "8px",
              color: "#f0f0f0",
              fontSize: "14px",
              outline: "none",
              boxSizing: "border-box",
              fontFamily: "inherit",
            }}
          />
        </div>
      </div>

      <div style={{ maxWidth: "900px", margin: "0 auto", padding: "24px 16px" }}>
        {/* Chapter navigation pills */}
        {!searchQuery && (
          <div style={{
            display: "flex",
            flexWrap: "wrap",
            gap: "8px",
            marginBottom: "28px",
            justifyContent: "center"
          }}>
            {chapters.map(c => (
              <button
                key={c.id}
                onClick={() => setActiveChapter(activeChapter === c.id ? null : c.id)}
                style={{
                  padding: "7px 14px",
                  borderRadius: "20px",
                  border: `1.5px solid ${activeChapter === c.id ? c.accent : "rgba(255,255,255,0.12)"}`,
                  background: activeChapter === c.id ? `${c.accent}22` : "transparent",
                  color: activeChapter === c.id ? c.accent : "#bbb",
                  fontSize: "12px",
                  fontWeight: activeChapter === c.id ? "700" : "400",
                  cursor: "pointer",
                  transition: "all 0.2s",
                  fontFamily: "inherit",
                }}
              >
                {c.icon} {c.title}
              </button>
            ))}
          </div>
        )}

        {/* Chapter cards */}
        {filtered.map(chapter => {
          const isExpanded = activeChapter === chapter.id || !!searchQuery;
          return (
            <div
              key={chapter.id}
              style={{
                background: `linear-gradient(135deg, ${chapter.color} 0%, rgba(13,13,20,0.95) 100%)`,
                borderRadius: "16px",
                border: `1px solid ${activeChapter === chapter.id ? chapter.accent + "55" : "rgba(255,255,255,0.06)"}`,
                marginBottom: "16px",
                overflow: "hidden",
                transition: "border-color 0.3s",
              }}
            >
              {/* Chapter header */}
              <div
                onClick={() => !searchQuery && setActiveChapter(activeChapter === chapter.id ? null : chapter.id)}
                style={{
                  padding: "20px 24px",
                  cursor: searchQuery ? "default" : "pointer",
                  display: "flex",
                  alignItems: "center",
                  gap: "14px",
                  borderBottom: isExpanded ? `1px solid rgba(255,255,255,0.06)` : "none",
                }}
              >
                <div style={{
                  width: "44px",
                  height: "44px",
                  borderRadius: "12px",
                  background: `${chapter.accent}22`,
                  border: `1.5px solid ${chapter.accent}44`,
                  display: "flex",
                  alignItems: "center",
                  justifyContent: "center",
                  fontSize: "22px",
                  flexShrink: 0,
                }}>
                  {chapter.icon}
                </div>
                <div style={{ flex: 1 }}>
                  <div style={{ fontSize: "11px", color: chapter.accent, letterSpacing: "0.1em", textTransform: "uppercase", fontWeight: "600", marginBottom: "3px", fontFamily: "monospace" }}>
                    {chapter.subtitle}
                  </div>
                  <div style={{ fontSize: "17px", fontWeight: "700", color: "#fff", lineHeight: "1.3" }}>
                    {chapter.title}
                  </div>
                  <div style={{ fontSize: "12px", color: "#666", marginTop: "3px" }}>
                    {chapter.sections.length} section{chapter.sections.length > 1 ? "s" : ""}
                  </div>
                </div>
                {!searchQuery && (
                  <span style={{
                    fontSize: "20px",
                    color: "#555",
                    transform: isExpanded ? "rotate(180deg)" : "rotate(0deg)",
                    transition: "transform 0.25s",
                  }}>▾</span>
                )}
              </div>

              {/* Sections */}
              {isExpanded && (
                <div style={{ padding: "16px 20px 8px" }}>
                  {chapter.sections.map((section, i) => (
                    <SectionCard key={i} section={section} />
                  ))}
                </div>
              )}
            </div>
          );
        })}

        {/* Footer */}
        <div style={{ textAlign: "center", padding: "20px 0", color: "#444", fontSize: "12px" }}>
          Cours de Droit des Contrats Civils et Commerciaux — Kenza Ezzahrati
        </div>
      </div>
    </div>
  );
}
