---
description: El \_ método get SrcOffsetX recupera el desplazamiento horizontal del rectángulo de origen.
ms.assetid: 528a5306-86bd-4ae2-ad03-57247362c5b5
title: 'Método IDxtCompositor:: get_SrcOffsetX (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ee116537061986a556854aed093b5e9a414016e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680684"
---
# <a name="idxtcompositorget_srcoffsetx-method"></a><span data-ttu-id="a22f4-103">IDxtCompositor:: get \_ SrcOffsetX (método)</span><span class="sxs-lookup"><span data-stu-id="a22f4-103">IDxtCompositor::get\_SrcOffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="a22f4-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a22f4-104">\[Deprecated.</span></span> <span data-ttu-id="a22f4-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a22f4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a22f4-106">El `get_SrcOffsetX` método recupera el desplazamiento horizontal del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="a22f4-106">The `get_SrcOffsetX` method retrieves the horizontal offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22f4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a22f4-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a22f4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a22f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22f4-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a22f4-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a22f4-110">Recibe el desplazamiento horizontal del rectángulo de origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a22f4-110">Receives the horizontal offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a22f4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a22f4-111">Return value</span></span>

<span data-ttu-id="a22f4-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a22f4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a22f4-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a22f4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22f4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a22f4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a22f4-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a22f4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a22f4-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a22f4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a22f4-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a22f4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a22f4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22f4-118">Requirements</span></span>



| <span data-ttu-id="a22f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22f4-119">Requirement</span></span> | <span data-ttu-id="a22f4-120">Value</span><span class="sxs-lookup"><span data-stu-id="a22f4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a22f4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a22f4-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a22f4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a22f4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a22f4-123">Library</span></span><br/> | <dl> <span data-ttu-id="a22f4-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a22f4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22f4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a22f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22f4-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="a22f4-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




