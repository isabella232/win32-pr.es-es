---
title: CdromCollection. Count
description: La propiedad Count recupera el número de unidades de CD y DVD disponibles en el sistema.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection. Count Windows Media Player
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700315"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="e465a-104">CdromCollection. Count</span><span class="sxs-lookup"><span data-stu-id="e465a-104">CdromCollection.count</span></span>

<span data-ttu-id="e465a-105">La propiedad **Count** recupera el número de unidades de CD y DVD disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e465a-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="e465a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e465a-106">Possible Values</span></span>

<span data-ttu-id="e465a-107">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e465a-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e465a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e465a-108">Remarks</span></span>

<span data-ttu-id="e465a-109">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e465a-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="e465a-110">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e465a-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e465a-111">Las unidades de DVD-ROM se cuentan exactamente como las unidades de CD.</span><span class="sxs-lookup"><span data-stu-id="e465a-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="e465a-112">Sin embargo, el control Media Player de Windows solo admite la funcionalidad de DVD para Windows XP o sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="e465a-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="e465a-113">Normalmente, las unidades de DVD pueden reproducir un CD, pero las unidades de CD no pueden reproducir medios de DVD.</span><span class="sxs-lookup"><span data-stu-id="e465a-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="e465a-114">**Windows Media Player 10 Mobile:** Este método siempre devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="e465a-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="e465a-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e465a-115">Examples</span></span>

<span data-ttu-id="e465a-116">En el siguiente ejemplo de JScript se usa *CdromCollection*. **recuento** para mostrar el número de unidades de CD y DVD disponibles en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e465a-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="e465a-117">El objeto Player se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e465a-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="e465a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e465a-118">Requirements</span></span>



| <span data-ttu-id="e465a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e465a-119">Requirement</span></span> | <span data-ttu-id="e465a-120">Value</span><span class="sxs-lookup"><span data-stu-id="e465a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e465a-121">Versión</span><span class="sxs-lookup"><span data-stu-id="e465a-121">Version</span></span><br/> | <span data-ttu-id="e465a-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e465a-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="e465a-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e465a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e465a-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e465a-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e465a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e465a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e465a-126">**Objeto CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="e465a-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="e465a-127">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e465a-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e465a-128">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e465a-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





