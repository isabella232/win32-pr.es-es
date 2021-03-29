---
description: El \_ método get BorderSoftness recupera el ancho de la región borrosa alrededor de los bordes del patrón de barrido.
ms.assetid: f5648cce-e44c-4ed6-8254-6511cd600629
title: 'Método IDxtJpeg:: get_BorderSoftness (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 968dbef4a87a7b88e16321693350d35d08225c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679273"
---
# <a name="idxtjpegget_bordersoftness-method"></a><span data-ttu-id="1f419-103">IDxtJpeg:: get \_ BorderSoftness (método)</span><span class="sxs-lookup"><span data-stu-id="1f419-103">IDxtJpeg::get\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="1f419-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1f419-104">\[Deprecated.</span></span> <span data-ttu-id="1f419-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1f419-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1f419-106">El `get_BorderSoftness` método recupera el ancho de la región borrosa alrededor de los bordes del patrón de barrido.</span><span class="sxs-lookup"><span data-stu-id="1f419-106">The `get_BorderSoftness` method retrieves the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f419-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f419-107">Syntax</span></span>


```C++
HRESULT get_BorderSoftness(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1f419-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f419-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f419-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1f419-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1f419-110">Recibe el ancho de la región borrosa, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1f419-110">Receives the width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f419-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f419-111">Return value</span></span>

<span data-ttu-id="1f419-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1f419-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f419-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f419-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f419-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f419-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f419-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1f419-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1f419-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1f419-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1f419-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1f419-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f419-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f419-118">Requirements</span></span>



| <span data-ttu-id="1f419-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f419-119">Requirement</span></span> | <span data-ttu-id="1f419-120">Value</span><span class="sxs-lookup"><span data-stu-id="1f419-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f419-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f419-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1f419-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f419-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1f419-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f419-123">Library</span></span><br/> | <dl> <span data-ttu-id="1f419-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f419-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f419-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f419-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f419-126">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="1f419-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




