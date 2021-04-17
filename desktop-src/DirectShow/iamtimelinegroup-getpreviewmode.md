---
description: El método GetPreviewMode recupera el modo de vista previa para el grupo.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'IAMTimelineGroup:: GetPreviewMode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691074"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a><span data-ttu-id="f9c92-103">IAMTimelineGroup:: GetPreviewMode (método)</span><span class="sxs-lookup"><span data-stu-id="f9c92-103">IAMTimelineGroup::GetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="f9c92-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f9c92-104">\[Deprecated.</span></span> <span data-ttu-id="f9c92-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9c92-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f9c92-106">El `GetPreviewMode` método recupera el modo de vista previa para el grupo.</span><span class="sxs-lookup"><span data-stu-id="f9c92-106">The `GetPreviewMode` method retrieves the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c92-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9c92-107">Syntax</span></span>


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a><span data-ttu-id="f9c92-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c92-109">*pfPreview*</span><span class="sxs-lookup"><span data-stu-id="f9c92-109">*pfPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="f9c92-110">Recibe un valor booleano que indica el modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="f9c92-110">Receives a Boolean value indicating the preview mode.</span></span> <span data-ttu-id="f9c92-111">Si es **true**, el grupo está en modo de vista previa.</span><span class="sxs-lookup"><span data-stu-id="f9c92-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="f9c92-112">Si es **false**, el grupo está en modo de creación.</span><span class="sxs-lookup"><span data-stu-id="f9c92-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c92-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9c92-113">Return value</span></span>

<span data-ttu-id="f9c92-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f9c92-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9c92-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9c92-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c92-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9c92-116">Remarks</span></span>

<span data-ttu-id="f9c92-117">En el modo de vista previa, los fotogramas se quitan durante los efectos lentos o las transiciones para mantener el vídeo sincronizado con el audio.</span><span class="sxs-lookup"><span data-stu-id="f9c92-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="f9c92-118">Es posible que el vídeo parezca entrecortado como resultado.</span><span class="sxs-lookup"><span data-stu-id="f9c92-118">The video might look choppy as a result.</span></span> <span data-ttu-id="f9c92-119">En el modo de creación, se representan todos los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="f9c92-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="f9c92-120">El modo de creación es adecuado para escribir archivos; en la vista previa en pantalla, es posible que el vídeo no esté sincronizado con el audio.</span><span class="sxs-lookup"><span data-stu-id="f9c92-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might become out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="f9c92-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f9c92-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9c92-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f9c92-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f9c92-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f9c92-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f9c92-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9c92-124">Requirements</span></span>



| <span data-ttu-id="f9c92-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9c92-125">Requirement</span></span> | <span data-ttu-id="f9c92-126">Value</span><span class="sxs-lookup"><span data-stu-id="f9c92-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c92-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9c92-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f9c92-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c92-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f9c92-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9c92-129">Library</span></span><br/> | <dl> <span data-ttu-id="f9c92-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9c92-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c92-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9c92-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c92-132">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="f9c92-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="f9c92-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f9c92-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




