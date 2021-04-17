---
title: Método Activate
description: Método Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695580"
---
# <a name="activate-method"></a><span data-ttu-id="d8be2-103">Método Activate</span><span class="sxs-lookup"><span data-stu-id="d8be2-103">Activate Method</span></span>

<span data-ttu-id="d8be2-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8be2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d8be2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Denominación**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="d8be2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="d8be2-106">Establece el cliente activo o el carácter.</span><span class="sxs-lookup"><span data-stu-id="d8be2-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="d8be2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="d8be2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d8be2-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Activar* \*  \[ *Estado*\]</span><span class="sxs-lookup"><span data-stu-id="d8be2-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="d8be2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d8be2-109">Part</span></span>    | <span data-ttu-id="d8be2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8be2-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8be2-111">*Estado*</span><span class="sxs-lookup"><span data-stu-id="d8be2-111">*State*</span></span> | <span data-ttu-id="d8be2-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d8be2-112">Optional.</span></span> <span data-ttu-id="d8be2-113">Puede especificar los siguientes valores para este parámetro: 0 no es el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="d8be2-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="d8be2-114">1 el cliente activo.</span><span class="sxs-lookup"><span data-stu-id="d8be2-114">1 The active client.</span></span> <br/> <span data-ttu-id="d8be2-115">2 (valor predeterminado) el carácter superior.</span><span class="sxs-lookup"><span data-stu-id="d8be2-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8be2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8be2-116">Remarks</span></span>

<span data-ttu-id="d8be2-117">Cuando hay varios caracteres visibles, solo uno de los caracteres recibe la entrada de voz a la vez.</span><span class="sxs-lookup"><span data-stu-id="d8be2-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="d8be2-118">Del mismo modo, cuando varias aplicaciones cliente comparten el mismo carácter, solo uno de los clientes recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft).</span><span class="sxs-lookup"><span data-stu-id="d8be2-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="d8be2-119">El juego de caracteres para recibir la entrada de mouse y voz es el carácter más alto y el cliente que recibe la entrada es el cliente activo de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="d8be2-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="d8be2-120">(La ventana del carácter superior también aparece en la parte superior del orden z de la ventana de caracteres). Normalmente, el usuario determina el carácter superior seleccionando explícitamente el carácter.</span><span class="sxs-lookup"><span data-stu-id="d8be2-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="d8be2-121">Sin embargo, la activación de nivel superior también cambia cuando se muestra o se oculta un carácter (el carácter se vuelve o ya no es más alto, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="d8be2-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="d8be2-122">También puede usar este método para administrar explícitamente cuando el cliente recibe entradas dirigidas al carácter como cuando la propia aplicación se activa.</span><span class="sxs-lookup"><span data-stu-id="d8be2-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="d8be2-123">Por ejemplo, establecer el *Estado* en 2 hace que el carácter sea más alto y el cliente recibe todos los eventos de entrada de voz y del mouse generados a partir de la interacción del usuario con el carácter.</span><span class="sxs-lookup"><span data-stu-id="d8be2-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="d8be2-124">Por lo tanto, también convierte al cliente en el cliente de entrada y activo del carácter.</span><span class="sxs-lookup"><span data-stu-id="d8be2-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="d8be2-125">Sin embargo, también puede establecer que sea el cliente activo para un carácter sin que el carácter sea más alto, estableciendo el *Estado* en 1.</span><span class="sxs-lookup"><span data-stu-id="d8be2-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="d8be2-126">Esto permite que el cliente reciba entradas dirigidas a ese carácter cuando el carácter se vuelve más alto.</span><span class="sxs-lookup"><span data-stu-id="d8be2-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="d8be2-127">Del mismo modo, puede configurar el cliente para que no sea el cliente activo (no para recibir la entrada) cuando el carácter se convierta en el nivel más alto, estableciendo el *Estado* en 0.</span><span class="sxs-lookup"><span data-stu-id="d8be2-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="d8be2-128">Evite llamar a este método directamente después de un método [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) .</span><span class="sxs-lookup"><span data-stu-id="d8be2-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="d8be2-129">**Mostrar** establece automáticamente el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="d8be2-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="d8be2-130">Cuando se oculta el carácter, se puede producir un error en la llamada a [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) si se procesa antes de que se complete el método **Show** .</span><span class="sxs-lookup"><span data-stu-id="d8be2-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="d8be2-131">Si llama a este método para una función, devuelve un valor booleano que indica si el método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8be2-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="d8be2-132">Se producirá un error al intentar llamar a este método con el parámetro de *Estado* establecido en 2 cuando se oculte el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="d8be2-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="d8be2-133">De forma similar, si establece *State* en 0 y la aplicación es el único cliente, se produce un error en esta llamada porque un carácter debe tener siempre un cliente superior.</span><span class="sxs-lookup"><span data-stu-id="d8be2-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="d8be2-134">La llamada a este método con el *Estado* establecido en 1 no genera normalmente un evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) a menos que no se cargue ningún otro carácter o que la aplicación ya sea de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="d8be2-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d8be2-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8be2-135">See Also</span></span>

<span data-ttu-id="d8be2-136">[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="d8be2-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 

