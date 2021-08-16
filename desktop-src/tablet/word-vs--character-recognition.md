---
description: Al establecer la propiedad Factoid en None, el reconocedor de caracteres reconoce la escritura a mano por carácter.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Reconocimiento de palabras frente a caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e704943afb2b411441752056aace0889e87483fc4992d59c39ea6a135ef76b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966604"
---
# <a name="word-vs-character-recognition"></a>Reconocimiento de palabras frente a caracteres

Al establecer la [propiedad Factoid](/previous-versions/ms835848(v=msdn.10)) en **None**, el reconocedor de caracteres reconoce la escritura a mano por carácter.

La [propiedad RecoTimeout](/previous-versions/ms835852(v=msdn.10)) [**(RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) en Automation) especifica el número [](/previous-versions/ms552692(v=vs.100)) de milisegundos de retraso entre el último trazo y el final de la entrada de escritura a mano. Puede aumentar este valor para reconocer texto antes de que se escriban palabras o oraciones enteras. También puede forzar el reconocimiento de la entrada de lápiz inmediatamente mediante el [método Recognize.](/previous-versions/ms836275(v=msdn.10))

 

 
