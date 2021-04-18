---
title: Player. error (evento)
description: El evento de error se produce cuando hay una condición de error.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Evento de error de Windows Media Player
- Evento de error Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento de error
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708964"
---
# <a name="playererror-event"></a><span data-ttu-id="c3617-106">Player. error (evento)</span><span class="sxs-lookup"><span data-stu-id="c3617-106">Player.Error event</span></span>

<span data-ttu-id="c3617-107">El evento de **error** se produce cuando hay una condición de error.</span><span class="sxs-lookup"><span data-stu-id="c3617-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3617-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3617-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="c3617-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3617-109">Parameters</span></span>

<span data-ttu-id="c3617-110">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c3617-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3617-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3617-111">Return value</span></span>

<span data-ttu-id="c3617-112">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c3617-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c3617-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c3617-113">Examples</span></span>

<span data-ttu-id="c3617-114">En el siguiente ejemplo de JScript se crea un controlador de eventos para mostrar el texto de Descripción del primer error en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="c3617-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="c3617-115">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c3617-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c3617-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3617-116">Requirements</span></span>



| <span data-ttu-id="c3617-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3617-117">Requirement</span></span> | <span data-ttu-id="c3617-118">Value</span><span class="sxs-lookup"><span data-stu-id="c3617-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3617-119">Versión</span><span class="sxs-lookup"><span data-stu-id="c3617-119">Version</span></span><br/> | <span data-ttu-id="c3617-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c3617-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c3617-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3617-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3617-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3617-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3617-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3617-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3617-124">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="c3617-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="c3617-125">**Error. Item**</span><span class="sxs-lookup"><span data-stu-id="c3617-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="c3617-126">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="c3617-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





