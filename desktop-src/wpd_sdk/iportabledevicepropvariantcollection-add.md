---
description: El método Add agrega un elemento a la colección.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'IPortableDevicePropVariantCollection:: Add (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708995"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="81a4a-103">IPortableDevicePropVariantCollection:: Add (método)</span><span class="sxs-lookup"><span data-stu-id="81a4a-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="81a4a-104">El método **Add** agrega un elemento a la colección.</span><span class="sxs-lookup"><span data-stu-id="81a4a-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81a4a-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="81a4a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81a4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a4a-107">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81a4a-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a4a-108">Puntero a un nuevo objeto **PROPVARIANT** que se va a agregar a la colección.</span><span class="sxs-lookup"><span data-stu-id="81a4a-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="81a4a-109">Este método copia el **PROPVARIANT** en la colección, por lo que debe liberar la copia local de la variable llamando a **PropVariantClear** después de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="81a4a-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a4a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81a4a-110">Return value</span></span>

<span data-ttu-id="81a4a-111">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="81a4a-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="81a4a-112">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="81a4a-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="81a4a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="81a4a-113">Return code</span></span>                                                                          | <span data-ttu-id="81a4a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="81a4a-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="81a4a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="81a4a-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="81a4a-116">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="81a4a-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81a4a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81a4a-117">Remarks</span></span>

<span data-ttu-id="81a4a-118">Cuando VARTYPE para *pValue* es VT \_ Vector o VT \_ UI1, no se admite el establecimiento y la recuperación de un búfer **nulo** o de tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="81a4a-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="81a4a-119">Por ejemplo, no se permite ningún pValue. Caub. pElems = **null** ni pvalue. Caub. cElems = 0.</span><span class="sxs-lookup"><span data-stu-id="81a4a-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="81a4a-120">Si un llamador intenta agregar un elemento de otro VARTYPE incluido en la colección y el valor PROPVARIANT no se puede cambiar automáticamente mediante esta interfaz, este método producirá un error.</span><span class="sxs-lookup"><span data-stu-id="81a4a-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="81a4a-121">Para cambiar el tipo de colección manualmente, llame a [**IPortableDevicePropVariantCollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="81a4a-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="81a4a-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="81a4a-122">Examples</span></span>

<span data-ttu-id="81a4a-123">Para obtener un ejemplo de cómo usar este método, vea [recuperar un identificador de objeto de un identificador único persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md) .</span><span class="sxs-lookup"><span data-stu-id="81a4a-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="81a4a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a4a-124">Requirements</span></span>



| <span data-ttu-id="81a4a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a4a-125">Requirement</span></span> | <span data-ttu-id="81a4a-126">Value</span><span class="sxs-lookup"><span data-stu-id="81a4a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a4a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81a4a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="81a4a-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a4a-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="81a4a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81a4a-129">Library</span></span><br/> | <dl> <span data-ttu-id="81a4a-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81a4a-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a4a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="81a4a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a4a-132">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="81a4a-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="81a4a-133">Mover contenido en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="81a4a-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="81a4a-134">Recuperar un identificador de objeto de un identificador único persistente</span><span class="sxs-lookup"><span data-stu-id="81a4a-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




