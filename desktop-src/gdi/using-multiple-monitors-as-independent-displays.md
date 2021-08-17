---
description: Cuando se usan varios monitores como pantallas independientes, el escritorio contiene una pantalla o un conjunto de pantallas.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Usar varios monitores como pantallas independientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710672e02e8ea7244e09c21b876197033e5f17144433b8f530ad8e52cd6806e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468255"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Usar varios monitores como pantallas independientes

Cuando se usan varios monitores como pantallas independientes, el escritorio contiene una pantalla o un conjunto de pantallas. Este conjunto de pantallas siempre incluye el monitor principal y se comporta como se mencionó en las otras secciones de este tema. Una aplicación puede usar cualquier otro monitor como una pantalla independiente.

> [!Note]  
> El uso de otros monitores como pantallas independientes no se admite en los controladores que se implementan en Windows Modelo de controlador de pantalla (WDDM).

 

El administrador de ventanas no sabe nada sobre las pantallas independientes. La aplicación los controla completamente y no hay ninguna función de administrador de ventanas disponible para la aplicación (todas las llamadas del administrador de ventanas van automáticamente a la pantalla principal). Cada pantalla independiente tiene su propio origen y coordenadas horizontales y verticales, y se accede a través de las funciones GDI, como [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) o las funciones de DirectX, **como DirectDrawCreate.**

Para buscar las pantallas independientes, llame [**a EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) y busque las pantallas que no tengan la marca DISPLAY DEVICE ATTACHED TO DESKTOP en la estructura \_ DISPLAY \_ \_ \_ [**\_ DEVICE.**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea)

Una aplicación puede abrir una pantalla mediante una llamada a


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



En esta llamada, el parámetro *lpszDisplayName* es uno de los nombres de dispositivo devueltos por [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) y *lpDevMode* es una descripción del modo gráfico para este dispositivo. El hdc resultante se puede usar para realizar cualquier operación de gráficos en el dispositivo.

 

 



