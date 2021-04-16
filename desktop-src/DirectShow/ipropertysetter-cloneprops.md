---
description: El método CloneProps clona un conjunto de propiedades de este establecedor de propiedad y los agrega a un nuevo establecedor de propiedad.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'IPropertySetter:: CloneProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690102"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="2485e-103">IPropertySetter:: CloneProps (método)</span><span class="sxs-lookup"><span data-stu-id="2485e-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="2485e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2485e-104">\[Deprecated.</span></span> <span data-ttu-id="2485e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2485e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2485e-106">El `CloneProps` método clona un conjunto de propiedades de este establecedor de propiedad y los agrega a un nuevo establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2485e-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2485e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2485e-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="2485e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2485e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2485e-109">*ppSetter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2485e-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2485e-110">Recibe un puntero a la interfaz **IPropertySetter** del nuevo establecedor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2485e-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="2485e-111">*rtStart* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2485e-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2485e-112">Hora de inicio del intervalo de valores que se va a clonar, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="2485e-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="2485e-113">*rtStop* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2485e-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2485e-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="2485e-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2485e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2485e-115">Return value</span></span>

<span data-ttu-id="2485e-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2485e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2485e-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2485e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2485e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2485e-118">Remarks</span></span>

<span data-ttu-id="2485e-119">Solo se clonan los valores que se encuentran después de la hora de inicio especificada.</span><span class="sxs-lookup"><span data-stu-id="2485e-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="2485e-120">Las horas de los valores clonados se ajustan en relación con la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="2485e-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="2485e-121">Por ejemplo, si *rtStart* es 20 millones (2 segundos), se clona un valor en el tiempo 30 millones (3 segundos) con la hora 10 millones (1 segundo).</span><span class="sxs-lookup"><span data-stu-id="2485e-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="2485e-122">Por último, a cada propiedad clonada se le asigna un valor inicial igual al valor de la propiedad original en la hora de inicio (correctamente interpolada si es necesario).</span><span class="sxs-lookup"><span data-stu-id="2485e-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="2485e-123">En efecto, los datos de la propiedad se dividen a la hora de inicio especificada.</span><span class="sxs-lookup"><span data-stu-id="2485e-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="2485e-124">Si el método se ejecuta correctamente, la interfaz [**IPropertySetter**](ipropertysetter.md) que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="2485e-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="2485e-125">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="2485e-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="2485e-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2485e-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2485e-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2485e-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2485e-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2485e-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2485e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2485e-129">Requirements</span></span>



| <span data-ttu-id="2485e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2485e-130">Requirement</span></span> | <span data-ttu-id="2485e-131">Value</span><span class="sxs-lookup"><span data-stu-id="2485e-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2485e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2485e-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2485e-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2485e-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2485e-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2485e-134">Library</span></span><br/> | <dl> <span data-ttu-id="2485e-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2485e-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2485e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2485e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2485e-137">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="2485e-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="2485e-138">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="2485e-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




