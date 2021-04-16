---
title: Método media. isIdentical
description: El método isIdentical recupera un valor que indica si el objeto proporcionado es igual que el actual. | Método media. isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- método isIdentical de Windows Media Player
- método isIdentical Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método isIdentical
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699816"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="9855a-107">Método media. isIdentical</span><span class="sxs-lookup"><span data-stu-id="9855a-107">Media.isIdentical method</span></span>

<span data-ttu-id="9855a-108">El método **isIdentical** recupera un valor que indica si el objeto proporcionado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="9855a-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="9855a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9855a-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="9855a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9855a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9855a-111">*medios* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9855a-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9855a-112">Objeto **multimedia** que se va a comparar con el objeto **multimedia** actual.</span><span class="sxs-lookup"><span data-stu-id="9855a-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9855a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9855a-113">Return value</span></span>

<span data-ttu-id="9855a-114">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="9855a-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="9855a-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9855a-115">Examples</span></span>

<span data-ttu-id="9855a-116">En el siguiente ejemplo de JScript se utiliza el *medio*. **isIdentical** para comprobar si un elemento multimedia con el nombre newMedia es el mismo que el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="9855a-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="9855a-117">Si no son iguales, se reproduce el nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="9855a-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="9855a-118">De lo contrario, el medio actual sigue reproduciéndose sin interrupciones.</span><span class="sxs-lookup"><span data-stu-id="9855a-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="9855a-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9855a-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="9855a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9855a-120">Requirements</span></span>



| <span data-ttu-id="9855a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9855a-121">Requirement</span></span> | <span data-ttu-id="9855a-122">Value</span><span class="sxs-lookup"><span data-stu-id="9855a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9855a-123">Versión</span><span class="sxs-lookup"><span data-stu-id="9855a-123">Version</span></span><br/> | <span data-ttu-id="9855a-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9855a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9855a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9855a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9855a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9855a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9855a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9855a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9855a-128">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="9855a-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





