---
title: Navegar a otras tiendas en línea
description: Navegar a otras tiendas en línea
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Reproductor de Windows Media en línea, navegar
- tiendas en línea, navegar
- tiendas en línea de tipo 2, navegar
- navegar por tiendas en línea de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967452"
---
# <a name="navigating-to-other-online-stores"></a>Navegar a otras tiendas en línea

Puede crear vínculos a otras tiendas en línea de su propiedad o a otras tiendas en línea proporcionadas por otros usuarios. Para ello, debe conocer el nombre de clave de la tienda en línea a la que desea navegar.

En el código de ejemplo siguiente se muestra HTML que crea un vínculo para cambiar de la tienda en línea de Proseware a la característica "ServiceTask2" de la tienda en línea South qr Video:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Cuando el usuario hace clic en el vínculo, Reproductor de Windows Media solicita al usuario que cambie al almacén de Vídeos de Southcore. Si el usuario lo permite, el Reproductor cambia los almacenes y navega al panel de tareas especificado, anexando los parámetros de la cadena de consulta. Los parámetros de cadena de consulta que se muestran en el ejemplo anterior son parámetros personalizados. Esto significa que la tienda en línea a la que cambia debe esperar estos valores y controlarlos. El almacén en línea (y cualquier almacén al que cambie) puede usar parámetros de cadena de consulta de la forma que elija.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Navegar entre los paneles de tareas de servicio**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navegación para tiendas en línea de tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




