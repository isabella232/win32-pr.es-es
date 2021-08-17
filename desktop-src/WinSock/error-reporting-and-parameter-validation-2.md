---
description: El esquema para los informes de errores difiere entre las interfaces SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Informes de errores y validación de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fdec1ee6a4cd7d052ba9f94cdf62ce7de70969a521a7023a5ca41e37f6a931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132627"
---
# <a name="error-reporting-and-parameter-validation"></a>Informes de errores y validación de parámetros

El esquema para los informes de errores difiere entre las interfaces SPI e API. Windows Los proveedores de servicios de sockets informan de errores junto con la devolución de la función, en lugar del enfoque basado en cada subproceso utilizado en la API. El32.dll Ws2 usa el código de error por función del proveedor de servicios para actualizar el valor de error por subproceso que se obtiene a través de la función de \_ API [**WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) Sin embargo, los proveedores de servicios siguen siendo necesarios para mantener el error por socket que se puede recuperar a través de la opción de \_ socket SO ERROR.

El Ws232.dll validación de parámetros solo en llamadas de función que \_ se implementan completamente dentro de sí mismo. Los proveedores de servicios son responsables de realizar todas sus propias validaciones de parámetros.

 

 



