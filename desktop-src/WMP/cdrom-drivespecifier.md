---
title: CDROM. driveSpecifier
description: La propiedad driveSpecifier recupera la letra de unidad de CD o DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Media Player de Windows de CDROM. driveSpecifier
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533909"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="6a680-104">CDROM. driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="6a680-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="6a680-105">La propiedad **driveSpecifier** recupera la letra de unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="6a680-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="6a680-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6a680-106">Possible Values</span></span>

<span data-ttu-id="6a680-107">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6a680-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a680-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a680-108">Remarks</span></span>

<span data-ttu-id="6a680-109">Normalmente, las unidades de DVD pueden reproducir un CD, pero las unidades de CD no pueden reproducir medios de DVD.</span><span class="sxs-lookup"><span data-stu-id="6a680-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="6a680-110">Esta propiedad recupera un especificador de unidad para un índice de unidad de base cero dentro del intervalo recuperado mediante *CdromCollection*. **recuento**.</span><span class="sxs-lookup"><span data-stu-id="6a680-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="6a680-111">El valor recuperado toma la forma *x*:, donde *X* representa la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="6a680-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="6a680-112">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6a680-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="6a680-113">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6a680-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6a680-114">**Windows Media Player 10 Mobile:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="6a680-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6a680-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6a680-115">Examples</span></span>

<span data-ttu-id="6a680-116">En el siguiente ejemplo de JScript se usa el *CDROM*. **driveSpecifier** para rellenar un área de texto HTML denominada mi texto con una lista separada por comas de unidades de CD y DVD disponibles.</span><span class="sxs-lookup"><span data-stu-id="6a680-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="6a680-117">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6a680-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="6a680-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a680-118">Requirements</span></span>



| <span data-ttu-id="6a680-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a680-119">Requirement</span></span> | <span data-ttu-id="6a680-120">Value</span><span class="sxs-lookup"><span data-stu-id="6a680-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a680-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a680-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a680-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6a680-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a680-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a680-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a680-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a680-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a680-125">Versión</span><span class="sxs-lookup"><span data-stu-id="6a680-125">Version</span></span><br/>                  | <span data-ttu-id="6a680-126">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6a680-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="6a680-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a680-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a680-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a680-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a680-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a680-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a680-130">**CDROM (objeto)**</span><span class="sxs-lookup"><span data-stu-id="6a680-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="6a680-131">**CdromCollection. Count**</span><span class="sxs-lookup"><span data-stu-id="6a680-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="6a680-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6a680-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6a680-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6a680-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





