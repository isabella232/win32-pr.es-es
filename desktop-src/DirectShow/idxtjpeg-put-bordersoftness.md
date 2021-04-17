---
description: El \_ método put BorderSoftness especifica el ancho de la región borrosa alrededor de los bordes del patrón de barrido.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: 'IDxtJpeg: método de ut_BorderSoftness de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680985"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="00a25-103">IDxtJpeg::p \_ método BorderSoftness UT</span><span class="sxs-lookup"><span data-stu-id="00a25-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="00a25-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="00a25-104">\[Deprecated.</span></span> <span data-ttu-id="00a25-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="00a25-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="00a25-106">El `put_BorderSoftness` método especifica el ancho de la región borrosa alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="00a25-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a25-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00a25-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="00a25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a25-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00a25-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a25-110">Ancho de la región borrosa, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="00a25-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a25-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00a25-111">Return value</span></span>

<span data-ttu-id="00a25-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="00a25-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00a25-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00a25-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a25-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00a25-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="00a25-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="00a25-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="00a25-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="00a25-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="00a25-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="00a25-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00a25-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a25-118">Requirements</span></span>



| <span data-ttu-id="00a25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a25-119">Requirement</span></span> | <span data-ttu-id="00a25-120">Value</span><span class="sxs-lookup"><span data-stu-id="00a25-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00a25-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00a25-121">Header</span></span><br/>  | <dl> <span data-ttu-id="00a25-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a25-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="00a25-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00a25-123">Library</span></span><br/> | <dl> <span data-ttu-id="00a25-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00a25-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a25-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="00a25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a25-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="00a25-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




