---
description: Windows paquetes de autenticación proporcionan servicios de autenticación mediante la implementación de la funcionalidad específica del paquete para las funciones LsaLogonUser y LsaCallAuthenticationPackage proporcionadas por LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Paquetes de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160887"
---
# <a name="windows-authentication-packages"></a>Windows Paquetes de autenticación

Windows paquetes de autenticación proporcionan servicios de autenticación mediante la implementación de la funcionalidad específica del paquete para las funciones [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) y [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) proporcionadas por LSA.

MSV1 \_ 0 es un ejemplo de un Windows [*de autenticación .*](../secgloss/a-gly.md) El paquete MSV1 0 acepta un nombre de usuario y una contraseña con hash, que busca en la base de datos del Administrador de cuentas de seguridad \_ (SAM). [](../secgloss/h-gly.md) [](../secgloss/s-gly.md) En función de los resultados de la búsqueda, el paquete de autenticación MSV1 0 acepta o \_ rechaza el intento de autenticación.

Para obtener una lista de las funciones de soporte técnico que el LSA proporciona para su uso por parte de los paquetes de autenticación de Windows que requieren servicios del sistema, vea Funciones de [LSA](authentication-functions.md)llamadas por paquetes de autenticación .

Windows paquetes de autenticación deben implementar un conjunto de funciones a las que llama el LSA. Para obtener la lista completa de funciones, vea [Funciones implementadas por paquetes de autenticación](authentication-functions.md).

 

 
