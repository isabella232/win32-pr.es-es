---
title: Error. errorCount
description: La propiedad errorCount recupera el número de errores en la cola de errores.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Error. errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698609"
---
# <a name="errorerrorcount"></a><span data-ttu-id="f1b5a-104">Error. errorCount</span><span class="sxs-lookup"><span data-stu-id="f1b5a-104">Error.errorCount</span></span>

<span data-ttu-id="f1b5a-105">La propiedad **errorCount** recupera el número de errores en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="f1b5a-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="f1b5a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f1b5a-106">Possible Values</span></span>

<span data-ttu-id="f1b5a-107">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="f1b5a-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b5a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1b5a-108">Remarks</span></span>

<span data-ttu-id="f1b5a-109">Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="f1b5a-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="f1b5a-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f1b5a-110">Examples</span></span>

<span data-ttu-id="f1b5a-111">En el siguiente ejemplo de JScript se utiliza el *error*. **errorCount** en un controlador de eventos para avisar al usuario sobre el error más reciente en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="f1b5a-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="f1b5a-112">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f1b5a-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="f1b5a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b5a-113">Requirements</span></span>



| <span data-ttu-id="f1b5a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b5a-114">Requirement</span></span> | <span data-ttu-id="f1b5a-115">Value</span><span class="sxs-lookup"><span data-stu-id="f1b5a-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b5a-116">Versión</span><span class="sxs-lookup"><span data-stu-id="f1b5a-116">Version</span></span><br/> | <span data-ttu-id="f1b5a-117">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f1b5a-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f1b5a-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1b5a-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1b5a-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1b5a-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b5a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1b5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b5a-121">**Objeto de error**</span><span class="sxs-lookup"><span data-stu-id="f1b5a-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





