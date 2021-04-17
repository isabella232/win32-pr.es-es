---
description: El método CreateEmptyNode crea un nuevo objeto Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'IAMTimeline:: CreateEmptyNode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679386"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="a7fa8-103">IAMTimeline:: CreateEmptyNode (método)</span><span class="sxs-lookup"><span data-stu-id="a7fa8-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="a7fa8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-104">\[Deprecated.</span></span> <span data-ttu-id="a7fa8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7fa8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a7fa8-106">El `CreateEmptyNode` método crea un nuevo objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="a7fa8-107">Utilice este método para crear objetos timeline, en lugar de la función **CoCreateInstance** , porque este método realiza rutinas de inicialización importantes.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="a7fa8-108">Cada objeto creado por este método admite al menos la interfaz [**IAMTimelineObj**](iamtimelineobj.md) , junto con otras interfaces específicas de ese tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fa8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7fa8-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="a7fa8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7fa8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fa8-111">*ppObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a7fa8-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa8-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa8-113">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="a7fa8-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="a7fa8-114">Miembro del tipo [**\_ principal \_**](timeline-major-type.md) de la escala de tiempo, que especifica el tipo de objeto que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fa8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7fa8-115">Return value</span></span>

<span data-ttu-id="a7fa8-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7fa8-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7fa8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7fa8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7fa8-118">Remarks</span></span>

<span data-ttu-id="a7fa8-119">No agregue el nuevo objeto a otra instancia de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="a7fa8-120">Cada objeto de una escala de tiempo debe crearse en esa escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="a7fa8-121">Si el método se ejecuta correctamente, la interfaz [**IAMTimelineObj**](iamtimelineobj.md) que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="a7fa8-122">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="a7fa8-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a7fa8-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7fa8-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a7fa8-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a7fa8-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7fa8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7fa8-126">Requirements</span></span>



| <span data-ttu-id="a7fa8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7fa8-127">Requirement</span></span> | <span data-ttu-id="a7fa8-128">Value</span><span class="sxs-lookup"><span data-stu-id="a7fa8-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fa8-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7fa8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a7fa8-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7fa8-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a7fa8-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7fa8-131">Library</span></span><br/> | <dl> <span data-ttu-id="a7fa8-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7fa8-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7fa8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7fa8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fa8-134">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="a7fa8-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="a7fa8-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a7fa8-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




