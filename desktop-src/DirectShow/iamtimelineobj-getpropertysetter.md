---
description: El método GetPropertySetter recupera el establecedor de propiedad del objeto. Cuando se representa el objeto, la información de la propiedad contenida en el establecedor de propiedad se aplica al objeto.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'IAMTimelineObj:: GetPropertySetter (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690759"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="deac2-104">IAMTimelineObj:: GetPropertySetter (método)</span><span class="sxs-lookup"><span data-stu-id="deac2-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="deac2-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="deac2-105">\[Deprecated.</span></span> <span data-ttu-id="deac2-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="deac2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="deac2-107">El `GetPropertySetter` método recupera el establecedor de propiedad del objeto.</span><span class="sxs-lookup"><span data-stu-id="deac2-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="deac2-108">Cuando se representa el objeto, la información de la propiedad contenida en el establecedor de propiedad se aplica al objeto.</span><span class="sxs-lookup"><span data-stu-id="deac2-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="deac2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="deac2-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="deac2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="deac2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deac2-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="deac2-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="deac2-112">Recibe un puntero a la interfaz [**IPropertySetter**](ipropertysetter.md) del establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="deac2-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="deac2-113">Si el objeto no tiene un establecedor de propiedad, el valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="deac2-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deac2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="deac2-114">Return value</span></span>

<span data-ttu-id="deac2-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="deac2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="deac2-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="deac2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="deac2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="deac2-117">Remarks</span></span>

<span data-ttu-id="deac2-118">Si el valor devuelto en *pval* no es **null**, la interfaz **IPropertySetter** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="deac2-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="deac2-119">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="deac2-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="deac2-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="deac2-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="deac2-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="deac2-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="deac2-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="deac2-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="deac2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deac2-123">Requirements</span></span>



| <span data-ttu-id="deac2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="deac2-124">Requirement</span></span> | <span data-ttu-id="deac2-125">Value</span><span class="sxs-lookup"><span data-stu-id="deac2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deac2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deac2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="deac2-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="deac2-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="deac2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deac2-128">Library</span></span><br/> | <dl> <span data-ttu-id="deac2-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deac2-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deac2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="deac2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deac2-131">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="deac2-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="deac2-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="deac2-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




