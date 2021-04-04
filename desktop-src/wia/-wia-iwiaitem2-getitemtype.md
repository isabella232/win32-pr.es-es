---
description: Obtiene la información de tipo de un elemento.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2:: GetItemType (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809986"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="c6631-103">IWiaItem2:: GetItemType (método)</span><span class="sxs-lookup"><span data-stu-id="c6631-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="c6631-104">Obtiene la información de tipo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c6631-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6631-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6631-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="c6631-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6631-107">*pItemType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c6631-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6631-108">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="c6631-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="c6631-109">Recibe un puntero a un _ *Long*\* que contiene una combinación de marcas de tipo.</span><span class="sxs-lookup"><span data-stu-id="c6631-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="c6631-110">Vea [**marcas de tipo de elemento de WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c6631-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6631-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6631-111">Return value</span></span>

<span data-ttu-id="c6631-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6631-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c6631-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c6631-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6631-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6631-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6631-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6631-115">Remarks</span></span>

<span data-ttu-id="c6631-116">Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociados a un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0 tiene un tipo de datos específico.</span><span class="sxs-lookup"><span data-stu-id="c6631-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="c6631-117">Los objetos de elemento representan carpetas y archivos.</span><span class="sxs-lookup"><span data-stu-id="c6631-117">Item objects represent folders and files.</span></span> <span data-ttu-id="c6631-118">Las carpetas contienen objetos de archivo.</span><span class="sxs-lookup"><span data-stu-id="c6631-118">Folders contain file objects.</span></span> <span data-ttu-id="c6631-119">Los objetos de archivo contienen datos adquiridos por el dispositivo, como imágenes y sonidos.</span><span class="sxs-lookup"><span data-stu-id="c6631-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="c6631-120">Este método permite a las aplicaciones identificar el tipo de cualquier elemento en un árbol jerárquico de objetos de elemento en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6631-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="c6631-121">Un elemento puede tener más de un tipo.</span><span class="sxs-lookup"><span data-stu-id="c6631-121">An item may have more than one type.</span></span> <span data-ttu-id="c6631-122">Por ejemplo, un elemento que representa un archivo de audio tendrá los atributos de tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span><span class="sxs-lookup"><span data-stu-id="c6631-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6631-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6631-123">Requirements</span></span>



| <span data-ttu-id="c6631-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6631-124">Requirement</span></span> | <span data-ttu-id="c6631-125">Value</span><span class="sxs-lookup"><span data-stu-id="c6631-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6631-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6631-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c6631-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6631-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c6631-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6631-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c6631-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6631-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c6631-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6631-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6631-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6631-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6631-132">IDL</span><span class="sxs-lookup"><span data-stu-id="c6631-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6631-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6631-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




