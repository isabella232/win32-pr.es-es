---
description: Security Support Provider Interface (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o red sin cambiar la interfaz al sistema de seguridad.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modelo SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5d915a8937f57105e2478b41955cc5789fba25791e7f118a84dc4fa38e12fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916822"
---
# <a name="sspi-model"></a>Modelo SSPI

[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o red sin cambiar la interfaz al sistema de seguridad. SSPI no establece credenciales de [*inicio de sesión*](../secgloss/c-gly.md) porque suele ser una operación con privilegios que controla el sistema operativo.

Un [*proveedor de soporte técnico*](../secgloss/s-gly.md) de seguridad (SSP) se encuentra en una biblioteca de [](../secgloss/s-gly.md) vínculos dinámicos [*(DLL)*](../secgloss/d-gly.md) que implementa SSPI haciendo que uno o varios paquetes de seguridad estén disponibles para las aplicaciones. Cada paquete de seguridad proporciona asignaciones entre las llamadas de función SSPI de una aplicación y las funciones de un modelo de seguridad real. Los paquetes de seguridad [*admiten protocolos de seguridad,*](../secgloss/s-gly.md) como la [*autenticación Kerberos*](../secgloss/k-gly.md) y el administrador de LAN.

La interfaz SSPI está disponible en modo kernel, así como en modo de usuario. Para usar la funcionalidad SSPI en modo kernel, debe instalar Windows DDK del sistema de archivos instalable. El modelo de llamada sigue siendo el mismo, pero las consideraciones sobre el modo kernel se anotan en las páginas de referencia de función. Para obtener más información, vea [Funciones de SSPI.](authentication-functions.md)

 

 
