---
description: El método SetAsClass del objeto SWbemObjectPath obliga a la ruta de acceso a una clase WMI.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. SetAsClass (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715729"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="ee7b8-103">Propiedad SWbemObjectPath. SetAsClass</span><span class="sxs-lookup"><span data-stu-id="ee7b8-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="ee7b8-104">El método **SetAsClass** del objeto [**SWbemObjectPath**](swbemobjectpath.md) obliga a la ruta de acceso a una clase WMI.</span><span class="sxs-lookup"><span data-stu-id="ee7b8-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="ee7b8-105">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="ee7b8-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7b8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee7b8-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="ee7b8-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ee7b8-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee7b8-108">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ee7b8-108">Error codes</span></span>

<span data-ttu-id="ee7b8-109">Después de obtener o establecer la propiedad **SetAsClass** , el objeto **Err** puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="ee7b8-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="ee7b8-110">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ee7b8-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ee7b8-111">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ee7b8-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee7b8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee7b8-112">Requirements</span></span>



| <span data-ttu-id="ee7b8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee7b8-113">Requirement</span></span> | <span data-ttu-id="ee7b8-114">Value</span><span class="sxs-lookup"><span data-stu-id="ee7b8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7b8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee7b8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7b8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee7b8-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee7b8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee7b8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7b8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee7b8-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee7b8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee7b8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee7b8-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b8-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee7b8-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ee7b8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee7b8-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b8-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ee7b8-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee7b8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee7b8-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b8-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ee7b8-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="ee7b8-125">CLSID</span></span><br/>                    | <span data-ttu-id="ee7b8-126">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="ee7b8-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="ee7b8-127">IID</span><span class="sxs-lookup"><span data-stu-id="ee7b8-127">IID</span></span><br/>                      | <span data-ttu-id="ee7b8-128">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="ee7b8-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




