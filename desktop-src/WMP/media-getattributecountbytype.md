---
title: Método media. getAttributeCountByType
description: El método getAttributeCountByType recupera el número de atributos asociados al nombre de atributo y el idioma especificados.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- método getAttributeCountByType de Windows Media Player
- método getAttributeCountByType Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700237"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="f3edb-106">Método media. getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="f3edb-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="f3edb-107">El método **getAttributeCountByType** recupera el número de atributos asociados al nombre de atributo y el idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="f3edb-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3edb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3edb-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="f3edb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3edb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3edb-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f3edb-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3edb-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="f3edb-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="f3edb-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f3edb-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3edb-113">*idioma* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f3edb-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3edb-114">**Cadena** que representa el idioma.</span><span class="sxs-lookup"><span data-stu-id="f3edb-114">**String** representing the language.</span></span> <span data-ttu-id="f3edb-115">Si el valor se establece en null o en "" (cadena vacía), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="f3edb-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="f3edb-116">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="f3edb-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3edb-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3edb-117">Return value</span></span>

<span data-ttu-id="f3edb-118">Este método devuelve un **número** (**Long**) que contiene el número de atributos.</span><span class="sxs-lookup"><span data-stu-id="f3edb-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3edb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3edb-119">Remarks</span></span>

<span data-ttu-id="f3edb-120">Este método se utiliza para determinar el número de atributos correspondientes a un nombre de atributo determinado para un objeto **multimedia** determinado.</span><span class="sxs-lookup"><span data-stu-id="f3edb-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="f3edb-121">Después, los números de índice se pueden pasar al método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="f3edb-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="f3edb-122">Esto resulta útil, por ejemplo, cuando un elemento multimedia se ha clasificado en varios géneros.</span><span class="sxs-lookup"><span data-stu-id="f3edb-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="f3edb-123">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f3edb-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f3edb-124">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f3edb-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f3edb-125">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="f3edb-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3edb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3edb-126">Requirements</span></span>



| <span data-ttu-id="f3edb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3edb-127">Requirement</span></span> | <span data-ttu-id="f3edb-128">Value</span><span class="sxs-lookup"><span data-stu-id="f3edb-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3edb-129">Versión</span><span class="sxs-lookup"><span data-stu-id="f3edb-129">Version</span></span><br/> | <span data-ttu-id="f3edb-130">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="f3edb-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f3edb-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3edb-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3edb-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3edb-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3edb-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3edb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3edb-134">**MediaObject**</span><span class="sxs-lookup"><span data-stu-id="f3edb-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f3edb-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="f3edb-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="f3edb-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f3edb-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f3edb-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f3edb-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





