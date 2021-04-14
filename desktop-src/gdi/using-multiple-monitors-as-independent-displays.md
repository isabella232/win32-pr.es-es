---
description: Cuando se usan varios monitores como pantallas independientes, el escritorio contiene una pantalla o un conjunto de pantallas.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Usar varios monitores como pantallas independientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985914"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Usar varios monitores como pantallas independientes

Cuando se usan varios monitores como pantallas independientes, el escritorio contiene una pantalla o un conjunto de pantallas. Este conjunto de pantallas incluye siempre el monitor principal y se comporta como se mencionó en las otras secciones de este tema. Una aplicación puede utilizar cualquier otro monitor como una pantalla independiente.

> [!Note]  
> No se admite el uso de otros monitores como pantallas independientes en los controladores que se implementan en el modelo de controladores de pantalla de Windows (WDDM).

 

El administrador de ventanas no sabe nada acerca de las pantallas independientes. Están completamente controlados por la aplicación y no hay ninguna función de administrador de ventanas disponible para la aplicación (todas las llamadas del administrador de ventanas pasan automáticamente a la pantalla principal). Cada pantalla independiente tiene su propio origen y coordenadas horizontales y verticales, y se obtiene acceso a ellas a través de las funciones GDI como [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) o las funciones de DirectX como **DirectDrawCreate**.

Para buscar las pantallas independientes, llame a [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) y busque las pantallas que no tienen el \_ dispositivo de pantalla \_ conectado \_ a \_ la marca de escritorio en la estructura de [**pantalla del \_ dispositivo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .

Una aplicación puede abrir una pantalla llamando a


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



En esta llamada, el parámetro *lpszDisplayName* es uno de los nombres de dispositivo devueltos por [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) y *lpDevMode* es una descripción del modo gráficos para este dispositivo. La HDC resultante se puede usar para realizar cualquier operación de gráficos en el dispositivo.

 

 



