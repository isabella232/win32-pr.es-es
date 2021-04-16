---
description: El \_ método put SrcWidth especifica el ancho del rectángulo de origen.
ms.assetid: 3dbf8ddb-1da9-468f-9960-30e7b8c305e0
title: 'IDxtCompositor: método de ut_SrcWidth de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7a1e32d5c38c69b61e52e7e66cc40d59ffae31c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679473"
---
# <a name="idxtcompositorput_srcwidth-method"></a><span data-ttu-id="2e66a-103">IDxtCompositor::p \_ método SrcWidth UT</span><span class="sxs-lookup"><span data-stu-id="2e66a-103">IDxtCompositor::put\_SrcWidth method</span></span>

> [!Note]  
> <span data-ttu-id="2e66a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2e66a-104">\[Deprecated.</span></span> <span data-ttu-id="2e66a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e66a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e66a-106">El `put_SrcWidth` método especifica el ancho del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2e66a-106">The `put_SrcWidth` method specifies the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e66a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e66a-107">Syntax</span></span>


```C++
HRESULT put_SrcWidth(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="2e66a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e66a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e66a-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e66a-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e66a-110">Ancho del rectángulo de origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2e66a-110">The width of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e66a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e66a-111">Return value</span></span>

<span data-ttu-id="2e66a-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2e66a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e66a-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e66a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e66a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e66a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e66a-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2e66a-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e66a-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e66a-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e66a-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2e66a-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e66a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e66a-118">Requirements</span></span>



| <span data-ttu-id="2e66a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e66a-119">Requirement</span></span> | <span data-ttu-id="2e66a-120">Value</span><span class="sxs-lookup"><span data-stu-id="2e66a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e66a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e66a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e66a-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e66a-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e66a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e66a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e66a-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e66a-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e66a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e66a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e66a-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="2e66a-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




