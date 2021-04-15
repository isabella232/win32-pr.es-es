---
title: Autenticación (AD DS)
description: Cada objeto de Active Directory Domain Services tiene un descriptor de seguridad único que define los permisos de acceso necesarios para leer o actualizar el objeto o sus propiedades individuales.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, enlace, autenticación
- autenticación de enlace AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487511"
---
# <a name="authentication-ad-ds"></a>Autenticación (AD DS)

Cada objeto de Active Directory Domain Services tiene un descriptor de seguridad único que define los permisos de acceso necesarios para leer o actualizar el objeto o sus propiedades individuales. Los privilegios de acceso se determinan mediante los derechos concedidos a la cuenta o pertenencia a grupos de un usuario.

Cuando una aplicación se enlaza a un objeto en el directorio, los privilegios de acceso que la aplicación tiene a ese objeto se basan en el contexto de usuario especificado durante la operación de enlace. En el caso de las funciones de enlace y los métodos [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), una aplicación puede usar implícitamente las credenciales del autor de la llamada, especificar explícitamente las credenciales de una cuenta de usuario o usar un contexto de usuario no autenticado (invitado).

 

 