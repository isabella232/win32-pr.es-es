---
description: El método GetPriority (recupera la prioridad del grupo.
ms.assetid: d698317f-ace6-40ed-b125-7e2427fb683b
title: 'IAMTimelineGroup:: GetPriority ((método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eef0c4e0c2db439a7c593841d3aed44ab7654db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680308"
---
# <a name="iamtimelinegroupgetpriority-method"></a><span data-ttu-id="fdc01-103">IAMTimelineGroup:: GetPriority ((método)</span><span class="sxs-lookup"><span data-stu-id="fdc01-103">IAMTimelineGroup::GetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="fdc01-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fdc01-104">\[Deprecated.</span></span> <span data-ttu-id="fdc01-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fdc01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fdc01-106">El `GetPriority` método recupera la prioridad del grupo.</span><span class="sxs-lookup"><span data-stu-id="fdc01-106">The `GetPriority` method retrieves the group's priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc01-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdc01-107">Syntax</span></span>


```C++
HRESULT GetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="fdc01-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdc01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc01-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="fdc01-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc01-110">Recibe la prioridad del grupo.</span><span class="sxs-lookup"><span data-stu-id="fdc01-110">Receives the group's priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc01-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdc01-111">Return value</span></span>

<span data-ttu-id="fdc01-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fdc01-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fdc01-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fdc01-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc01-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdc01-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fdc01-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fdc01-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fdc01-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdc01-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fdc01-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fdc01-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fdc01-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdc01-118">Requirements</span></span>



| <span data-ttu-id="fdc01-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc01-119">Requirement</span></span> | <span data-ttu-id="fdc01-120">Value</span><span class="sxs-lookup"><span data-stu-id="fdc01-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc01-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdc01-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fdc01-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc01-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fdc01-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdc01-123">Library</span></span><br/> | <dl> <span data-ttu-id="fdc01-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdc01-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc01-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdc01-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc01-126">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="fdc01-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="fdc01-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="fdc01-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




