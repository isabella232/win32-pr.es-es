---
description: Obtiene el componente de vista previa de la adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2:: GetPreviewComponent (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154398"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a><span data-ttu-id="2f717-103">IWiaItem2:: GetPreviewComponent (método)</span><span class="sxs-lookup"><span data-stu-id="2f717-103">IWiaItem2::GetPreviewComponent method</span></span>

<span data-ttu-id="2f717-104">Obtiene el componente de vista previa de la adquisición de imágenes de Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f717-104">Gets the Windows Image Acquisition (WIA) 2.0 preview component.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f717-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f717-105">Syntax</span></span>


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a><span data-ttu-id="2f717-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f717-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f717-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f717-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="2f717-108">Type: **LONG**</span></span>

<span data-ttu-id="2f717-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2f717-109">Not used.</span></span> <span data-ttu-id="2f717-110">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="2f717-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2f717-111">*ppWiaPreview* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f717-111">*ppWiaPreview* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f717-112">Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f717-112">Type: **[**IWiaPreview**](-wia-iwiapreview.md)\*\***</span></span>

<span data-ttu-id="2f717-113">Devuelve la dirección de un puntero a la interfaz [**IWiaPreview**](-wia-iwiapreview.md) del componente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2f717-113">Returns the address of a pointer to the [**IWiaPreview**](-wia-iwiapreview.md) interface of the preview component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f717-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f717-114">Return value</span></span>

<span data-ttu-id="2f717-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f717-115">Type: **HRESULT**</span></span>

<span data-ttu-id="2f717-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2f717-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f717-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f717-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f717-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f717-118">Remarks</span></span>

<span data-ttu-id="2f717-119">Use esta función para devolver un puntero a la dirección del componente de vista previa de WIA 2,0 para cualquier objeto [**IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f717-119">Use this function to return a pointer to the address of the WIA 2.0 preview component for any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device.</span></span>

<span data-ttu-id="2f717-120">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppWiaPreview* .</span><span class="sxs-lookup"><span data-stu-id="2f717-120">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppWiaPreview* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f717-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f717-121">Requirements</span></span>



| <span data-ttu-id="2f717-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f717-122">Requirement</span></span> | <span data-ttu-id="2f717-123">Value</span><span class="sxs-lookup"><span data-stu-id="2f717-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f717-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f717-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2f717-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2f717-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f717-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f717-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2f717-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f717-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f717-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f717-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f717-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f717-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f717-130">IDL</span><span class="sxs-lookup"><span data-stu-id="2f717-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f717-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f717-131"><dt>Wia.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f717-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f717-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f717-133">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="2f717-133">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="2f717-134">**IWiaPreview**</span><span class="sxs-lookup"><span data-stu-id="2f717-134">**IWiaPreview**</span></span>](-wia-iwiapreview.md)
</dt> </dl>

 

 
