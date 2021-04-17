---
description: El \_ método get height recupera el alto del rectángulo de destino.
ms.assetid: af555a7b-de0a-4c44-9623-f1ec8b44969a
title: 'Método IDxtCompositor:: get_Height (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1901264572f0deb3453738789f3d2cf2413fb401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680566"
---
# <a name="idxtcompositorget_height-method"></a><span data-ttu-id="f0c25-103">IDxtCompositor:: get \_ Height (método)</span><span class="sxs-lookup"><span data-stu-id="f0c25-103">IDxtCompositor::get\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="f0c25-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f0c25-104">\[Deprecated.</span></span> <span data-ttu-id="f0c25-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f0c25-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0c25-106">El `get_Height` método recupera el alto del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="f0c25-106">The `get_Height` method retrieves the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c25-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0c25-107">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f0c25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0c25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c25-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f0c25-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c25-110">Recibe el alto del rectángulo de destino, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f0c25-110">Receives the height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c25-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0c25-111">Return value</span></span>

<span data-ttu-id="f0c25-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f0c25-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0c25-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0c25-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c25-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0c25-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0c25-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f0c25-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0c25-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0c25-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0c25-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f0c25-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0c25-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c25-118">Requirements</span></span>



| <span data-ttu-id="f0c25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c25-119">Requirement</span></span> | <span data-ttu-id="f0c25-120">Value</span><span class="sxs-lookup"><span data-stu-id="f0c25-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c25-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0c25-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f0c25-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c25-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0c25-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0c25-123">Library</span></span><br/> | <dl> <span data-ttu-id="f0c25-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0c25-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c25-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c25-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="f0c25-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




