---
description: Security Support Provider Interface (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o red sin cambiar la interfaz al sistema de seguridad.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modelo SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160971"
---
# <a name="sspi-model"></a>Modelo SSPI

[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o red sin cambiar la interfaz al sistema de seguridad. SSPI no establece credenciales de [*inicio de sesión*](../secgloss/c-gly.md) porque suele ser una operación con privilegios que controla el sistema operativo.

Un [*proveedor de compatibilidad de*](../secgloss/s-gly.md) seguridad (SSP) se encuentra en una biblioteca de vínculos dinámicos (DLL) que implementa SSPI al poner uno o varios paquetes de seguridad a disposición de las aplicaciones. [](../secgloss/d-gly.md) [](../secgloss/s-gly.md) Cada paquete de seguridad proporciona asignaciones entre las llamadas de función SSPI de una aplicación y las funciones de un modelo de seguridad real. Los paquetes de seguridad [*admiten protocolos de seguridad,*](../secgloss/s-gly.md) como la [*autenticación Kerberos*](../secgloss/k-gly.md) y el administrador de LAN.

La interfaz SSPI está disponible en modo kernel, así como en modo de usuario. Para usar la funcionalidad SSPI en modo kernel, debe instalar el DDK Windows sistema de archivos instalable. El modelo de llamada sigue siendo el mismo, pero las consideraciones sobre el modo kernel se anotan en las páginas de referencia de función. Para obtener más información, vea [Funciones de SSPI.](authentication-functions.md)

 

 
