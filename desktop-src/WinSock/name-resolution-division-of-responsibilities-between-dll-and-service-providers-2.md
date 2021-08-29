---
title: Resolución de nombres para dll y proveedores de servicios
description: En los párrafos siguientes se describe cómo Ws232.dll y los proveedores de espacios de nombres implementan los servicios de resolución de nombres compatibles \_ con la API Winsock.
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f0ecd7e40d27d6dd9faa541bbca8f7543e6538702599de78a64104f10b1c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097715"
---
# <a name="name-resolution-for-dll-and-service-providers"></a>Resolución de nombres para dll y proveedores de servicios

En los párrafos siguientes se describe cómo Ws232.dll y los proveedores de espacios de nombres implementan los servicios de resolución de nombres compatibles \_ con la API Winsock.

## <a name="ws2_32dll-functionality-for-name-resolution"></a>Funcionalidad de \_32.dll Ws2 para la resolución de nombres

El proveedor Ws232.dll el registro y la carga de demanda de archivos DLL de proveedor de espacios \_ de nombres individuales. También es responsable de enrutar las operaciones del espacio de nombres Windows sockets 2 al conjunto adecuado de proveedores de espacios de nombres. Esta asignación se rige por el valor de los parámetros de identificador de proveedor de servicios y espacio de nombres que se encuentran en funciones de API individuales. Como regla general, cuando se hace referencia a un proveedor de espacio de nombres específico, la operación solo se enruta a un proveedor identificado. Si el identificador del proveedor de espacios de nombres es NULL pero se hace referencia a un espacio de nombres determinado, la operación se enruta a todos los proveedores de espacios de nombres que admiten el espacio de nombres identificado. Si el identificador del proveedor de espacios de nombres es NULL y el identificador de espacio de nombres se proporciona como NS ALL, la operación se enruta a todos los proveedores de espacios \_ de nombres activos.

Como parte del inicio de una consulta a uno o varios proveedores de servicios, el32.dll Ws2 asigna un objeto para realizar un seguimiento del estado en \_ curso de la consulta. Se devuelve un identificador opaco que representa este objeto a la aplicación que inició la consulta. La aplicación proporciona este identificador como parámetro cada vez que llama de forma repetitiva a una función de interfaz de aplicación para recuperar la siguiente unidad de datos resultante de la consulta.

En respuesta a estas llamadas a procedimientos de interfaz de aplicación, el32.dll Ws2 usa la información que almacena en el objeto para realizar llamadas correspondientes a los proveedores de espacios de nombres implicados en \_ la consulta. El32.dll Ws2 actualiza la información en su objeto a medida que se produce cada llamada de interfaz de aplicación sucesiva para que las llamadas correspondientes a los proveedores de espacios de nombres progresan correctamente a través de todos los proveedores de espacios de nombres implicados en la \_ consulta.

## <a name="namespace-provider-functionality"></a>Funcionalidad del proveedor de espacios de nombres

Cada proveedor de espacios de nombres es responsable de asignar el conjunto de funciones que aparecen en el SPI de resolución de nombres de Windows Sockets 2 a las transacciones adecuadas con el espacio de nombres admitido. En algunos casos, se trata principalmente de asignar el SPI a cualquier interfaz nativa que exista para el espacio de nombres. En otros, el proveedor de espacios de nombres debe realizar transacciones con el proveedor de espacios de nombres a través de la red. Algunos proveedores de espacios de nombres lo harán mediante llamadas a Windows Sockets API, mientras que otros usarán interfaces privadas para las pilas de transporte asociadas.

 

 



