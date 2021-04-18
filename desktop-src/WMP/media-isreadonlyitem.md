---
title: Método media. isReadOnlyItem
description: El método isReadOnlyItem devuelve un valor que indica si se puede editar el atributo especificado del elemento multimedia.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- método isReadOnlyItem de Windows Media Player
- método isReadOnlyItem Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698470"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="f18c7-106">Método media. isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="f18c7-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="f18c7-107">El método **isReadOnlyItem** devuelve un valor que indica si se puede editar el atributo especificado del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="f18c7-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f18c7-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="f18c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f18c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18c7-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f18c7-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18c7-111">**Cadena** que indica el nombre del atributo que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="f18c7-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="f18c7-112">Para obtener información acerca de los atributos que admite Windows Media Player, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f18c7-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18c7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f18c7-113">Return value</span></span>

<span data-ttu-id="f18c7-114">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="f18c7-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f18c7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f18c7-115">Remarks</span></span>

<span data-ttu-id="f18c7-116">Si un atributo es de solo lectura, no se puede establecer con el método **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="f18c7-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="f18c7-117">Tenga en cuenta que este método puede devolver valores diferentes para un atributo determinado cuando se usa con versiones diferentes de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f18c7-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="f18c7-118">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f18c7-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f18c7-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f18c7-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f18c7-120">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="f18c7-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="f18c7-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f18c7-121">Examples</span></span>

<span data-ttu-id="f18c7-122">En el siguiente ejemplo de JScript se utiliza el *medio*. **isReadOnlyItem** para rellenar un elemento TEXTAREA HTML denominado rwText con información sobre el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="f18c7-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="f18c7-123">El código genera cada atributo del elemento multimedia actual, junto con el texto que indica si el atributo es de solo lectura o de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f18c7-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="f18c7-124">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f18c7-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="f18c7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f18c7-125">Requirements</span></span>



| <span data-ttu-id="f18c7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f18c7-126">Requirement</span></span> | <span data-ttu-id="f18c7-127">Value</span><span class="sxs-lookup"><span data-stu-id="f18c7-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f18c7-128">Versión</span><span class="sxs-lookup"><span data-stu-id="f18c7-128">Version</span></span><br/> | <span data-ttu-id="f18c7-129">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f18c7-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f18c7-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f18c7-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="f18c7-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f18c7-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18c7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f18c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18c7-133">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="f18c7-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f18c7-134">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="f18c7-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="f18c7-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f18c7-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f18c7-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f18c7-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





