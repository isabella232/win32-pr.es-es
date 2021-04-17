---
description: La Acción ValidateProductID establece la propiedad ProductID en el identificador de producto completo.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Acción ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652460"
---
# <a name="validateproductid-action"></a><span data-ttu-id="f2da9-103">Acción ValidateProductID</span><span class="sxs-lookup"><span data-stu-id="f2da9-103">ValidateProductID Action</span></span>

<span data-ttu-id="f2da9-104">La Acción ValidateProductID establece la propiedad [**ProductID**](productid.md) en el identificador de producto completo.</span><span class="sxs-lookup"><span data-stu-id="f2da9-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f2da9-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="f2da9-105">Sequence Restrictions</span></span>

<span data-ttu-id="f2da9-106">Esta acción se debe secuenciar antes del Asistente para la interfaz de usuario en la [tabla InstallUISequence](installuisequence-table.md) y antes de la [acción RegisterUser](registeruser-action.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2da9-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f2da9-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="f2da9-107">ActionData Messages</span></span>

<span data-ttu-id="f2da9-108">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="f2da9-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2da9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2da9-109">Remarks</span></span>

<span data-ttu-id="f2da9-110">El instalador comprueba si un producto se ha validado correctamente mediante la comprobación de la propiedad [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="f2da9-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="f2da9-111">El instalador establece la propiedad **ProductID** en el identificador de producto completo después de una validación correcta.</span><span class="sxs-lookup"><span data-stu-id="f2da9-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="f2da9-112">La Acción ValidateProductID no hace nada si la propiedad **ProductID** ya se ha establecido mediante una validación correcta u otro método.</span><span class="sxs-lookup"><span data-stu-id="f2da9-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="f2da9-113">La Acción ValidateProductID siempre devuelve un resultado correcto, tanto si el identificador de producto es válido como si no, para que el identificador de producto se pueda escribir en la línea de comandos la primera vez que se ejecute el producto.</span><span class="sxs-lookup"><span data-stu-id="f2da9-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="f2da9-114">El identificador de producto se puede validar sin que el usuario vuelva a escribir esta información estableciendo la propiedad [**PIDKEY**](pidkey.md) en la línea de comandos o mediante una transformación.</span><span class="sxs-lookup"><span data-stu-id="f2da9-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="f2da9-115">La presentación del cuadro de diálogo que solicita al usuario que escriba el identificador de producto se puede hacer condicional según la presencia de la propiedad [**ProductID**](productid.md) , que se establece cuando se valida la propiedad **PIDKEY** .</span><span class="sxs-lookup"><span data-stu-id="f2da9-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



