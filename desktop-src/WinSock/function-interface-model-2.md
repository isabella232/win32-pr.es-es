---
description: Windows Transporte de sockets y espacio de nombres&8211; los proveedores de servicios son archivos DLL con un único punto de entrada de procedimiento exportado para la función de inicialización del proveedor de servicios \# WSPStartup o NSPStartup, respectivamente.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modelo de interfaz de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 224c3735d6230bfa8a307918de8ac7ce6a2acb3d7a0d671fee37fc6f62dcd310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132418"
---
# <a name="function-interface-model"></a>Modelo de interfaz de función

Windows Los proveedores de servicios de espacio de nombres y transporte de sockets son archivos DLL con un único punto de entrada de procedimiento exportado para la función de inicialización del proveedor de servicios [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) o [**NSPStartup,**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)respectivamente. Todas las demás funciones del proveedor de servicios se hacen accesibles a la32.dll Ws2 a través de la tabla de distribución \_ del proveedor de servicios. Los archivos DLL del proveedor de servicios se cargan en la memoria mediante el32.dll Ws2 solo cuando es necesario y se descargan cuando sus servicios \_ ya no son necesarios.

El SPI también define varias circunstancias en las que un proveedor de servicios de transporte llama a Ws232.dll (llamadas arriba) para obtener servicios de soporte técnico \_ de DLL. El archivo DLL del proveedor de servicios de transporte se proporciona a la tabla de distribución de llamada32.dll Ws2 a través del parámetro \_ *UpcallTable* a [**WSPStartup.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)

Los proveedores de servicios deben cambiar su extensión de nombre de archivo de "DLL" a ". WSP" o ". NSP". Este requisito no es estricto. Un proveedor de servicios seguirá funcionando con la32.dll Ws2 \_ con cualquier extensión de nombre de archivo.

El SPI de Winsock usa la siguiente convención de nomenclatura de prefijo de función:

| Prefijo | Significado                          | Descripción                                       |
|--------|----------------------------------|---------------------------------------------------|
| Wsp    | Windows Proveedor de servicios sockets | Puntos de entrada del proveedor de servicios de transporte           |
| WPU    | Windows Llamada upcall del proveedor de sockets  | Puntos de entrada32.dll Ws2 \_ para proveedores de servicios    |
| Wsc    | Windows Configuración de sockets    | Puntos de entrada32.dll WS2 \_ para applets de instalación |
| Nsp    | Proveedor de espacios de nombres               | Puntos de entrada del proveedor de espacios de nombres                   |



 

Como se ha descrito anteriormente, estos puntos de entrada no se exportan (a excepción de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) y [**NSPStartup),**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)sino que se accede a ellos a través de un intercambio de tablas de distribución.

 

 



