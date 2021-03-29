---
description: El método CreateObject del objeto Microsoft. Windows. ActCtx crea un objeto en el contexto del manifiesto actual.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. CreateObject (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277351"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="f6af3-103">ActCtx. CreateObject (método)</span><span class="sxs-lookup"><span data-stu-id="f6af3-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="f6af3-104">El método **CreateObject** del objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) crea un objeto en el contexto del manifiesto actual.</span><span class="sxs-lookup"><span data-stu-id="f6af3-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6af3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6af3-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="f6af3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6af3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6af3-107">*objectId*</span><span class="sxs-lookup"><span data-stu-id="f6af3-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="f6af3-108">Cadena que especifica el tipo de objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="f6af3-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="f6af3-109">Por ejemplo, un ProgID de COM.</span><span class="sxs-lookup"><span data-stu-id="f6af3-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6af3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6af3-110">Return value</span></span>

<span data-ttu-id="f6af3-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f6af3-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6af3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6af3-112">Requirements</span></span>



| <span data-ttu-id="f6af3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6af3-113">Requirement</span></span> | <span data-ttu-id="f6af3-114">Value</span><span class="sxs-lookup"><span data-stu-id="f6af3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6af3-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6af3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f6af3-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6af3-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f6af3-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6af3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f6af3-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6af3-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6af3-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6af3-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6af3-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6af3-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6af3-121">IID</span><span class="sxs-lookup"><span data-stu-id="f6af3-121">IID</span></span><br/>                      | <span data-ttu-id="f6af3-122">IID \_ IActCtx se define como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="f6af3-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f6af3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6af3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6af3-124">**GetObject (Método)**</span><span class="sxs-lookup"><span data-stu-id="f6af3-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 




