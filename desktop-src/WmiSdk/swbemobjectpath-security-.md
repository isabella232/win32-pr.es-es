---
description: La propiedad Security del objeto SWbemObjectPath se usa para obtener o establecer los componentes de seguridad de una ruta de acceso de objeto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276123"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="05426-103">Propiedad SWbemObjectPath. Security \_</span><span class="sxs-lookup"><span data-stu-id="05426-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="05426-104">La propiedad **Security** del objeto [**SWbemObjectPath**](swbemobjectpath.md) se usa para obtener o establecer los componentes de seguridad de una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="05426-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="05426-105">Tenga en cuenta que no se utiliza para establecer los atributos de seguridad del propio objeto **SWbemObjectPath** .</span><span class="sxs-lookup"><span data-stu-id="05426-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="05426-106">Solo se usa para representar los componentes de seguridad de la ruta de acceso de un objeto [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="05426-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="05426-107">Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="05426-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="05426-108">Al establecer la propiedad [**\_ Security**](swbemobject-security-.md) de un objeto [**SWbemObjectPath**](swbemobjectset.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento.</span><span class="sxs-lookup"><span data-stu-id="05426-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="05426-109">Para obtener más información, vea [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="05426-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="05426-110">Para obtener más información, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="05426-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="05426-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05426-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05426-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05426-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="05426-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="05426-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="05426-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05426-114">Requirements</span></span>



| <span data-ttu-id="05426-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="05426-115">Requirement</span></span> | <span data-ttu-id="05426-116">Value</span><span class="sxs-lookup"><span data-stu-id="05426-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05426-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05426-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05426-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05426-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05426-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05426-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05426-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05426-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05426-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05426-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="05426-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05426-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="05426-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="05426-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="05426-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="05426-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="05426-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05426-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05426-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05426-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="05426-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="05426-127">CLSID</span></span><br/>                    | <span data-ttu-id="05426-128">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="05426-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="05426-129">IID</span><span class="sxs-lookup"><span data-stu-id="05426-129">IID</span></span><br/>                      | <span data-ttu-id="05426-130">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="05426-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="05426-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="05426-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05426-132">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="05426-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="05426-133">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="05426-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="05426-134">Establecer la \_ seguridad del proceso de la aplicación cliente \_</span><span class="sxs-lookup"><span data-stu-id="05426-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




