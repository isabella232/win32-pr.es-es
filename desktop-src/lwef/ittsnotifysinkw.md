---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86cedf8c4a349da800f34f2f6acd7266f9cd0c3c383be9accb72dd162df8e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748713"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El motor debe llamar a través [**de AudioStop,**](https://www.bing.com/search?q=**AudioStop**) [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)y [**Visual**](https://www.bing.com/search?q=**Visual**). La **devolución** de llamada visual debe proporcionar phonemes IPA. (Alfabeto fonético internacional) \[ IPA \] es una notación universal para describir el contenido fonético de la comunicación hablada. Todos los phonemes que se pueden hablar tienen representaciones en IPA. Los detalles de IPA se encuentran en la parte de especificación Speech API Microsoft de la descarga del \[ SDK de Voz 4.0 \] en [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) ).

Aunque la [**notificación visual**](https://www.bing.com/search?q=**Visual**) es bastante enriquezca, Microsoft Agent solo usa el valor **cIPAPhoneme** para animar la voz mientras el carácter habla. Cualquier motor compatible con Microsoft Agent debe proporcionar  un flujo de notificaciones visuales estrechamente sincronizado que refleje el contenido fonético de la expresión producida. En este caso, la "notificación relativamente a tiempo" no es adecuada, ya que los oradores son bastante sensibles a las discrepancias entre la posición de las manos y el contenido acústico. **Las** notificaciones visuales deben devolverse rápidamente.

 

 




