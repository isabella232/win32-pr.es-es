---
description: Windows Sockets Transport y namespace&\# 8211; los proveedores de servicios son dll con un único punto de entrada de procedimiento exportado para la función de inicialización de proveedor de servicios WSPStartup o NSPStartup, respectivamente.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modelo de interfaz de función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705618"
---
# <a name="function-interface-model"></a>Modelo de interfaz de función

Espacio de nombres y transporte de Windows Sockets: los proveedores de servicios son archivos DLL con un único punto de entrada de procedimiento exportado para la función de inicialización de proveedor de servicio [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) o [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectivamente. Todas las demás funciones del proveedor de servicios son accesibles para el \_32.dll Ws2 a través de la tabla de envío del proveedor de servicios. Los archivos DLL del proveedor de servicios se cargan en la memoria mediante el \_32.dll Ws2 solo cuando sea necesario y se descargan cuando sus servicios ya no son necesarios.

El SPI también define varias circunstancias en las que un proveedor de servicios de transporte llama a Ws2 \_32.dll (llamadas) para obtener los servicios de soporte de dll. La DLL del proveedor de servicios de transporte recibe la \_ tabla de envío de llamadas de Ws232.dll a través del parámetro *UpcallTable* a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).

Los proveedores de servicios deben cambiar su extensión de nombre de archivo de "DLL" a ". WSP "o". NSP ". Este requisito no es estricto. Un proveedor de servicios seguirá funcionando con el \_32.dll Ws2 con cualquier extensión de nombre de archivo.

El SPI de Winsock usa la siguiente Convención de nomenclatura de prefijos de función:

| Prefijo | Significado                          | Descripción                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Proveedor de servicios de Windows Sockets | Puntos de entrada del proveedor de servicios de transporte           |
| WPU    | Llamada al proveedor de Windows Sockets  | Ws2 \_32.dll puntos de entrada para proveedores de servicios    |
| WSC    | Configuración de Windows Sockets    | WS2 \_32.dll puntos de entrada para applets de instalación |
| NSP    | Proveedor de espacios de nombres               | Puntos de entrada del proveedor de espacios de nombres                   |



 

Tal y como se ha descrito anteriormente, estos puntos de entrada no se exportan (con la excepción de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) y [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), pero se obtiene acceso a ellos a través de un intercambio de tablas de distribución.

 

 



