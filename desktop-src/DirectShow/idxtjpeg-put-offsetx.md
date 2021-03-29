---
description: El \_ método put OffsetX especifica el desplazamiento horizontal del origen de borrado.
ms.assetid: 7bc721fd-7e72-49d4-90ae-a193df46326c
title: 'IDxtJpeg: método de ut_OffsetX de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 70bb908be3f2e2173ebae12f45e24600b38a0441
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678937"
---
# <a name="idxtjpegput_offsetx-method"></a><span data-ttu-id="69b0e-103">IDxtJpeg::p el \_ método UT OffsetX</span><span class="sxs-lookup"><span data-stu-id="69b0e-103">IDxtJpeg::put\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="69b0e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="69b0e-104">\[Deprecated.</span></span> <span data-ttu-id="69b0e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69b0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="69b0e-106">El `put_OffsetX` método especifica el desplazamiento horizontal del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="69b0e-106">The `put_OffsetX` method specifies the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69b0e-107">Syntax</span></span>


```C++
HRESULT put_OffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="69b0e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69b0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b0e-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69b0e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b0e-110">Desplazamiento horizontal del origen de borrado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="69b0e-110">The horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="69b0e-111">El centro del borrado se desplaza por esta cantidad.</span><span class="sxs-lookup"><span data-stu-id="69b0e-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b0e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69b0e-112">Return value</span></span>

<span data-ttu-id="69b0e-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="69b0e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69b0e-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69b0e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b0e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69b0e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69b0e-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="69b0e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="69b0e-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="69b0e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="69b0e-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="69b0e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69b0e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b0e-119">Requirements</span></span>



| <span data-ttu-id="69b0e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b0e-120">Requirement</span></span> | <span data-ttu-id="69b0e-121">Value</span><span class="sxs-lookup"><span data-stu-id="69b0e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69b0e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69b0e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="69b0e-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b0e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="69b0e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69b0e-124">Library</span></span><br/> | <dl> <span data-ttu-id="69b0e-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69b0e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b0e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="69b0e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b0e-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="69b0e-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




