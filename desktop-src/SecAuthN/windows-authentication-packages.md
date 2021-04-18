---
description: Los paquetes de autenticación de Windows proporcionan servicios de autenticación implementando la funcionalidad específica del paquete para las funciones LsaLogonUser y LsaCallAuthenticationPackage proporcionadas por la LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Paquetes de autenticación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541150"
---
# <a name="windows-authentication-packages"></a>Paquetes de autenticación de Windows

Los paquetes de autenticación de Windows proporcionan servicios de autenticación implementando la funcionalidad específica del paquete para las funciones [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) y [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) proporcionadas por la LSA.

MSV1 \_ 0 es un ejemplo de un [*paquete de autenticación*](../secgloss/a-gly.md)de Windows. El \_ paquete MSV1 0 acepta un nombre de usuario y una contraseña con [*hash*](../secgloss/h-gly.md) , que busca en la base de datos del administrador de [*cuentas de seguridad*](../secgloss/s-gly.md) (SAM). En función de los resultados de la búsqueda, el \_ paquete de autenticación MSV1 0 acepta o rechaza el intento de autenticación.

Para obtener una lista de las funciones de soporte que LSA proporciona para que las usen los paquetes de autenticación de Windows que requieren servicios del sistema, consulte [funciones de LSA llamadas por paquetes de autenticación](authentication-functions.md).

Los paquetes de autenticación de Windows deben implementar un conjunto de funciones a las que llama la LSA. Para obtener la lista completa de funciones, consulte [funciones implementadas por paquetes de autenticación](authentication-functions.md).

 

 
