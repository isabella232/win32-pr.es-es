---
description: El \_ método put BorderColor especifica el color del borde alrededor de los bordes del patrón de barrido.
ms.assetid: d6a49956-8fc9-4ba2-8485-a49175da3cf7
title: 'IDxtJpeg: método de ut_BorderColor de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faacc76eaa120467aa6cfb6c318aac0d9baec334
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679210"
---
# <a name="idxtjpegput_bordercolor-method"></a><span data-ttu-id="f48a0-103">IDxtJpeg::p \_ método BorderColor BorderColor</span><span class="sxs-lookup"><span data-stu-id="f48a0-103">IDxtJpeg::put\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="f48a0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f48a0-104">\[Deprecated.</span></span> <span data-ttu-id="f48a0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f48a0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f48a0-106">El `put_BorderColor` método especifica el color del borde alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="f48a0-106">The `put_BorderColor` method specifies the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="f48a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f48a0-107">Syntax</span></span>


```C++
HRESULT put_BorderColor(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f48a0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f48a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f48a0-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f48a0-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f48a0-110">Especifica el color como un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.</span><span class="sxs-lookup"><span data-stu-id="f48a0-110">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f48a0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f48a0-111">Return value</span></span>

<span data-ttu-id="f48a0-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f48a0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f48a0-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f48a0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f48a0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f48a0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f48a0-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f48a0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f48a0-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f48a0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f48a0-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f48a0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f48a0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f48a0-118">Requirements</span></span>



| <span data-ttu-id="f48a0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f48a0-119">Requirement</span></span> | <span data-ttu-id="f48a0-120">Value</span><span class="sxs-lookup"><span data-stu-id="f48a0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f48a0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f48a0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f48a0-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f48a0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f48a0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f48a0-123">Library</span></span><br/> | <dl> <span data-ttu-id="f48a0-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f48a0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f48a0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f48a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48a0-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="f48a0-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




