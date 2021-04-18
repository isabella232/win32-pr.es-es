---
description: Obtiene la información de la categoría de un elemento.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2:: GetItemCategory (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715191"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="817dd-103">IWiaItem2:: GetItemCategory (método)</span><span class="sxs-lookup"><span data-stu-id="817dd-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="817dd-104">Obtiene la información de la categoría de un elemento.</span><span class="sxs-lookup"><span data-stu-id="817dd-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="817dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="817dd-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="817dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="817dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="817dd-107">*pItemCategoryGUID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="817dd-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="817dd-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="817dd-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="817dd-109">Recibe un puntero al GUID que identifica la categoría del elemento.</span><span class="sxs-lookup"><span data-stu-id="817dd-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="817dd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="817dd-110">Return value</span></span>

<span data-ttu-id="817dd-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="817dd-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="817dd-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="817dd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="817dd-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="817dd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="817dd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="817dd-114">Remarks</span></span>

<span data-ttu-id="817dd-115">Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociados a un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0 tiene una categoría específica.</span><span class="sxs-lookup"><span data-stu-id="817dd-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="817dd-116">Este método permite a las aplicaciones identificar la categoría de cualquier elemento en un árbol jerárquico de objetos de elemento en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="817dd-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="817dd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="817dd-117">Requirements</span></span>



| <span data-ttu-id="817dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="817dd-118">Requirement</span></span> | <span data-ttu-id="817dd-119">Value</span><span class="sxs-lookup"><span data-stu-id="817dd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="817dd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="817dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="817dd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="817dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="817dd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="817dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="817dd-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="817dd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="817dd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="817dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="817dd-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="817dd-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="817dd-126">IDL</span><span class="sxs-lookup"><span data-stu-id="817dd-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="817dd-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="817dd-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




