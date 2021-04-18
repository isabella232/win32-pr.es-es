---
description: El esquema de informes de errores difiere entre las interfaces SPI y API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Informes de errores y validación de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705630"
---
# <a name="error-reporting-and-parameter-validation"></a>Informes de errores y validación de parámetros

El esquema de informes de errores difiere entre las interfaces SPI y API. Los proveedores de servicios de Windows Sockets notifican errores junto con la función que devuelve, en lugar del enfoque basado en subprocesos utilizado en la API. El \_32.dll Ws2 utiliza el código de error por función del proveedor de servicios para actualizar el valor de error por subproceso que se obtiene a través de la función de la API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Los proveedores de servicios siguen siendo necesarios, sin embargo, para mantener el error basado en sockets, que se puede recuperar mediante la \_ opción de socket de error.

El \_32.dll Ws2 realiza la validación de parámetros solo en las llamadas de función que se implementan completamente dentro de sí mismo. Los proveedores de servicios son responsables de realizar su propia validación de parámetros.

 

 



