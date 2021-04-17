---
title: ErrorItem. errorDescription
description: La propiedad errorDescription recupera una descripción del error.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem. errorDescription Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698628"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="9aebc-104">ErrorItem. errorDescription</span><span class="sxs-lookup"><span data-stu-id="9aebc-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="9aebc-105">La propiedad **errorDescription** recupera una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="9aebc-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="9aebc-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="9aebc-106">Possible Values</span></span>

<span data-ttu-id="9aebc-107">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9aebc-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aebc-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9aebc-108">Remarks</span></span>

<span data-ttu-id="9aebc-109">Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="9aebc-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="9aebc-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9aebc-110">Examples</span></span>

<span data-ttu-id="9aebc-111">En el siguiente ejemplo de JScript se usa *ErrorItem*. **errorDescription** en un controlador de eventos para mostrar el mensaje de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="9aebc-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="9aebc-112">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9aebc-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="9aebc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aebc-113">Requirements</span></span>



| <span data-ttu-id="9aebc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aebc-114">Requirement</span></span> | <span data-ttu-id="9aebc-115">Value</span><span class="sxs-lookup"><span data-stu-id="9aebc-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9aebc-116">Versión</span><span class="sxs-lookup"><span data-stu-id="9aebc-116">Version</span></span><br/> | <span data-ttu-id="9aebc-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9aebc-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="9aebc-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9aebc-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="9aebc-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aebc-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aebc-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aebc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aebc-121">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="9aebc-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





