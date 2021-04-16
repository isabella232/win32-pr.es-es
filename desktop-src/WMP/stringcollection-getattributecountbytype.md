---
title: StringCollection. getAttributeCountByType (método)
description: El método getAttributeCountByType recupera el número de atributos asociados con el índice del elemento StringCollection, el nombre de atributo y el idioma especificados.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718783"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="aa871-106">StringCollection. getAttributeCountByType (método)</span><span class="sxs-lookup"><span data-stu-id="aa871-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="aa871-107">El método **getAttributeCountByType** recupera el número de atributos asociados con el índice del elemento **StringCollection** , el nombre de atributo y el idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="aa871-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa871-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa871-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="aa871-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa871-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa871-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="aa871-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa871-111">**Número** (**Long**) que especifica el índice de base cero del elemento **StringCollection** del que se va a obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="aa871-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="aa871-112">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="aa871-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa871-113">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="aa871-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="aa871-114">*idioma* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="aa871-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa871-115">**Cadena** que contiene el idioma.</span><span class="sxs-lookup"><span data-stu-id="aa871-115">**String** containing the language.</span></span> <span data-ttu-id="aa871-116">Si el valor se establece en null o en una cadena vacía (""), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="aa871-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="aa871-117">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="aa871-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa871-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa871-118">Return value</span></span>

<span data-ttu-id="aa871-119">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="aa871-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa871-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa871-120">Remarks</span></span>

<span data-ttu-id="aa871-121">Este método se utiliza para determinar el número de atributos correspondientes a un nombre de atributo determinado para un elemento **StringCollection** determinado.</span><span class="sxs-lookup"><span data-stu-id="aa871-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="aa871-122">Los números de índice se pueden pasar al cuarto parámetro del método **StringCollection. getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="aa871-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="aa871-123">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="aa871-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="aa871-124">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="aa871-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa871-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa871-125">Requirements</span></span>



| <span data-ttu-id="aa871-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa871-126">Requirement</span></span> | <span data-ttu-id="aa871-127">Value</span><span class="sxs-lookup"><span data-stu-id="aa871-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa871-128">Versión</span><span class="sxs-lookup"><span data-stu-id="aa871-128">Version</span></span><br/> | <span data-ttu-id="aa871-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="aa871-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="aa871-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa871-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa871-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa871-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa871-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa871-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa871-133">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="aa871-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





