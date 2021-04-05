---
title: Comprobar un derecho de acceso a control en la ACL de un objeto
description: Para comprobar un derecho de acceso de control en la ACL de un objeto, utilice la función AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Comprobando el derecho de acceso de un control en un anuncio de ACL de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077559"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="27b4e-104">Comprobar un derecho de acceso a control en la ACL de un objeto</span><span class="sxs-lookup"><span data-stu-id="27b4e-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="27b4e-105">Para comprobar un derecho de acceso de control en la ACL de un objeto, utilice la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .</span><span class="sxs-lookup"><span data-stu-id="27b4e-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="27b4e-106">Para usar esta función, una aplicación requiere un puntero al [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para el objeto en lugar de una interfaz [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) a un objeto com del descriptor de seguridad de ADSI.</span><span class="sxs-lookup"><span data-stu-id="27b4e-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="27b4e-107">Use los pasos siguientes para comprobar el acceso de un derecho de acceso controlado en un objeto:</span><span class="sxs-lookup"><span data-stu-id="27b4e-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="27b4e-108">Obtiene un puntero de la interfaz [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) al objeto.</span><span class="sxs-lookup"><span data-stu-id="27b4e-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="27b4e-109">Use el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para obtener el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="27b4e-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="27b4e-110">El nombre de la propiedad que contiene el descriptor de seguridad es [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span><span class="sxs-lookup"><span data-stu-id="27b4e-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="27b4e-111">La propiedad se devuelve como un puntero a una estructura de [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="27b4e-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="27b4e-112">Use la estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para comprobar los permisos para el derecho de acceso de control especificado para el cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="27b4e-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="27b4e-113">En el código de ejemplo del [código de ejemplo para comprobar el derecho de acceso a un control en la ACL de un objeto](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) se muestra, en detalle, cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="27b4e-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 