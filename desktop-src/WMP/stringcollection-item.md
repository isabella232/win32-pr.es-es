---
title: StringCollection. Item (método)
description: El método Item recupera la cadena en el índice especificado.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718625"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="e99e4-106">StringCollection. Item (método)</span><span class="sxs-lookup"><span data-stu-id="e99e4-106">StringCollection.item method</span></span>

<span data-ttu-id="e99e4-107">El método **Item** recupera la cadena en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="e99e4-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99e4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e99e4-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e99e4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e99e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99e4-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e99e4-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e4-111">**Número** (**largo**) que contiene el índice.</span><span class="sxs-lookup"><span data-stu-id="e99e4-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99e4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e99e4-112">Return value</span></span>

<span data-ttu-id="e99e4-113">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="e99e4-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e99e4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e99e4-114">Remarks</span></span>

<span data-ttu-id="e99e4-115">El objeto **StringCollection** se utiliza para recuperar el conjunto de valores disponibles para un atributo.</span><span class="sxs-lookup"><span data-stu-id="e99e4-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="e99e4-116">Por ejemplo, *MediaCollection*. el método **getAttributeStringCollection** se puede utilizar para recuperar un objeto **StringCollection** que representa todos los valores del atributo Genre en el tipo de medios de audio.</span><span class="sxs-lookup"><span data-stu-id="e99e4-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="e99e4-117">La propiedad **Item** se puede usar para recorrer en iteración todos los valores posibles del atributo Genre.</span><span class="sxs-lookup"><span data-stu-id="e99e4-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="e99e4-118">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e99e4-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e99e4-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e99e4-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e99e4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e99e4-120">Requirements</span></span>



| <span data-ttu-id="e99e4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e99e4-121">Requirement</span></span> | <span data-ttu-id="e99e4-122">Value</span><span class="sxs-lookup"><span data-stu-id="e99e4-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e99e4-123">Versión</span><span class="sxs-lookup"><span data-stu-id="e99e4-123">Version</span></span><br/> | <span data-ttu-id="e99e4-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e99e4-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e99e4-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e99e4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="e99e4-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e99e4-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e99e4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e99e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99e4-128">**MediaCollection.getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="e99e4-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="e99e4-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e99e4-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e99e4-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e99e4-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e99e4-131">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="e99e4-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





