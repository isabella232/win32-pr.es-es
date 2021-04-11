---
description: La \_ propiedad Security del objeto SWbemObject se usa para leer o establecer la configuración de seguridad para un objeto SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361443"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="b49fa-103">Propiedad SWbemObject. Security \_</span><span class="sxs-lookup"><span data-stu-id="b49fa-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="b49fa-104">La **propiedad \_ Security** del objeto [**SWbemObject**](swbemobject.md) se usa para leer o establecer la configuración de seguridad para un objeto **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="b49fa-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="b49fa-105">Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="b49fa-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="b49fa-106">La configuración de seguridad de este objeto no indica la configuración de autenticación, suplantación o privilegio realizada en una conexión a Instrumental de administración de Windows (WMI) o la seguridad activa para el proxy cuando un objeto se entrega a un receptor en una llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b49fa-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="b49fa-107">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="b49fa-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="b49fa-108">Al establecer la propiedad **\_ Security** de un objeto [**SWbemObject**](swbemobject.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento.</span><span class="sxs-lookup"><span data-stu-id="b49fa-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="b49fa-109">Para obtener más información, vea [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="b49fa-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="b49fa-110">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b49fa-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b49fa-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b49fa-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49fa-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b49fa-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="b49fa-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b49fa-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="b49fa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b49fa-114">Requirements</span></span>



| <span data-ttu-id="b49fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b49fa-115">Requirement</span></span> | <span data-ttu-id="b49fa-116">Value</span><span class="sxs-lookup"><span data-stu-id="b49fa-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b49fa-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b49fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b49fa-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b49fa-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b49fa-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b49fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b49fa-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b49fa-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b49fa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b49fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49fa-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b49fa-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b49fa-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b49fa-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b49fa-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b49fa-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b49fa-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b49fa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b49fa-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b49fa-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b49fa-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="b49fa-127">CLSID</span></span><br/>                    | <span data-ttu-id="b49fa-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="b49fa-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b49fa-129">IID</span><span class="sxs-lookup"><span data-stu-id="b49fa-129">IID</span></span><br/>                      | <span data-ttu-id="b49fa-130">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="b49fa-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b49fa-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b49fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49fa-132">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b49fa-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b49fa-133">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="b49fa-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="b49fa-134">Establecer la \_ seguridad del proceso de la aplicación cliente \_</span><span class="sxs-lookup"><span data-stu-id="b49fa-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="b49fa-135">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="b49fa-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="b49fa-136">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="b49fa-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="b49fa-137">**WbemImpersonationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="b49fa-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="b49fa-138">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="b49fa-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="b49fa-139">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="b49fa-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




