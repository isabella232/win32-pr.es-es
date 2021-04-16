---
description: El \_ método put MaskNum especifica el código de borrado de SMPTE del borrado.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: 'IDxtJpeg: método de ut_MaskNum de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679457"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="a4ac6-103">IDxtJpeg::p \_ método MaskNum UT</span><span class="sxs-lookup"><span data-stu-id="a4ac6-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="a4ac6-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-104">\[Deprecated.</span></span> <span data-ttu-id="a4ac6-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4ac6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a4ac6-106">El `put_MaskNum` método especifica el código de borrado de SMPTE del borrado.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ac6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4ac6-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a4ac6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4ac6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ac6-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4ac6-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ac6-110">Especifica el código de borrado de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="a4ac6-111">Para obtener una lista de barridos SMPTE admitidos, consulte [transición de borrado de SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac6-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4ac6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4ac6-112">Return value</span></span>

<span data-ttu-id="a4ac6-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4ac6-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4ac6-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4ac6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4ac6-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4ac6-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a4ac6-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4ac6-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a4ac6-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4ac6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4ac6-119">Requirements</span></span>



| <span data-ttu-id="a4ac6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4ac6-120">Requirement</span></span> | <span data-ttu-id="a4ac6-121">Value</span><span class="sxs-lookup"><span data-stu-id="a4ac6-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ac6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4ac6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a4ac6-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4ac6-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a4ac6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4ac6-124">Library</span></span><br/> | <dl> <span data-ttu-id="a4ac6-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4ac6-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4ac6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4ac6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ac6-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="a4ac6-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




