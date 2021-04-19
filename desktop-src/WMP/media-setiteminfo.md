---
title: Método media. setItemInfo
description: El método setItemInfo establece el valor del atributo especificado para el elemento multimedia actual.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699955"
---
# <a name="mediasetiteminfo-method"></a><span data-ttu-id="d068e-106">Método media. setItemInfo</span><span class="sxs-lookup"><span data-stu-id="d068e-106">Media.setItemInfo method</span></span>

<span data-ttu-id="d068e-107">El método **setItemInfo** establece el valor del atributo especificado para el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="d068e-107">The **setItemInfo** method sets the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="d068e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d068e-108">Syntax</span></span>


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="d068e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d068e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d068e-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d068e-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d068e-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="d068e-111">**String** containing the attribute name.</span></span> <span data-ttu-id="d068e-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d068e-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="d068e-113">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d068e-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d068e-114">**Cadena** que contiene el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="d068e-114">**String** containing the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d068e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d068e-115">Return value</span></span>

<span data-ttu-id="d068e-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d068e-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d068e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d068e-117">Remarks</span></span>

<span data-ttu-id="d068e-118">La propiedad **attributeCount** contiene el número de atributos disponibles para un objeto **multimedia** determinado.</span><span class="sxs-lookup"><span data-stu-id="d068e-118">The **attributeCount** property contains the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="d068e-119">Los números de índice se pueden usar con el método **getAttributeName** para determinar los nombres de los atributos integrados que se pueden usar con este método.</span><span class="sxs-lookup"><span data-stu-id="d068e-119">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="d068e-120">Antes de utilizar este método, utilice el método **isReadOnlyItem** para determinar si se puede establecer un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="d068e-120">Before using this method, use the **isReadOnlyItem** method to determine whether a particular attribute can be set.</span></span>

<span data-ttu-id="d068e-121">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d068e-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="d068e-122">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d068e-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d068e-123">**Note**</span><span class="sxs-lookup"><span data-stu-id="d068e-123">**Note**</span></span>

<span data-ttu-id="d068e-124">Si incrusta el control Media Player de Windows en la aplicación, los atributos de archivo que cambie no se escribirán en el archivo multimedia digital hasta que el usuario ejecute Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="d068e-124">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="d068e-125">Si utiliza el control en una aplicación remota escrita en C++, los atributos de archivo que cambie se escribirán en el archivo multimedia digital poco después de realizar los cambios.</span><span class="sxs-lookup"><span data-stu-id="d068e-125">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="d068e-126">En cualquier caso, los cambios están inmediatamente disponibles para el código a través de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d068e-126">In either case, the changes are immediately available to your code through the library.</span></span>

<span data-ttu-id="d068e-127">**Windows Media Player 10 Mobile:** Este método no está implementado.</span><span class="sxs-lookup"><span data-stu-id="d068e-127">**Windows Media Player 10 Mobile:** This method is not implemented.</span></span>

## <a name="examples"></a><span data-ttu-id="d068e-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d068e-128">Examples</span></span>

<span data-ttu-id="d068e-129">En el siguiente ejemplo de JScript se utiliza el *medio*. **setItemInfo** para cambiar el valor del atributo Genre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="d068e-129">The following JScript example uses *Media*.**setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="d068e-130">Un elemento de entrada de texto HTML denominado genText permite al usuario escribir una cadena de texto, que se usa para cambiar la información de atributo.</span><span class="sxs-lookup"><span data-stu-id="d068e-130">An HTML TEXT input element named genText allows the user to enter a text string, which is then used to change the attribute information.</span></span> <span data-ttu-id="d068e-131">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d068e-131">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a><span data-ttu-id="d068e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d068e-132">Requirements</span></span>



| <span data-ttu-id="d068e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d068e-133">Requirement</span></span> | <span data-ttu-id="d068e-134">Value</span><span class="sxs-lookup"><span data-stu-id="d068e-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d068e-135">Versión</span><span class="sxs-lookup"><span data-stu-id="d068e-135">Version</span></span><br/> | <span data-ttu-id="d068e-136">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d068e-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d068e-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d068e-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="d068e-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d068e-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d068e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d068e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d068e-140">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="d068e-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d068e-141">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="d068e-141">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="d068e-142">**Media. isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="d068e-142">**Media.isReadOnlyItem**</span></span>](media-isreadonlyitem.md)
</dt> <dt>

[<span data-ttu-id="d068e-143">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d068e-143">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d068e-144">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d068e-144">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





