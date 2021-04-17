---
description: El \_ método get width recupera el ancho del rectángulo de destino.
ms.assetid: 023c976e-279e-489c-ada5-ae33144c6358
title: 'Método IDxtCompositor:: get_Width (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_Width
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8f7b18e4cc02b28284f8ce680a7de04eaf8c9b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680674"
---
# <a name="idxtcompositorget_width-method"></a><span data-ttu-id="d883d-103">IDxtCompositor:: get \_ width (método)</span><span class="sxs-lookup"><span data-stu-id="d883d-103">IDxtCompositor::get\_Width method</span></span>

> [!Note]  
> <span data-ttu-id="d883d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d883d-104">\[Deprecated.</span></span> <span data-ttu-id="d883d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d883d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d883d-106">El `get_Width` método recupera el ancho del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="d883d-106">The `get_Width` method retrieves the width of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d883d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d883d-107">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d883d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d883d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d883d-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d883d-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d883d-110">Recibe el ancho del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="d883d-110">Receives the width of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d883d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d883d-111">Return value</span></span>

<span data-ttu-id="d883d-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d883d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d883d-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d883d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d883d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d883d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d883d-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d883d-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d883d-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d883d-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d883d-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d883d-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d883d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d883d-118">Requirements</span></span>



| <span data-ttu-id="d883d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d883d-119">Requirement</span></span> | <span data-ttu-id="d883d-120">Value</span><span class="sxs-lookup"><span data-stu-id="d883d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d883d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d883d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d883d-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d883d-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d883d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d883d-123">Library</span></span><br/> | <dl> <span data-ttu-id="d883d-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d883d-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d883d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d883d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d883d-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="d883d-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




