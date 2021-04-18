---
title: ErrorItem. errorCode
description: La propiedad errorCode recupera el código de error actual.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem. errorCode Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698630"
---
# <a name="erroritemerrorcode"></a><span data-ttu-id="4c680-104">ErrorItem. errorCode</span><span class="sxs-lookup"><span data-stu-id="4c680-104">ErrorItem.errorCode</span></span>

<span data-ttu-id="4c680-105">La propiedad **ErrorCode** recupera el código de error actual.</span><span class="sxs-lookup"><span data-stu-id="4c680-105">The **errorCode** property retrieves the current error code.</span></span>

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a><span data-ttu-id="4c680-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4c680-106">Possible Values</span></span>

<span data-ttu-id="4c680-107">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4c680-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c680-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c680-108">Remarks</span></span>

<span data-ttu-id="4c680-109">Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="4c680-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="4c680-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c680-110">Examples</span></span>

<span data-ttu-id="4c680-111">En el siguiente ejemplo de JScript se usa *ErrorItem*. **ErrorCode** en un controlador de eventos para mostrar el código de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="4c680-111">The following JScript example uses *ErrorItem*.**errorCode** in an event handler to display the error code to the user.</span></span> <span data-ttu-id="4c680-112">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4c680-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="4c680-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c680-113">Requirements</span></span>



| <span data-ttu-id="4c680-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c680-114">Requirement</span></span> | <span data-ttu-id="4c680-115">Value</span><span class="sxs-lookup"><span data-stu-id="4c680-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c680-116">Versión</span><span class="sxs-lookup"><span data-stu-id="4c680-116">Version</span></span><br/> | <span data-ttu-id="4c680-117">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4c680-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4c680-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c680-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c680-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c680-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c680-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c680-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c680-121">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="4c680-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="4c680-122">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="4c680-122">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> </dl>

 

 





