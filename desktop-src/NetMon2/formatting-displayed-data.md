---
description: Monitor de red o el archivo DLL del analizador pueden dar formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Datos de formato mostrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071559"
---
# <a name="formatting-displayed-data"></a>Datos de formato mostrados

Monitor de red o el archivo DLL del analizador pueden dar formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario.

Monitor de red proporciona un formateador genérico que proporciona los servicios básicos necesarios para mostrar la mayoría de los tipos de datos que existen dentro de un protocolo. Sin embargo, el formateador genérico no admite todos los tipos de datos. Por ejemplo, el formateador genérico no admite lo siguiente:

-   Varios tipos de direcciones.
-   Nombres descriptivos de origen y destino.
-   Identificadores de objeto.
-   Tipos de datos enteros grandes.
-   Tipos de datos enteros pequeños de longitud variable.

En el ejemplo siguiente se identifican dos cadenas con formato para la propiedad Id. de privilegio.

-   La primera línea de código muestra la salida del formateador genérico. La salida se basa en el tipo de datos.
-   La segunda línea de código muestra la salida de un formateador personalizado con una cadena para los datos de propiedad.

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> Cuando sea posible, use el formateador genérico para mostrar los datos, ya que permite controlar el tamaño de la DLL del analizador y proporciona mejores funcionalidades multiplataforma para el archivo DLL del analizador.

 

 

 



