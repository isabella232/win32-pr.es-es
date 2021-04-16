---
description: El método GetGroup recupera un grupo especificado.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'IAMTimeline:: GetGroup (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679160"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="de2d1-103">IAMTimeline:: GetGroup (método)</span><span class="sxs-lookup"><span data-stu-id="de2d1-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="de2d1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="de2d1-104">\[Deprecated.</span></span> <span data-ttu-id="de2d1-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de2d1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="de2d1-106">El `GetGroup` método recupera un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="de2d1-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de2d1-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="de2d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de2d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de2d1-109">*ppGroup* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="de2d1-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de2d1-110">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del grupo.</span><span class="sxs-lookup"><span data-stu-id="de2d1-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="de2d1-111">*WhichGroup*</span><span class="sxs-lookup"><span data-stu-id="de2d1-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="de2d1-112">Índice del grupo que se va a recuperar, en función del orden en que se agregaron los grupos a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="de2d1-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="de2d1-113">El primer grupo agregado a la escala de tiempo tiene un índice de 0.</span><span class="sxs-lookup"><span data-stu-id="de2d1-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de2d1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de2d1-114">Return value</span></span>

<span data-ttu-id="de2d1-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="de2d1-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de2d1-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de2d1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de2d1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de2d1-117">Remarks</span></span>

<span data-ttu-id="de2d1-118">Si el método se ejecuta correctamente, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="de2d1-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="de2d1-119">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="de2d1-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="de2d1-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="de2d1-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="de2d1-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="de2d1-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="de2d1-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="de2d1-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de2d1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de2d1-123">Requirements</span></span>



| <span data-ttu-id="de2d1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="de2d1-124">Requirement</span></span> | <span data-ttu-id="de2d1-125">Value</span><span class="sxs-lookup"><span data-stu-id="de2d1-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de2d1-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de2d1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="de2d1-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="de2d1-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="de2d1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de2d1-128">Library</span></span><br/> | <dl> <span data-ttu-id="de2d1-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de2d1-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de2d1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="de2d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de2d1-131">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="de2d1-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="de2d1-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="de2d1-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




