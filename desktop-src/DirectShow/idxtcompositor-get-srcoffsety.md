---
description: El \_ método get SrcOffsetY recupera el desplazamiento vertical del rectángulo de origen.
ms.assetid: b692e71b-c7a9-437c-9127-fa517e817883
title: 'Método IDxtCompositor:: get_SrcOffsetY (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fbe254037d35504a46aed519f1030a9d0aff0d02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680677"
---
# <a name="idxtcompositorget_srcoffsety-method"></a><span data-ttu-id="85890-103">IDxtCompositor:: get \_ SrcOffsetY (método)</span><span class="sxs-lookup"><span data-stu-id="85890-103">IDxtCompositor::get\_SrcOffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="85890-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="85890-104">\[Deprecated.</span></span> <span data-ttu-id="85890-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85890-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="85890-106">El `get_SrcOffsetY` método recupera el desplazamiento vertical del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="85890-106">The `get_SrcOffsetY` method retrieves the vertical offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="85890-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85890-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="85890-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85890-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85890-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="85890-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="85890-110">Recibe el desplazamiento vertical del rectángulo de origen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="85890-110">Receives the vertical offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85890-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85890-111">Return value</span></span>

<span data-ttu-id="85890-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="85890-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85890-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85890-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85890-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85890-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85890-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="85890-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="85890-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="85890-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="85890-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="85890-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85890-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85890-118">Requirements</span></span>



| <span data-ttu-id="85890-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="85890-119">Requirement</span></span> | <span data-ttu-id="85890-120">Value</span><span class="sxs-lookup"><span data-stu-id="85890-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85890-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85890-121">Header</span></span><br/>  | <dl> <span data-ttu-id="85890-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="85890-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="85890-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85890-123">Library</span></span><br/> | <dl> <span data-ttu-id="85890-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85890-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85890-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="85890-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85890-126">**Interfaz IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="85890-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




