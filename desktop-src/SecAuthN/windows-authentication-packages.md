---
description: Windows paquetes de autenticación proporcionan servicios de autenticación mediante la implementación de la funcionalidad específica del paquete para las funciones LsaLogonUser y LsaCallAuthenticationPackage proporcionadas por LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Paquetes de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915084"
---
# <a name="windows-authentication-packages"></a>Windows Paquetes de autenticación

Windows paquetes de autenticación proporcionan servicios de autenticación mediante la implementación de la funcionalidad específica del paquete para las funciones [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) y [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) proporcionadas por LSA.

MSV1 \_ 0 es un ejemplo de un Windows [*de autenticación .*](../secgloss/a-gly.md) El paquete MSV1 0 acepta un nombre de usuario y una contraseña con hash, que busca en la base de datos del Administrador de cuentas de seguridad \_ (SAM). [](../secgloss/h-gly.md) [](../secgloss/s-gly.md) En función de los resultados de la búsqueda, el paquete de autenticación MSV1 0 acepta o \_ rechaza el intento de autenticación.

Para obtener una lista de las funciones de soporte técnico que el LSA proporciona para su uso por parte de los paquetes de autenticación de Windows que requieren servicios del sistema, vea Funciones de [LSA](authentication-functions.md)llamadas por paquetes de autenticación .

Windows paquetes de autenticación deben implementar un conjunto de funciones a las que llama el LSA. Para obtener la lista completa de funciones, vea [Funciones implementadas por paquetes de autenticación](authentication-functions.md).

 

 
