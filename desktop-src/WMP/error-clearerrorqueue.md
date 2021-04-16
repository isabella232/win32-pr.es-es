---
title: Error. clearErrorQueue (método)
description: El método clearErrorQueue borra los errores de la cola de errores. | Error. clearErrorQueue (método)
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- método clearErrorQueue de Windows Media Player
- método clearErrorQueue Windows Media Player, clase error
- Clase de error Windows Media Player, método clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699589"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="f9920-107">Error. clearErrorQueue (método)</span><span class="sxs-lookup"><span data-stu-id="f9920-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="f9920-108">El método **clearErrorQueue** borra los errores de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="f9920-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9920-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9920-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="f9920-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9920-110">Parameters</span></span>

<span data-ttu-id="f9920-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f9920-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9920-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9920-112">Return value</span></span>

<span data-ttu-id="f9920-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f9920-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9920-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9920-114">Remarks</span></span>

<span data-ttu-id="f9920-115">Este método es útil para borrar la cola de errores después de haber procesado una serie de errores.</span><span class="sxs-lookup"><span data-stu-id="f9920-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="f9920-116">Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="f9920-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="f9920-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f9920-117">Examples</span></span>

<span data-ttu-id="f9920-118">En el siguiente ejemplo de JScript se utiliza el *error*. **clearErrorQueue** en un controlador de eventos para vaciar la cola de errores después de que se muestren todas las descripciones de errores.</span><span class="sxs-lookup"><span data-stu-id="f9920-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="f9920-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f9920-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="f9920-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9920-120">Requirements</span></span>



| <span data-ttu-id="f9920-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9920-121">Requirement</span></span> | <span data-ttu-id="f9920-122">Value</span><span class="sxs-lookup"><span data-stu-id="f9920-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9920-123">Versión</span><span class="sxs-lookup"><span data-stu-id="f9920-123">Version</span></span><br/> | <span data-ttu-id="f9920-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f9920-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f9920-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9920-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9920-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9920-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9920-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9920-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9920-128">**Objeto de error**</span><span class="sxs-lookup"><span data-stu-id="f9920-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





