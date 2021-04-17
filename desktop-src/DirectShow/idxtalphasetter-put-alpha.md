---
description: El \_ método Alpha Put especifica el valor alfa de toda la imagen.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter: método de ut_Alpha de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690573"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="e9f94-103">IDxtAlphaSetter: \_ método alfa:p UT</span><span class="sxs-lookup"><span data-stu-id="e9f94-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="e9f94-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e9f94-104">\[Deprecated.</span></span> <span data-ttu-id="e9f94-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9f94-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e9f94-106">El `put_Alpha` método especifica el valor alfa de toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="e9f94-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f94-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9f94-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="e9f94-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9f94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f94-109">*Alfa* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9f94-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f94-110">Valor alfa.</span><span class="sxs-lookup"><span data-stu-id="e9f94-110">The alpha value.</span></span> <span data-ttu-id="e9f94-111">Este valor se aplicará a toda la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="e9f94-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="e9f94-112">Para deshabilitar esta propiedad, establezca un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="e9f94-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f94-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9f94-113">Return value</span></span>

<span data-ttu-id="e9f94-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e9f94-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9f94-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9f94-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f94-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9f94-116">Remarks</span></span>

<span data-ttu-id="e9f94-117">Si establece esta propiedad en un valor no negativo, también debe deshabilitar la propiedad de rampa alfa, llamando a **Put \_ AlphaRamp** con un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="e9f94-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="e9f94-118">De lo contrario, el efecto no se representará correctamente.</span><span class="sxs-lookup"><span data-stu-id="e9f94-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="e9f94-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e9f94-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9f94-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9f94-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e9f94-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e9f94-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9f94-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9f94-122">Requirements</span></span>



| <span data-ttu-id="e9f94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f94-123">Requirement</span></span> | <span data-ttu-id="e9f94-124">Value</span><span class="sxs-lookup"><span data-stu-id="e9f94-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f94-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9f94-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f94-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f94-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e9f94-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9f94-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9f94-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9f94-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f94-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9f94-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f94-130">**Interfaz IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="e9f94-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="e9f94-131">**IDxtAlphaSetter::p UT \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="e9f94-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




