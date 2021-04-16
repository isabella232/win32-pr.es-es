---
title: IWMPStringCollection2 getAttributeCountByType, método
description: El método getAttributeCountByType devuelve el número de atributos asociados al índice de la colección de cadenas, el nombre de atributo y el idioma especificados.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709116"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="3fdfb-106">IWMPStringCollection2:: getAttributeCountByType (método)</span><span class="sxs-lookup"><span data-stu-id="3fdfb-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="3fdfb-107">El método **getAttributeCountByType** devuelve el número de atributos asociados al índice de la colección de cadenas, el nombre de atributo y el idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fdfb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fdfb-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="3fdfb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fdfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fdfb-110">*lCollectionIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fdfb-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fdfb-111">**System. Int32** que especifica el índice de base cero del elemento de colección de cadenas del que se va a obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3fdfb-112">*bstrType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fdfb-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fdfb-113">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3fdfb-114">*bstrLanguage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fdfb-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fdfb-115">**System. String** que es el nombre del idioma.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="3fdfb-116">Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="3fdfb-117">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="3fdfb-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fdfb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fdfb-118">Return value</span></span>

<span data-ttu-id="3fdfb-119">**System. Int32** que es el recuento.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fdfb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fdfb-120">Remarks</span></span>

<span data-ttu-id="3fdfb-121">Este método se utiliza para detectar el número de atributos correspondientes a un nombre de atributo determinado para un elemento **StringCollection** determinado.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="3fdfb-122">Los números de índice se pueden pasar al cuarto parámetro del método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="3fdfb-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="3fdfb-123">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3fdfb-124">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3fdfb-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fdfb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fdfb-125">Requirements</span></span>



| <span data-ttu-id="3fdfb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fdfb-126">Requirement</span></span> | <span data-ttu-id="3fdfb-127">Value</span><span class="sxs-lookup"><span data-stu-id="3fdfb-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdfb-128">Versión</span><span class="sxs-lookup"><span data-stu-id="3fdfb-128">Version</span></span><br/>   | <span data-ttu-id="3fdfb-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3fdfb-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="3fdfb-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fdfb-130">Namespace</span></span><br/> | <span data-ttu-id="3fdfb-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3fdfb-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3fdfb-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3fdfb-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3fdfb-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3fdfb-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fdfb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fdfb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fdfb-135">**Interfaz IWMPStringCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3fdfb-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3fdfb-136">**IWMPStringCollection2. getItemInfoByType (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3fdfb-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





