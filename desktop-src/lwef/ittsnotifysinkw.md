---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420337"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El motor debe llamar a a través de [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)y [**Visual**](https://www.bing.com/search?q=**Visual**). La devolución de llamada **Visual** debe proporcionar IPA fonemas. (El alfabeto \[ fonético internacional IPA \] es una notación universal para describir el contenido fonético de la comunicación oral. Todos los fonemas que se hablan tienen representaciones en IPA. Los detalles de IPA se encuentran en la parte especificación de Microsoft Speech API \[ de la descarga de Speech SDK 4,0 \] en [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)

Aunque la notificación [**Visual**](https://www.bing.com/search?q=**Visual**) es bastante enriquecida, Microsoft Agent solo usa el valor **cIPAPhoneme** para animar la boca a medida que el carácter habla. Cualquier motor compatible con agente de Microsoft debe proporcionar un flujo muy sincronizado de notificaciones **visuales** que reflejen el contenido fonético del utterance generado. En este caso, "notificación relativamente puntual" no es adecuado, ya que los hablantes de los oradores son bastante sensibles a las discrepancias entre la posición de la boca y el contenido acústico. Las notificaciones **visuales** deben devolverse rápidamente.

 

 




