---
description: No se admite.
ms.assetid: a6242c1d-cf9a-4c96-9cfd-d32199ae74b8
title: 'IAMTimelineObj:: GetGroupIBelongTo (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGroupIBelongTo
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cefd3bb5923e056497556b15b6308160a2066c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690761"
---
# <a name="iamtimelineobjgetgroupibelongto-method"></a><span data-ttu-id="1d676-103">IAMTimelineObj:: GetGroupIBelongTo (método)</span><span class="sxs-lookup"><span data-stu-id="1d676-103">IAMTimelineObj::GetGroupIBelongTo method</span></span>

> [!Note]  
> <span data-ttu-id="1d676-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1d676-104">\[Deprecated.</span></span> <span data-ttu-id="1d676-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d676-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d676-106">No se admite.</span><span class="sxs-lookup"><span data-stu-id="1d676-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d676-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d676-107">Syntax</span></span>


```C++
HRESULT GetGroupIBelongTo(
   IAMTimelineGroup **ppGroup
);
```



## <a name="parameters"></a><span data-ttu-id="1d676-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d676-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d676-109">*ppGroup*</span><span class="sxs-lookup"><span data-stu-id="1d676-109">*ppGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="1d676-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1d676-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d676-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d676-111">Return value</span></span>

<span data-ttu-id="1d676-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1d676-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d676-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d676-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d676-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d676-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d676-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1d676-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d676-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d676-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1d676-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1d676-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d676-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d676-118">Requirements</span></span>



| <span data-ttu-id="1d676-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d676-119">Requirement</span></span> | <span data-ttu-id="1d676-120">Value</span><span class="sxs-lookup"><span data-stu-id="1d676-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d676-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d676-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1d676-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d676-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1d676-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d676-123">Library</span></span><br/> | <dl> <span data-ttu-id="1d676-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d676-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d676-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d676-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d676-126">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="1d676-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




