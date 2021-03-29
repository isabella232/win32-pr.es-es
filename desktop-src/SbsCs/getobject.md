---
description: El método GetObject obtiene una instancia de un objeto Microsoft. Windows. ActCtx existente.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809373"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="bbe97-103">ActCtx. GetObject (método)</span><span class="sxs-lookup"><span data-stu-id="bbe97-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="bbe97-104">El método **GetObject** obtiene una instancia de un objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) existente.</span><span class="sxs-lookup"><span data-stu-id="bbe97-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbe97-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="bbe97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbe97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe97-107">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="bbe97-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="bbe97-108">Cadena requerida que indica el objeto.</span><span class="sxs-lookup"><span data-stu-id="bbe97-108">Required string that indicates the object.</span></span> <span data-ttu-id="bbe97-109">El nombre debe estar en el registro en **HKEY \_ local \_ Machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.</span><span class="sxs-lookup"><span data-stu-id="bbe97-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe97-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbe97-110">Return value</span></span>

<span data-ttu-id="bbe97-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bbe97-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe97-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbe97-112">Requirements</span></span>



| <span data-ttu-id="bbe97-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe97-113">Requirement</span></span> | <span data-ttu-id="bbe97-114">Value</span><span class="sxs-lookup"><span data-stu-id="bbe97-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe97-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbe97-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe97-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bbe97-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bbe97-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbe97-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe97-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbe97-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bbe97-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbe97-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe97-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe97-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbe97-121">IID</span><span class="sxs-lookup"><span data-stu-id="bbe97-121">IID</span></span><br/>                      | <span data-ttu-id="bbe97-122">IID \_ IActCtx se define como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="bbe97-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bbe97-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbe97-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe97-124">**CreateObject (método)**</span><span class="sxs-lookup"><span data-stu-id="bbe97-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 




