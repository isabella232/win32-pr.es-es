---
description: El \_ método get OffsetX recupera el desplazamiento horizontal del rectángulo de destino.
ms.assetid: a9d8c81b-f978-4b47-9c7f-12cee7c2c40d
title: 'Método IDxtCompositor:: get_OffsetX (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8e2f21956e67b42158f4e646d33aa6e3e90d9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680987"
---
# <a name="idxtcompositorget_offsetx-method"></a><span data-ttu-id="27045-103">IDxtCompositor:: get \_ offsetX (método)</span><span class="sxs-lookup"><span data-stu-id="27045-103">IDxtCompositor::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="27045-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="27045-104">\[Deprecated.</span></span> <span data-ttu-id="27045-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27045-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27045-106">El `get_OffsetX` método recupera el desplazamiento horizontal del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="27045-106">The `get_OffsetX` method retrieves the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="27045-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27045-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="27045-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27045-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27045-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27045-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27045-110">Recibe el desplazamiento horizontal del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="27045-110">Receives the horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27045-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27045-111">Return value</span></span>

<span data-ttu-id="27045-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="27045-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27045-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27045-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27045-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27045-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="27045-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="27045-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27045-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27045-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27045-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27045-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27045-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27045-118">Requirements</span></span>



| <span data-ttu-id="27045-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27045-119">Requirement</span></span> | <span data-ttu-id="27045-120">Value</span><span class="sxs-lookup"><span data-stu-id="27045-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27045-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27045-121">Header</span></span><br/>  | <dl> <span data-ttu-id="27045-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="27045-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27045-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27045-123">Library</span></span><br/> | <dl> <span data-ttu-id="27045-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27045-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27045-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="27045-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27045-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="27045-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




