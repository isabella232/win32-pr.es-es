---
description: El método GetStretchMode recupera el modo Stretch. El modo Stretch determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'IAMTimelineSrc:: GetStretchMode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681076"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="7fbbd-104">IAMTimelineSrc:: GetStretchMode (método)</span><span class="sxs-lookup"><span data-stu-id="7fbbd-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="7fbbd-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-105">\[Deprecated.</span></span> <span data-ttu-id="7fbbd-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fbbd-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7fbbd-107">El `GetStretchMode` método recupera el modo de Stretch.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="7fbbd-108">El modo Stretch determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbbd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fbbd-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="7fbbd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fbbd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbbd-111">*pnStretchMode*</span><span class="sxs-lookup"><span data-stu-id="7fbbd-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbbd-112">Recibe una marca que indica el modo de ajuste actual.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="7fbbd-113">Para obtener una lista de los valores posibles, vea [**cambiar el tamaño**](resize-flags.md)de las marcas.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbbd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fbbd-114">Return value</span></span>

<span data-ttu-id="7fbbd-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7fbbd-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fbbd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fbbd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fbbd-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7fbbd-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7fbbd-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fbbd-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7fbbd-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7fbbd-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7fbbd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbbd-121">Requirements</span></span>



| <span data-ttu-id="7fbbd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbbd-122">Requirement</span></span> | <span data-ttu-id="7fbbd-123">Value</span><span class="sxs-lookup"><span data-stu-id="7fbbd-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbbd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fbbd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7fbbd-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbd-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7fbbd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fbbd-126">Library</span></span><br/> | <dl> <span data-ttu-id="7fbbd-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fbbd-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbbd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fbbd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbbd-129">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="7fbbd-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="7fbbd-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="7fbbd-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




