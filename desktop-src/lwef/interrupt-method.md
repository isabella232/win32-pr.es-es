---
title: Método Interrupt
description: Método Interrupt
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420720"
---
# <a name="interrupt-method"></a><span data-ttu-id="6b69c-103">Método Interrupt</span><span class="sxs-lookup"><span data-stu-id="6b69c-103">Interrupt Method</span></span>

<span data-ttu-id="6b69c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6b69c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6b69c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="6b69c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6b69c-106">Interrumpe la animación del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="6b69c-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="6b69c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="6b69c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6b69c-108">\*agente ***. Caracteres ("*** CharacterID \* *").* \*  *Solicitud* de interrupción</span><span class="sxs-lookup"><span data-stu-id="6b69c-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="6b69c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6b69c-109">Part</span></span>      | <span data-ttu-id="6b69c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b69c-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="6b69c-111">*Solicitud*</span><span class="sxs-lookup"><span data-stu-id="6b69c-111">*Request*</span></span> | <span data-ttu-id="6b69c-112">Objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) para una llamada de animación determinada.</span><span class="sxs-lookup"><span data-stu-id="6b69c-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b69c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b69c-113">Remarks</span></span>

<span data-ttu-id="6b69c-114">Puede utilizar esto para sincronizar la animación entre los caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b69c-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="6b69c-115">Por ejemplo, si hay otro carácter en una animación de bucle, este método detendrá el bucle y se desplazará a la siguiente animación de la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="6b69c-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="6b69c-116">No se puede interrumpir una animación de caracteres que no se esté usando (que no se ha cargado).</span><span class="sxs-lookup"><span data-stu-id="6b69c-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="6b69c-117">Para especificar el parámetro de solicitud, debe crear una variable y asignar la solicitud de animación que desea interrumpir:</span><span class="sxs-lookup"><span data-stu-id="6b69c-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="6b69c-118">No se puede interrumpir la animación del mismo carácter que se especifica en este método porque el servidor pone en cola el método de **interrupción** en la cola de animaciones de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="6b69c-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="6b69c-119">Por lo tanto, solo puede usar la **interrupción** para detener la animación de otro carácter que haya cargado.</span><span class="sxs-lookup"><span data-stu-id="6b69c-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="6b69c-120">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="6b69c-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="6b69c-121">La **interrupción** no vacía la cola del carácter; detiene la animación existente y pasa a la siguiente animación de la cola del carácter.</span><span class="sxs-lookup"><span data-stu-id="6b69c-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="6b69c-122">Para detener y vaciar la cola de un carácter, utilice el método [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69c-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6b69c-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b69c-123">See Also</span></span>

[<span data-ttu-id="6b69c-124">**Método Stop**</span><span class="sxs-lookup"><span data-stu-id="6b69c-124">**Stop method**</span></span>](stop-method.md)


 

 