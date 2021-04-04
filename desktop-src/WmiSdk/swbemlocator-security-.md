---
description: La \_ propiedad Security del objeto SWbemLocator se usa para leer o establecer la configuración de seguridad de un objeto SWbemLocator. Esta propiedad es un objeto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Propiedad SWbemLocator.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812421"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="69d7e-104">Propiedad SWbemLocator. Security \_</span><span class="sxs-lookup"><span data-stu-id="69d7e-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="69d7e-105">La **propiedad \_ Security** del objeto [**SWbemLocator**](swbemlocator.md) se usa para leer o establecer la configuración de seguridad de un objeto **SWbemLocator** .</span><span class="sxs-lookup"><span data-stu-id="69d7e-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="69d7e-106">Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="69d7e-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="69d7e-107">Al establecer la propiedad **\_ Security** de un objeto [**SWbemLocator**](swbemlocator.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento.</span><span class="sxs-lookup"><span data-stu-id="69d7e-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="69d7e-108">Para obtener más información, vea [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="69d7e-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="69d7e-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="69d7e-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="69d7e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69d7e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d7e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69d7e-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="69d7e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="69d7e-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="69d7e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69d7e-113">Remarks</span></span>

<span data-ttu-id="69d7e-114">Las propiedades de un objeto **SWbemLocator. \_ Security** no tienen valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="69d7e-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="69d7e-115">Si intenta obtener el valor de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) o [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) en un objeto [**SWbemLocator**](swbemlocator.md) antes de establecerlo, se produce un error [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .</span><span class="sxs-lookup"><span data-stu-id="69d7e-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d7e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d7e-116">Requirements</span></span>



| <span data-ttu-id="69d7e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d7e-117">Requirement</span></span> | <span data-ttu-id="69d7e-118">Value</span><span class="sxs-lookup"><span data-stu-id="69d7e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69d7e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69d7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69d7e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69d7e-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69d7e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69d7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69d7e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69d7e-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69d7e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69d7e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d7e-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d7e-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="69d7e-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="69d7e-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="69d7e-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="69d7e-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="69d7e-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69d7e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69d7e-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69d7e-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="69d7e-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="69d7e-129">CLSID</span></span><br/>                    | <span data-ttu-id="69d7e-130">CLSID \_ SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="69d7e-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="69d7e-131">IID</span><span class="sxs-lookup"><span data-stu-id="69d7e-131">IID</span></span><br/>                      | <span data-ttu-id="69d7e-132">\_ISWBEMLOCATOR IID</span><span class="sxs-lookup"><span data-stu-id="69d7e-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="69d7e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="69d7e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d7e-134">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="69d7e-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="69d7e-135">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="69d7e-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="69d7e-136">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="69d7e-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="69d7e-137">Establecer la \_ seguridad del proceso de la aplicación cliente \_</span><span class="sxs-lookup"><span data-stu-id="69d7e-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="69d7e-138">**Objeto SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="69d7e-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="69d7e-139">Protección de una conexión WMI remota</span><span class="sxs-lookup"><span data-stu-id="69d7e-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




