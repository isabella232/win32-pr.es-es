---
description: El método SetPropertySetter establece el establecedor de la propiedad del objeto. Cuando se representa el objeto, la información de la propiedad contenida en el establecedor de propiedad se aplica al objeto. Llame a este método en objetos de transición y efecto.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'IAMTimelineObj:: SetPropertySetter (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680726"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="d58d0-105">IAMTimelineObj:: SetPropertySetter (método)</span><span class="sxs-lookup"><span data-stu-id="d58d0-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="d58d0-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d58d0-106">\[Deprecated.</span></span> <span data-ttu-id="d58d0-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d58d0-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d58d0-108">El `SetPropertySetter` método establece el establecedor de propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="d58d0-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="d58d0-109">Cuando se representa el objeto, la información de la propiedad contenida en el establecedor de propiedad se aplica al objeto.</span><span class="sxs-lookup"><span data-stu-id="d58d0-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="d58d0-110">Llame a este método en objetos de transición y efecto.</span><span class="sxs-lookup"><span data-stu-id="d58d0-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="d58d0-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d58d0-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d58d0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d58d0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d58d0-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="d58d0-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d58d0-114">Puntero a la interfaz [**IPropertySetter**](ipropertysetter.md) del establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d58d0-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d58d0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d58d0-115">Return value</span></span>

<span data-ttu-id="d58d0-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d58d0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d58d0-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d58d0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d58d0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d58d0-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d58d0-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d58d0-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d58d0-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d58d0-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d58d0-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d58d0-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d58d0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d58d0-122">Requirements</span></span>



| <span data-ttu-id="d58d0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d58d0-123">Requirement</span></span> | <span data-ttu-id="d58d0-124">Value</span><span class="sxs-lookup"><span data-stu-id="d58d0-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d58d0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d58d0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d58d0-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d58d0-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d58d0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d58d0-127">Library</span></span><br/> | <dl> <span data-ttu-id="d58d0-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d58d0-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d58d0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d58d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58d0-130">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="d58d0-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d58d0-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d58d0-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




