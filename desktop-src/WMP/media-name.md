---
title: Media.name
description: La propiedad Name especifica o recupera el nombre del elemento multimedia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699814"
---
# <a name="medianame"></a><span data-ttu-id="01794-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="01794-104">Media.name</span></span>

<span data-ttu-id="01794-105">La propiedad **Name** especifica o recupera el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="01794-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="01794-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01794-106">Syntax</span></span>

<span data-ttu-id="01794-107">*reproductor*. *currentMedia*. **nombre** de</span><span class="sxs-lookup"><span data-stu-id="01794-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="01794-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="01794-108">Possible Values</span></span>

<span data-ttu-id="01794-109">Esta propiedad es una **cadena** de lectura/escritura que contiene el nombre del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="01794-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="01794-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01794-110">Remarks</span></span>

<span data-ttu-id="01794-111">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="01794-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="01794-112">Para especificar el valor de esta propiedad, se requiere acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="01794-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="01794-113">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="01794-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="01794-114">Antes de utilizar este método para especificar el nombre de un elemento multimedia, use **isReadOnlyItem** para determinar si se puede establecer el nombre.</span><span class="sxs-lookup"><span data-stu-id="01794-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="01794-115">**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01794-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="01794-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="01794-116">Examples</span></span>

<span data-ttu-id="01794-117">En el siguiente ejemplo de JScript se utiliza el *medio*. **nombre** para cambiar el nombre del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="01794-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="01794-118">Un elemento de entrada de texto HTML denominado NameText permite al usuario escribir una cadena de texto para el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="01794-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="01794-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="01794-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="01794-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01794-120">Requirements</span></span>



| <span data-ttu-id="01794-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="01794-121">Requirement</span></span> | <span data-ttu-id="01794-122">Value</span><span class="sxs-lookup"><span data-stu-id="01794-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01794-123">Versión</span><span class="sxs-lookup"><span data-stu-id="01794-123">Version</span></span><br/> | <span data-ttu-id="01794-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="01794-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="01794-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01794-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="01794-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01794-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01794-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="01794-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01794-128">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="01794-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="01794-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="01794-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="01794-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="01794-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





