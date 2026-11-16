# Struggle

Un skill Claude Code qui recentre sur le but quand une demande est trop vague, au lieu de foncer avec une solution toute cuite.

**Le partage des rôles.** Tu décides du but et du sens : quoi, pourquoi, pour qui. Claude trouve les moyens techniques et exécute. Il ne te pose jamais de question technique, et il ne choisit jamais le but à ta place.

## Ce qu'il fait

| Situation | Ce que fait Claude |
|---|---|
| Le but et l'objectif sont clairs | Il exécute, sans question |
| La demande est trop vague (« améliore la home », « propose un truc ») | Il pose la question qui manque, une à la fois, puis il exécute |
| Le travail s'éloigne du but en cours de route | Il rappelle le but en une ligne et demande si ça le sert toujours |
| Tu ne sais pas répondre, tu hésites, tu tournes en rond | Il passe en déblocage avec une méthode éprouvée (5 pourquoi, prochaine action physique, pré-mortem, Mom Test…) |

Il se déclenche tout seul. Tu peux aussi le lancer avec `/struggle`.

## Installer

```bash
npx skills add https://github.com/AlexFrs-777/struggle --skill struggle -g
```

`-g` l'installe pour tous tes projets. Sans `-g`, il ne s'installe que dans le projet courant.

Pour qu'il se déclenche aussi dans les projets où Claude ne pense pas à lui, ajoute dans `~/.claude/CLAUDE.md` :

```markdown
Je décide du but et du sens (quoi, pourquoi, pour qui). Tu décides des moyens techniques et tu exécutes.
Si ma demande est trop vague pour connaître le but ou l'objectif, recentre-moi par une question avant de proposer ou de coder (skill struggle). Sinon, exécute.
```

## Contenu

- `SKILL.md` : les règles du skill.
- `references/methodes.md` : les méthodes de déblocage, chargées seulement quand tu bloques.

Licence MIT.
