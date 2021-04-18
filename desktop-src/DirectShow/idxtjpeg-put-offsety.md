---
description: El \_ método de desplazamiento de put especifica el desplazamiento vertical del origen de borrado.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: 'IDxtJpeg: método de ut_OffsetY de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680945"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="e6998-103">IDxtJpeg::p método de desplazamiento de UT \_</span><span class="sxs-lookup"><span data-stu-id="e6998-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="e6998-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e6998-104">\[Deprecated.</span></span> <span data-ttu-id="e6998-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6998-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6998-106">El `put_OffsetY` método especifica el desplazamiento vertical del origen de borrado.</span><span class="sxs-lookup"><span data-stu-id="e6998-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6998-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6998-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e6998-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6998-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6998-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6998-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6998-110">Desplazamiento vertical del origen de borrado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e6998-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="e6998-111">El centro del borrado se desplaza por esta cantidad.</span><span class="sxs-lookup"><span data-stu-id="e6998-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6998-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6998-112">Return value</span></span>

<span data-ttu-id="e6998-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e6998-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6998-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6998-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6998-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6998-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6998-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e6998-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6998-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6998-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6998-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e6998-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6998-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6998-119">Requirements</span></span>



| <span data-ttu-id="e6998-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6998-120">Requirement</span></span> | <span data-ttu-id="e6998-121">Value</span><span class="sxs-lookup"><span data-stu-id="e6998-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6998-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6998-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e6998-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6998-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6998-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6998-124">Library</span></span><br/> | <dl> <span data-ttu-id="e6998-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6998-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6998-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6998-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6998-127">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="e6998-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




