---
description: Monitor de red o el archivo DLL del analizador pueden dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Datos de formato mostrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540219"
---
# <a name="formatting-displayed-data"></a>Datos de formato mostrados

Monitor de red o el archivo DLL del analizador pueden dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.

Monitor de red proporciona un formateador genérico que proporciona los servicios básicos necesarios para mostrar la mayoría de los tipos de datos que existen dentro de un protocolo. Sin embargo, el formateador genérico no admite todos los tipos de datos. Por ejemplo, el formateador genérico no admite lo siguiente:

-   Varios tipos de direcciones.
-   Nombres descriptivos de origen y destino.
-   Identificadores de objetos.
-   Tipos de datos enteros grandes.
-   Tipos de datos enteros de longitud variable pequeños.

En el ejemplo siguiente se identifican dos cadenas con formato para la propiedad ID. de privilegio.

-   La primera línea de código muestra la salida del formateador genérico. El resultado se basa en el tipo de datos.
-   En la segunda línea de código se muestra la salida de un formateador personalizado con una cadena para los datos de la propiedad.

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> Cuando sea posible, use el formateador genérico para mostrar los datos porque le permite controlar el tamaño de la DLL del analizador y proporciona mejores capacidades multiplataforma para el archivo DLL del analizador.

 

 

 



