---
description: El \_ método put SrcHeight especifica el alto del rectángulo de origen.
ms.assetid: 80c8cf92-36e2-4e57-8ce7-6a114bc8bab4
title: 'IDxtCompositor: método de ut_SrcHeight de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 80697a3c4a159256389f48273e66ca86547478fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680418"
---
# <a name="idxtcompositorput_srcheight-method"></a><span data-ttu-id="c3af3-103">IDxtCompositor::p \_ método SrcHeight UT</span><span class="sxs-lookup"><span data-stu-id="c3af3-103">IDxtCompositor::put\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="c3af3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c3af3-104">\[Deprecated.</span></span> <span data-ttu-id="c3af3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3af3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c3af3-106">El `put_SrcHeight` método especifica el alto del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="c3af3-106">The `put_SrcHeight` method specifies the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3af3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3af3-107">Syntax</span></span>


```C++
HRESULT put_SrcHeight(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c3af3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3af3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3af3-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3af3-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3af3-110">Alto del rectángulo de origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c3af3-110">The height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3af3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3af3-111">Return value</span></span>

<span data-ttu-id="c3af3-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c3af3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c3af3-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3af3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3af3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3af3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c3af3-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c3af3-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c3af3-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3af3-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c3af3-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c3af3-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3af3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3af3-118">Requirements</span></span>



| <span data-ttu-id="c3af3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3af3-119">Requirement</span></span> | <span data-ttu-id="c3af3-120">Value</span><span class="sxs-lookup"><span data-stu-id="c3af3-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3af3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3af3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c3af3-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3af3-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c3af3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3af3-123">Library</span></span><br/> | <dl> <span data-ttu-id="c3af3-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3af3-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3af3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3af3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3af3-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="c3af3-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




