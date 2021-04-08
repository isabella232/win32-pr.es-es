---
title: Resolución de nombres para los proveedores de servicios y DLL
description: En los párrafos siguientes se describe cómo el \_32.dll Ws2 y los proveedores de espacio de nombres implementan los servicios de resolución de nombres admitidos por la API de Winsock.
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b527f0849eb441ab7bc8d096c0198d703f2ce337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001139"
---
# <a name="name-resolution-for-dll-and-service-providers"></a>Resolución de nombres para los proveedores de servicios y DLL

En los párrafos siguientes se describe cómo el \_32.dll Ws2 y los proveedores de espacio de nombres implementan los servicios de resolución de nombres admitidos por la API de Winsock.

## <a name="ws2_32dll-functionality-for-name-resolution"></a>Ws2 \_32.dll funcionalidad para la resolución de nombres

El \_32.dll Ws2 administra el registro y la carga de la demanda de archivos dll individuales del proveedor de espacios de nombres. También es responsable de enrutar las operaciones de espacio de nombres desde una aplicación de Windows Sockets 2 al conjunto de proveedores de espacios de nombres adecuado. Esta asignación se rige por el valor de los parámetros de identificador de proveedor de servicios y espacio de nombres que se encuentran en las funciones individuales de la API. Como norma general, cuando se hace referencia a un proveedor de espacios de nombres específico, la operación solo se enruta a un proveedor identificado. Si el identificador del proveedor de espacio de nombres es null, pero se hace referencia a un espacio de nombres determinado, la operación se enruta a todos los proveedores de espacios de nombres que admiten el espacio de nombres identificado. Si el identificador del proveedor de espacio de nombres es NULL y el identificador del espacio de nombres se proporciona como NS \_ All, la operación se enruta a todos los proveedores de espacios de nombres activos.

Como parte del inicio de una consulta a uno o varios proveedores de servicios, el \_32.dll Ws2 asigna un objeto para realizar un seguimiento del estado actual de la consulta. Un identificador opaco que representa este objeto se devuelve a la aplicación que inició la consulta. La aplicación proporciona este identificador como parámetro cada vez que llama a una función de interfaz de aplicación repetidamente para recuperar la siguiente unidad de datos resultante de la consulta.

En respuesta a estas llamadas a procedimientos de la interfaz de aplicación, el \_32.dll Ws2 utiliza la información que almacena en el objeto para realizar las llamadas correspondientes a los proveedores de espacios de nombres implicados en la consulta. El \_32.dll Ws2 actualiza la información de su objeto, ya que cada llamada de interfaz de aplicación sucesiva se produce para que las llamadas correspondientes a los proveedores de espacios de nombres progresen adecuadamente a través de todos los proveedores de espacio de nombres implicados en la consulta.

## <a name="namespace-provider-functionality"></a>Funcionalidad del proveedor de espacio de nombres

Cada proveedor de espacios de nombres es responsable de asignar el conjunto de funciones que aparecen en el SPI de resolución de nombres de Windows Sockets 2 a las transacciones adecuadas con el espacio de nombres compatible. En algunos casos, esto es principalmente una cuestión de asignar el SPI a cualquier interfaz nativa que exista para el espacio de nombres. En otros, el proveedor de espacios de nombres debe realizar transacciones con el proveedor de espacios de nombres a través de la red. Algunos proveedores de espacios de nombres realizarán las llamadas a la API de Windows Sockets, mientras que otras utilizarán interfaces privadas para las pilas de transporte asociadas.

 

 



