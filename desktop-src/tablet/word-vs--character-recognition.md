---
description: Al establecer la propiedad Factoid en None, el reconocedor de caracteres reconoce la escritura a mano por carácter.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Reconocimiento de palabras frente a caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247706"
---
# <a name="word-vs-character-recognition"></a>Reconocimiento de palabras frente a caracteres

Al establecer la [propiedad Factoid](/previous-versions/ms835848(v=msdn.10)) en **None**, el reconocedor de caracteres reconoce la escritura a mano por carácter.

La [propiedad RecoTimeout](/previous-versions/ms835852(v=msdn.10)) [**(RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) en Automation) especifica el número [](/previous-versions/ms552692(v=vs.100)) de milisegundos de retraso entre el último trazo y el final de la entrada de escritura a mano. Puede aumentar este valor para reconocer texto antes de que se escriban palabras o oraciones enteras. También puede forzar el reconocimiento de la entrada de lápiz inmediatamente mediante el [método Recognize.](/previous-versions/ms836275(v=msdn.10))

 

 
