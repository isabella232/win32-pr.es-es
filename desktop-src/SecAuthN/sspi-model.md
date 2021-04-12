---
description: La interfaz del proveedor de compatibilidad para seguridad (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o una red sin cambiar la interfaz al sistema de seguridad.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modelo SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423620"
---
# <a name="sspi-model"></a>Modelo SSPI

La [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) permite que una aplicación use varios modelos de seguridad disponibles en un equipo o una red sin cambiar la interfaz al sistema de seguridad. SSPI no establece [*las credenciales*](../secgloss/c-gly.md) de inicio de sesión porque normalmente es una operación privilegiada administrada por el sistema operativo.

Un [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) se incluye en una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (dll) que implementa SSPI al hacer que uno o varios [*paquetes de seguridad*](../secgloss/s-gly.md) estén disponibles para las aplicaciones. Cada paquete de seguridad proporciona asignaciones entre las llamadas a funciones SSPI de una aplicación y las funciones de un modelo de seguridad real. Los paquetes de seguridad admiten [*protocolos de seguridad*](../secgloss/s-gly.md) , como la autenticación [*Kerberos*](../secgloss/k-gly.md) y LAN Manager.

La interfaz SSPI está disponible en modo kernel y en modo de usuario. Para usar la funcionalidad SSPI en modo kernel, debe instalar el DDK del sistema de archivos instalables de Windows. El modelo de llamada sigue siendo el mismo, pero las consideraciones sobre el modo kernel se indican en las páginas de referencia de la función. Para obtener más información, vea [funciones de SSPI](authentication-functions.md).

 

 
