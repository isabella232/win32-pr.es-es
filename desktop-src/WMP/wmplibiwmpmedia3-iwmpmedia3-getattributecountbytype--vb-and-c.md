---
title: IWMPMedia3 getAttributeCountByType, método
description: El método getAttributeCountByType devuelve el número de atributos asociados al tipo de atributo especificado.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, interfaz IWMPMedia3
- Interfaz IWMPMedia3 Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670364"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="c1a6d-106">IWMPMedia3:: getAttributeCountByType (método)</span><span class="sxs-lookup"><span data-stu-id="c1a6d-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="c1a6d-107">El método **getAttributeCountByType** devuelve el número de atributos asociados al tipo de atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a6d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1a6d-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="c1a6d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1a6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a6d-110">*bstrType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1a6d-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a6d-111">**System. String** que es el tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="c1a6d-112">*bstrLanguage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1a6d-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a6d-113">**System. String** que es el idioma.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-113">A **System.String** that is the language.</span></span> <span data-ttu-id="c1a6d-114">Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="c1a6d-115">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="c1a6d-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a6d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1a6d-116">Return value</span></span>

<span data-ttu-id="c1a6d-117">**System. Int32** que es el recuento de atributos asociados al tipo.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a6d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1a6d-118">Remarks</span></span>

<span data-ttu-id="c1a6d-119">Este método se utiliza para detectar el número de atributos correspondientes a un nombre de atributo determinado para un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="c1a6d-120">Después, los números de índice se pueden pasar al método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="c1a6d-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="c1a6d-121">Esto resulta útil, por ejemplo, cuando un elemento multimedia se ha clasificado en varios géneros.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="c1a6d-122">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c1a6d-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c1a6d-123">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c1a6d-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a6d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1a6d-124">Requirements</span></span>



| <span data-ttu-id="c1a6d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1a6d-125">Requirement</span></span> | <span data-ttu-id="c1a6d-126">Value</span><span class="sxs-lookup"><span data-stu-id="c1a6d-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a6d-127">Versión</span><span class="sxs-lookup"><span data-stu-id="c1a6d-127">Version</span></span><br/>   | <span data-ttu-id="c1a6d-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c1a6d-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c1a6d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1a6d-129">Namespace</span></span><br/> | <span data-ttu-id="c1a6d-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c1a6d-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c1a6d-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c1a6d-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c1a6d-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c1a6d-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a6d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1a6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a6d-134">**Interfaz IWMPMedia3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1a6d-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1a6d-135">**IWMPMedia3. getItemInfoByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1a6d-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





