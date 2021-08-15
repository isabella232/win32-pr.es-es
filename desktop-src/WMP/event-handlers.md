---
title: Controladores de eventos
description: Controladores de eventos
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Reproductor de Windows Media máscaras, controladores de eventos en JScript
- máscaras, controladores de eventos en JScript
- events,JScript
- JScript archivos para máscaras, controladores de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c936e36cd9b7404260473068ccc3d6c3f5d0ab75553ba878dff88587e535ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339276"
---
# <a name="event-handlers"></a>Controladores de eventos

Microsoft JScript se usa para procesar eventos en el archivo de definición de máscara. Consulte [Control de eventos](handling-events.md) para obtener más información sobre los controladores de eventos.

Puede tener más de una línea de código en un controlador de eventos, pero debe tener cuidado de no superar la longitud de línea que JScript permite. Separe las líneas por punto y coma.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de JScript**](using-jscript.md)
</dt> </dl>

 

 




