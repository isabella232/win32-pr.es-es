---
description: El \_ método put MaskName especifica el nombre de un archivo JPEG que se va a usar como máscara de borrado.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg: método de ut_MaskName de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680437"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="c9090-103">IDxtJpeg::p \_ método MaskName UT</span><span class="sxs-lookup"><span data-stu-id="c9090-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="c9090-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c9090-104">\[Deprecated.</span></span> <span data-ttu-id="c9090-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c9090-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c9090-106">El `put_MaskName` método especifica el nombre de un archivo JPEG que se va a usar como máscara de borrado.</span><span class="sxs-lookup"><span data-stu-id="c9090-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="c9090-107">Esta máscara se usará en lugar de una de las máscaras de borrado integradas.</span><span class="sxs-lookup"><span data-stu-id="c9090-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="c9090-108">El archivo debe contener un degradado monocromo de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="c9090-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="c9090-109">El degradado se usa como máscara para definir la progresión del barrido.</span><span class="sxs-lookup"><span data-stu-id="c9090-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9090-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9090-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c9090-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9090-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9090-112">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9090-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9090-113">Especifica el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="c9090-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9090-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9090-114">Return value</span></span>

<span data-ttu-id="c9090-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c9090-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9090-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9090-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9090-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9090-117">Remarks</span></span>

<span data-ttu-id="c9090-118">Para revertir a una máscara integrada, establezca la propiedad **MaskNum** .</span><span class="sxs-lookup"><span data-stu-id="c9090-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="c9090-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c9090-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c9090-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9090-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c9090-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c9090-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9090-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9090-122">Requirements</span></span>



| <span data-ttu-id="c9090-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9090-123">Requirement</span></span> | <span data-ttu-id="c9090-124">Value</span><span class="sxs-lookup"><span data-stu-id="c9090-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9090-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9090-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c9090-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9090-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c9090-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9090-127">Library</span></span><br/> | <dl> <span data-ttu-id="c9090-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9090-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9090-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9090-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9090-130">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="c9090-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="c9090-131">**IDxtJpeg::p UT \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="c9090-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




