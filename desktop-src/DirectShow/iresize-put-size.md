---
description: El \_ método put size establece el tamaño de salida y el modo de ajuste.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize: método de ut_Size de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679439"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="4b9cc-103">IResize: método de tamaño de:p UT \_</span><span class="sxs-lookup"><span data-stu-id="4b9cc-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="4b9cc-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-104">\[Deprecated.</span></span> <span data-ttu-id="4b9cc-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b9cc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4b9cc-106">El `put_Size` método establece el tamaño de salida y el modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b9cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b9cc-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="4b9cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b9cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b9cc-109">*Alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4b9cc-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9cc-110">Alto del vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4b9cc-111">*Ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4b9cc-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9cc-112">Ancho del vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4b9cc-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4b9cc-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b9cc-114">Modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-114">The stretch mode.</span></span> <span data-ttu-id="4b9cc-115">Vea [**cambiar el tamaño**](resize-flags.md) de las marcas para los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b9cc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b9cc-116">Return value</span></span>

<span data-ttu-id="4b9cc-117">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b9cc-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b9cc-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b9cc-118">Remarks</span></span>

<span data-ttu-id="4b9cc-119">DES puede llamar a este método antes o después de llamar a **Put \_ mediatype**.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="4b9cc-120">Si DES llama a este método antes de llamar a **Put \_ mediatype**, el filtro debe seleccionar un valor predeterminado para la profundidad de bits y usar los valores de tamaño para construir un tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="4b9cc-121">Si DES llama a este método después de llamar a **Put \_ mediatype**, el filtro debe modificar su tipo de salida actual con los nuevos tamaños.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="4b9cc-122">DES también puede llamar a este método después de que el PIN de salida esté conectado.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="4b9cc-123">En ese caso, modifique el tipo de salida y vuelva a conectar el PIN de salida con el nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="4b9cc-124">Consulte [reconexión de PIN](reconnecting-pins.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="4b9cc-125">El parámetro *Flags* especifica cómo el filtro debe realizar la operación de cambio de tamaño.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="4b9cc-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b9cc-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4b9cc-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4b9cc-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4b9cc-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b9cc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b9cc-129">Requirements</span></span>



| <span data-ttu-id="4b9cc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b9cc-130">Requirement</span></span> | <span data-ttu-id="4b9cc-131">Value</span><span class="sxs-lookup"><span data-stu-id="4b9cc-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9cc-132">Versión</span><span class="sxs-lookup"><span data-stu-id="4b9cc-132">Version</span></span><br/> | <span data-ttu-id="4b9cc-133">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4b9cc-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="4b9cc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b9cc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4b9cc-135"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b9cc-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4b9cc-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b9cc-136">Library</span></span><br/> | <dl> <span data-ttu-id="4b9cc-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b9cc-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b9cc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b9cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9cc-139">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4b9cc-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="4b9cc-140">**Interfaz IResize**</span><span class="sxs-lookup"><span data-stu-id="4b9cc-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




