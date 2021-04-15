---
title: IWMPStringCollection (método del elemento)
description: El método Item devuelve la cadena en el índice especificado.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Método de elemento Media Player de Windows
- Método de elemento Windows Media Player, interfaz IWMPStringCollection
- Interfaz IWMPStringCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708779"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="5a968-106">IWMPStringCollection:: Item (método)</span><span class="sxs-lookup"><span data-stu-id="5a968-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="5a968-107">El método **Item** devuelve la cadena en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5a968-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a968-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a968-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="5a968-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a968-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a968-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a968-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a968-111">**System. Int32** que es el índice.</span><span class="sxs-lookup"><span data-stu-id="5a968-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a968-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a968-112">Return value</span></span>

<span data-ttu-id="5a968-113">**System. String** que es la cadena que se encuentra en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5a968-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a968-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a968-114">Remarks</span></span>

<span data-ttu-id="5a968-115">La interfaz **IWMPStringCollection** se usa para recuperar el conjunto de valores disponibles para un atributo.</span><span class="sxs-lookup"><span data-stu-id="5a968-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="5a968-116">Por ejemplo, el método **IWMPMediaCollection. getAttributeStringCollection** se puede usar para recuperar una interfaz **IWMPStringCollection** que representa todos los valores del atributo Genre en el tipo de medio de audio.</span><span class="sxs-lookup"><span data-stu-id="5a968-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="5a968-117">El método **Item** se puede usar para recorrer en iteración todos los valores posibles del atributo Genre.</span><span class="sxs-lookup"><span data-stu-id="5a968-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="5a968-118">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5a968-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5a968-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5a968-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a968-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a968-120">Requirements</span></span>



| <span data-ttu-id="5a968-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a968-121">Requirement</span></span> | <span data-ttu-id="5a968-122">Value</span><span class="sxs-lookup"><span data-stu-id="5a968-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a968-123">Versión</span><span class="sxs-lookup"><span data-stu-id="5a968-123">Version</span></span><br/>   | <span data-ttu-id="5a968-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="5a968-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5a968-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a968-125">Namespace</span></span><br/> | <span data-ttu-id="5a968-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5a968-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5a968-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="5a968-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5a968-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5a968-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a968-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a968-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a968-130">**IWMPMediaCollection. getAttributeStringCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5a968-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5a968-131">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5a968-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5a968-132">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5a968-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5a968-133">**Interfaz IWMPStringCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5a968-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





