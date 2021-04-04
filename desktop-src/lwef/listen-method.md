---
title: Listen (método)
description: Listen (método)
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077623"
---
# <a name="listen-method"></a><span data-ttu-id="09016-103">Listen (método)</span><span class="sxs-lookup"><span data-stu-id="09016-103">Listen Method</span></span>

<span data-ttu-id="09016-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09016-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="09016-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="09016-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="09016-106">Activa el modo de escucha (reconocimiento de voz) durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="09016-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="09016-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="09016-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="09016-108">\*agente. ***Caracteres \* \* \* \* ("*** CharacterID \* \* *").* \*  *Estado* de escucha</span><span class="sxs-lookup"><span data-stu-id="09016-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="09016-109">Parte</span><span class="sxs-lookup"><span data-stu-id="09016-109">Part</span></span>    | <span data-ttu-id="09016-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="09016-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09016-111">*Estado*</span><span class="sxs-lookup"><span data-stu-id="09016-111">*State*</span></span> | <span data-ttu-id="09016-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09016-112">Required.</span></span> <span data-ttu-id="09016-113">Valor booleano que determina si se activa o desactiva el modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="09016-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="09016-114">**True** Activa el modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="09016-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="09016-115">**False** Desactiva el modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="09016-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09016-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09016-116">Remarks</span></span>

<span data-ttu-id="09016-117">Al establecer este método en **true** , se habilita el modo de escucha (activa el reconocimiento de voz) durante un período de tiempo fijo (10 segundos).</span><span class="sxs-lookup"><span data-stu-id="09016-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="09016-118">Aunque no se puede establecer el valor del tiempo de espera, puede desactivar el modo de escucha antes de que expire el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="09016-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="09016-119">Si usted (u otro cliente) establece correctamente el modo de escucha en e intenta establecer esta propiedad en **true** antes de que expire el tiempo de espera, el método se ejecuta correctamente y restablece el tiempo de espera. Sin embargo, si el modo de escucha está activado porque el usuario está presionando la clave de escucha, el método se ejecuta correctamente, pero se omite el tiempo de espera y el modo de escucha finaliza en función de la interacción del usuario con la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="09016-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="09016-120">Este método solo se realiza correctamente cuando lo llama el cliente de entrada-activo y si se han iniciado los servicios de voz.</span><span class="sxs-lookup"><span data-stu-id="09016-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="09016-121">Para asegurarse de que se han iniciado los servicios de voz, consulte o establezca el valor de [**SRModeID**](srmodeid-property.md) o establezca la configuración de [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object) antes de llamar a **Listen** ; de lo contrario, se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="09016-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="09016-122">Para detectar el éxito de este método, llámelo como una función y devolverá un valor booleano que indica si el método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="09016-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="09016-123">También se produce un error en el método si el usuario presiona la tecla de escucha e intenta establecer **Listen** en **false**.</span><span class="sxs-lookup"><span data-stu-id="09016-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="09016-124">Sin embargo, si el usuario ha liberado la clave de escucha y el modo de escucha no ha agotado el tiempo de espera, se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="09016-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="09016-125">La **escucha** también produce un error si no hay ningún motor de voz compatible disponible que coincida con la configuración de [**LanguageID**](languageid-property.md) del carácter, el usuario ha deshabilitado la entrada de voz mediante la hoja de propiedades del agente de Microsoft o el dispositivo de audio está ocupado.</span><span class="sxs-lookup"><span data-stu-id="09016-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="09016-126">Cuando se establece correctamente este método en **true**, el servidor desencadena el evento [**ListenStart**](listenstart-event.md) .</span><span class="sxs-lookup"><span data-stu-id="09016-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="09016-127">El servidor envía [**ListenComplete**](listencomplete-event.md) cuando se completa el tiempo de espera de modo de escucha o cuando se establece la **escucha** en **false**.</span><span class="sxs-lookup"><span data-stu-id="09016-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="09016-128">Este método no llama automáticamente a [**detener**](stop-method.md) y reproducir una animación de estado de escucha como el servidor cuando se presiona la tecla de escucha.</span><span class="sxs-lookup"><span data-stu-id="09016-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="09016-129">Esto le permite determinar si desea interrumpir la animación actual mediante la animación [**ListenStart**](listenstart-event.md) llamando a **Stop** y reproduciendo su propia animación adecuada.</span><span class="sxs-lookup"><span data-stu-id="09016-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="09016-130">Sin embargo, el servidor llama a **Stop** y reproduce una animación de estado de audición cuando se detecta un utterance de usuario.</span><span class="sxs-lookup"><span data-stu-id="09016-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="09016-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="09016-131">See Also</span></span>

<span data-ttu-id="09016-132">[**Propiedad LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="09016-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

