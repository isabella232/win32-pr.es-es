---
description: La propiedad Keys del objeto SWbemObjectPath es un objeto SWbemNamedValueSet que contiene los enlaces de valor de clave. Esta propiedad es de solo lectura.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Keys (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082391"
---
# <a name="swbemobjectpathkeys-property"></a><span data-ttu-id="37ce9-104">SWbemObjectPath. Keys (propiedad)</span><span class="sxs-lookup"><span data-stu-id="37ce9-104">SWbemObjectPath.Keys property</span></span>

<span data-ttu-id="37ce9-105">La propiedad **Keys** del objeto [**SWbemObjectPath**](swbemobjectpath.md) es un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contiene los enlaces de valor de clave.</span><span class="sxs-lookup"><span data-stu-id="37ce9-105">The **Keys** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span> <span data-ttu-id="37ce9-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="37ce9-106">This property is read-only.</span></span>

<span data-ttu-id="37ce9-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="37ce9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="37ce9-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="37ce9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ce9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37ce9-109">Syntax</span></span>


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a><span data-ttu-id="37ce9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="37ce9-110">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="37ce9-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="37ce9-111">Error codes</span></span>

<span data-ttu-id="37ce9-112">Después de recuperar la propiedad **Keys** , el objeto **Err** puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="37ce9-112">After you retrieve the **Keys** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="37ce9-113">**wbemErrNotSupported** -2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="37ce9-113">**wbemErrNotSupported** - 2147749900 (0x8004100C)</span></span>
</dt> <dd>

<span data-ttu-id="37ce9-114">No se admite esta característica u operación.</span><span class="sxs-lookup"><span data-stu-id="37ce9-114">The feature or operation is not supported.</span></span> <span data-ttu-id="37ce9-115">Se devuelve este error si un script intenta escribir en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="37ce9-115">This error is returned if a script attempts to write to this property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37ce9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37ce9-116">Requirements</span></span>



| <span data-ttu-id="37ce9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37ce9-117">Requirement</span></span> | <span data-ttu-id="37ce9-118">Value</span><span class="sxs-lookup"><span data-stu-id="37ce9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ce9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37ce9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37ce9-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37ce9-120">Windows Vista</span></span><br/>                                                                                   |
| <span data-ttu-id="37ce9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37ce9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37ce9-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37ce9-122">Windows Server 2008</span></span><br/>                                                                             |
| <span data-ttu-id="37ce9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37ce9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37ce9-124"><dt>Adoctint. h (incluye Wbemdisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37ce9-124"><dt>Adoctint.h (include Wbemdisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="37ce9-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="37ce9-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="37ce9-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="37ce9-126"><dt>Wbemdisp.tlb</dt></span></span> </dl>                    |
| <span data-ttu-id="37ce9-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37ce9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ce9-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ce9-128"><dt>Wbemdisp.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="37ce9-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="37ce9-129">CLSID</span></span><br/>                    | <span data-ttu-id="37ce9-130">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="37ce9-130">CLSID\_SWbemObjectPath</span></span><br/>                                                                          |
| <span data-ttu-id="37ce9-131">IID</span><span class="sxs-lookup"><span data-stu-id="37ce9-131">IID</span></span><br/>                      | <span data-ttu-id="37ce9-132">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="37ce9-132">IID\_ISWbemObjectPath</span></span><br/>                                                                           |



 

 




