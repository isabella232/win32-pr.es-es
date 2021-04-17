---
description: El método SetOutputBuffering especifica el número de fotogramas representados de antemano durante la vista previa.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'IAMTimelineGroup:: SetOutputBuffering (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690791"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="747eb-103">IAMTimelineGroup:: SetOutputBuffering (método)</span><span class="sxs-lookup"><span data-stu-id="747eb-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="747eb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="747eb-104">\[Deprecated.</span></span> <span data-ttu-id="747eb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="747eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="747eb-106">El `SetOutputBuffering` método especifica el número de fotogramas representados de antemano durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="747eb-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="747eb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="747eb-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="747eb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="747eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747eb-109">*nBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="747eb-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747eb-110">Número de fotogramas que se almacenarán en búfer durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="747eb-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="747eb-111">Debe ser dos o más.</span><span class="sxs-lookup"><span data-stu-id="747eb-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747eb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="747eb-112">Return value</span></span>

<span data-ttu-id="747eb-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="747eb-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="747eb-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="747eb-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="747eb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="747eb-115">Remarks</span></span>

<span data-ttu-id="747eb-116">Un búfer mayor requiere más memoria, pero puede dar lugar a una vista previa más suave, especialmente durante los efectos o las transiciones que requieren más tiempo para representarse.</span><span class="sxs-lookup"><span data-stu-id="747eb-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="747eb-117">El búfer predeterminado es 30 fotogramas.</span><span class="sxs-lookup"><span data-stu-id="747eb-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="747eb-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="747eb-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="747eb-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="747eb-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="747eb-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="747eb-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="747eb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="747eb-121">Requirements</span></span>



| <span data-ttu-id="747eb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="747eb-122">Requirement</span></span> | <span data-ttu-id="747eb-123">Value</span><span class="sxs-lookup"><span data-stu-id="747eb-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="747eb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="747eb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="747eb-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="747eb-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="747eb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="747eb-126">Library</span></span><br/> | <dl> <span data-ttu-id="747eb-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="747eb-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747eb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="747eb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747eb-129">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="747eb-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="747eb-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="747eb-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




