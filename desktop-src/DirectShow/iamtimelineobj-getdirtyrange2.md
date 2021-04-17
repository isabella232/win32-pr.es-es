---
description: No se admite.
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: 'IAMTimelineObj:: GetDirtyRange2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 44a78366c14db35f0b90b6e09cd4851d1b0a3855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681223"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="87ee8-103">IAMTimelineObj:: GetDirtyRange2 (método)</span><span class="sxs-lookup"><span data-stu-id="87ee8-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="87ee8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="87ee8-104">\[Deprecated.</span></span> <span data-ttu-id="87ee8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="87ee8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="87ee8-106">No se admite.</span><span class="sxs-lookup"><span data-stu-id="87ee8-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ee8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87ee8-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="87ee8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87ee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ee8-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="87ee8-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="87ee8-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="87ee8-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="87ee8-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="87ee8-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="87ee8-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="87ee8-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ee8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87ee8-113">Return value</span></span>

<span data-ttu-id="87ee8-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="87ee8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87ee8-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87ee8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ee8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87ee8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87ee8-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="87ee8-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="87ee8-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="87ee8-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="87ee8-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="87ee8-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87ee8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ee8-120">Requirements</span></span>



| <span data-ttu-id="87ee8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ee8-121">Requirement</span></span> | <span data-ttu-id="87ee8-122">Value</span><span class="sxs-lookup"><span data-stu-id="87ee8-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ee8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87ee8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="87ee8-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="87ee8-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="87ee8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87ee8-125">Library</span></span><br/> | <dl> <span data-ttu-id="87ee8-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87ee8-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ee8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="87ee8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ee8-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="87ee8-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




