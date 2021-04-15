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
# <a name="authentication-ad-ds"></a><span data-ttu-id="919ed-105">Autenticación (AD DS)</span><span class="sxs-lookup"><span data-stu-id="919ed-105">Authentication (AD DS)</span></span>

<span data-ttu-id="919ed-106">Cada objeto de Active Directory Domain Services tiene un descriptor de seguridad único que define los permisos de acceso necesarios para leer o actualizar el objeto o sus propiedades individuales.</span><span class="sxs-lookup"><span data-stu-id="919ed-106">Every object in Active Directory Domain Services has a unique security descriptor that defines the access permissions that are required to read or update the object or its individual properties.</span></span> <span data-ttu-id="919ed-107">Los privilegios de acceso se determinan mediante los derechos concedidos a la cuenta o pertenencia a grupos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="919ed-107">Access privileges are determined by the rights granted to a user's account or group memberships.</span></span>

<span data-ttu-id="919ed-108">Cuando una aplicación se enlaza a un objeto en el directorio, los privilegios de acceso que la aplicación tiene a ese objeto se basan en el contexto de usuario especificado durante la operación de enlace.</span><span class="sxs-lookup"><span data-stu-id="919ed-108">When an application binds to an object in the directory, the access privileges that the application has to that object are based on the user context specified during the bind operation.</span></span> <span data-ttu-id="919ed-109">En el caso de las funciones de enlace y los métodos [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), una aplicación puede usar implícitamente las credenciales del autor de la llamada, especificar explícitamente las credenciales de una cuenta de usuario o usar un contexto de usuario no autenticado (invitado).</span><span class="sxs-lookup"><span data-stu-id="919ed-109">For the binding functions and methods [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), an application can implicitly use the credentials of the caller, explicitly specify the credentials of a user account, or use an unauthenticated user context (Guest).</span></span>

 

 