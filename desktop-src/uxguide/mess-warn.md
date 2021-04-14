---
title: Mensajes de advertencia
description: Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje en contexto, una notificación o un globo que alerta al usuario de una condición que puede provocar un problema en el futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361816"
---
# <a name="warning-messages"></a><span data-ttu-id="4b585-103">Mensajes de advertencia</span><span class="sxs-lookup"><span data-stu-id="4b585-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="4b585-104">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="4b585-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="4b585-105">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="4b585-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="4b585-106">Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje en contexto, una notificación o un globo que alerta al usuario de una condición que puede provocar un problema en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4b585-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![captura de pantalla de un mensaje de advertencia típico](images/mess-warn-image1.png)

<span data-ttu-id="4b585-108">Un mensaje de advertencia modal típico.</span><span class="sxs-lookup"><span data-stu-id="4b585-108">A typical modal warning message.</span></span>

<span data-ttu-id="4b585-109">La característica fundamental de las advertencias es que implican el riesgo de perder una o varias de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="4b585-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="4b585-110">Un activo valioso, como información financiera importante u otros datos.</span><span class="sxs-lookup"><span data-stu-id="4b585-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="4b585-111">Acceso al sistema o integridad.</span><span class="sxs-lookup"><span data-stu-id="4b585-111">System access or integrity.</span></span>
-   <span data-ttu-id="4b585-112">Privacidad o control sobre la información confidencial.</span><span class="sxs-lookup"><span data-stu-id="4b585-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="4b585-113">Hora del usuario (una cantidad significativa, como 30 segundos o más).</span><span class="sxs-lookup"><span data-stu-id="4b585-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="4b585-114">Por el contrario, una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción.</span><span class="sxs-lookup"><span data-stu-id="4b585-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="4b585-115">Algunos tipos de advertencias se presentan como confirmaciones y, si es así, también se aplican las directrices de confirmación.</span><span class="sxs-lookup"><span data-stu-id="4b585-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="4b585-116">**Nota:** Las instrucciones relacionadas con los [cuadros de diálogo](win-dialog-box.md), las [confirmaciones](mess-confirm.md), los [iconos estándar](vis-std-icons.md)de [los mensajes de error](mess-error.md), las [notificaciones](mess-notif.md)y el [diseño](vis-layout.md) se presentan en artículos independientes.</span><span class="sxs-lookup"><span data-stu-id="4b585-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="4b585-117">¿Es la interfaz de usuario correcta?</span><span class="sxs-lookup"><span data-stu-id="4b585-117">Is this the right user interface?</span></span>

<span data-ttu-id="4b585-118">Para decidirte, intenta responder a estas preguntas:</span><span class="sxs-lookup"><span data-stu-id="4b585-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="4b585-119">**¿El usuario recibe una alerta de una condición que puede provocar un problema en el futuro?**</span><span class="sxs-lookup"><span data-stu-id="4b585-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="4b585-120">Si no es así, el mensaje no es una advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="4b585-121">**¿La interfaz de usuario presenta un error o un problema que ya se ha producido?**</span><span class="sxs-lookup"><span data-stu-id="4b585-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="4b585-122">Si es así, use un mensaje de error en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4b585-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="4b585-123">**¿Es probable que los usuarios realicen una acción o cambien su comportamiento como resultado del mensaje?**</span><span class="sxs-lookup"><span data-stu-id="4b585-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="4b585-124">En caso contrario, la condición no justifica interrumpir al usuario, por lo que es mejor suprimir la advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="4b585-125">**¿Es la condición el resultado directo de una acción iniciada por el usuario?**</span><span class="sxs-lookup"><span data-stu-id="4b585-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="4b585-126">Si no es así, considere la posibilidad de usar [notificaciones de eventos no críticas](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="4b585-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="4b585-127">**¿Es la condición una condición especial en un control?**</span><span class="sxs-lookup"><span data-stu-id="4b585-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="4b585-128">Si es así, use un [globo](ctrl-balloons.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4b585-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="4b585-129">**En el caso de las confirmaciones, ¿el usuario está a punto de realizar una acción de riesgo?**</span><span class="sxs-lookup"><span data-stu-id="4b585-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="4b585-130">Si es así, una advertencia es adecuada si la acción tiene consecuencias importantes o no se puede deshacer fácilmente.</span><span class="sxs-lookup"><span data-stu-id="4b585-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="4b585-131">**Para otros tipos de advertencias, ¿el usuario tiene que actuar ahora o en el futuro inmediato?**</span><span class="sxs-lookup"><span data-stu-id="4b585-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="4b585-132">No muestre advertencias si los usuarios pueden seguir trabajando de manera productiva sin problemas inmediatos.</span><span class="sxs-lookup"><span data-stu-id="4b585-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="4b585-133">Posponer la advertencia hasta que la condición sea más inmediata y relevante.</span><span class="sxs-lookup"><span data-stu-id="4b585-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="4b585-134">Conceptos de diseño</span><span class="sxs-lookup"><span data-stu-id="4b585-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="4b585-135">Evitar las sobreadvertencias</span><span class="sxs-lookup"><span data-stu-id="4b585-135">Avoid overwarning</span></span>

<span data-ttu-id="4b585-136">Se recomienda que se avise en los programas de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4b585-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="4b585-137">El programa típico de Windows tiene advertencias aparentemente en todas partes, advertencia sobre cosas que tienen poca importancia.</span><span class="sxs-lookup"><span data-stu-id="4b585-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="4b585-138">En algunos programas, casi todas las preguntas se presentan como una advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="4b585-139">La sobreadvertencia hace que el uso de un programa se parezca a una actividad peligrosa y se reste de problemas realmente significativos.</span><span class="sxs-lookup"><span data-stu-id="4b585-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="4b585-140">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-140">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-141">captura de pantalla de un mensaje de advertencia innecesario</span><span class="sxs-lookup"><span data-stu-id="4b585-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="4b585-142">La sobreadvertencia hace que el programa se sienta peligroso y parezca que lo diseñó un abogados.</span><span class="sxs-lookup"><span data-stu-id="4b585-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="4b585-143">La mera posibilidad de pérdida de datos o un problema futuro por sí solo es insuficiente para llamar a una advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="4b585-144">Además, los resultados no deseados deberían ser inesperados o no deseados, y no se pueden corregir fácilmente.</span><span class="sxs-lookup"><span data-stu-id="4b585-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="4b585-145">De lo contrario, cualquier error de usuario podría interpretarse para producir la pérdida de datos o un posible problema de algún tipo y merecen una advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="4b585-146">Características de las buenas advertencias</span><span class="sxs-lookup"><span data-stu-id="4b585-146">Characteristics of good warnings</span></span>

<span data-ttu-id="4b585-147">Buenas advertencias:</span><span class="sxs-lookup"><span data-stu-id="4b585-147">Good warnings:</span></span>

-   <span data-ttu-id="4b585-148">**Implicar riesgo.**</span><span class="sxs-lookup"><span data-stu-id="4b585-148">**Involve risk.**</span></span> <span data-ttu-id="4b585-149">Las advertencias correctas alertan a los usuarios de algo importante.</span><span class="sxs-lookup"><span data-stu-id="4b585-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="4b585-150">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-150">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-151">captura de pantalla de "¿desea salir?"</span><span class="sxs-lookup"><span data-stu-id="4b585-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="4b585-152">warning</span><span class="sxs-lookup"><span data-stu-id="4b585-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="4b585-153">¿Y qué?</span><span class="sxs-lookup"><span data-stu-id="4b585-153">So what?</span></span> <span data-ttu-id="4b585-154">Esta confirmación supone que los usuarios suelen salir de los programas por accidente.</span><span class="sxs-lookup"><span data-stu-id="4b585-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="4b585-155">**Tienen relevancia inmediata.**</span><span class="sxs-lookup"><span data-stu-id="4b585-155">**Have immediate relevance.**</span></span> <span data-ttu-id="4b585-156">No solo los usuarios tienen que preocuparse, ya que tienen que preocuparse.</span><span class="sxs-lookup"><span data-stu-id="4b585-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="4b585-157">Normalmente, los usuarios no están interesados en los problemas que puedan tener más adelante, siempre y cuando puedan hacer su trabajo ahora.</span><span class="sxs-lookup"><span data-stu-id="4b585-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="4b585-158">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-158">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-159">captura de pantalla de una advertencia de batería baja en tres horas</span><span class="sxs-lookup"><span data-stu-id="4b585-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="4b585-160">En este caso, es mejor avisar al usuario en tres horas.</span><span class="sxs-lookup"><span data-stu-id="4b585-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="4b585-161">**Conducen a la acción.**</span><span class="sxs-lookup"><span data-stu-id="4b585-161">**Lead to action.**</span></span> <span data-ttu-id="4b585-162">Hay algo que los usuarios deben hacer o tener en cuenta como resultado de la advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="4b585-163">Quizás deban realizar una acción ahora o en algún momento en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4b585-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="4b585-164">Quizás realizarán una tarea de manera diferente como resultado.</span><span class="sxs-lookup"><span data-stu-id="4b585-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="4b585-165">La consecuencia de omitir la advertencia debe ser clara.</span><span class="sxs-lookup"><span data-stu-id="4b585-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="4b585-166">Las advertencias sin acciones solo hacen que los usuarios sientan Paranoid.</span><span class="sxs-lookup"><span data-stu-id="4b585-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="4b585-167">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-167">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-168">captura de pantalla de la advertencia "Live Messenger está en ejecución"</span><span class="sxs-lookup"><span data-stu-id="4b585-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="4b585-169">¿Por qué esta notificación es una advertencia?</span><span class="sxs-lookup"><span data-stu-id="4b585-169">Why is this notification a warning?</span></span> <span data-ttu-id="4b585-170">¿Qué se supone que deben hacer los usuarios (junto a preocuparse)?</span><span class="sxs-lookup"><span data-stu-id="4b585-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="4b585-171">**No son obvios.**</span><span class="sxs-lookup"><span data-stu-id="4b585-171">**Are not obvious.**</span></span> <span data-ttu-id="4b585-172">No muestre una advertencia para indicar la consecuencia obvia de una acción.</span><span class="sxs-lookup"><span data-stu-id="4b585-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="4b585-173">Por ejemplo, supongamos que los usuarios entienden las consecuencias de no completar una tarea.</span><span class="sxs-lookup"><span data-stu-id="4b585-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="4b585-174">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-174">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-175">captura de pantalla de ¿desea salir del asistente? atención</span><span class="sxs-lookup"><span data-stu-id="4b585-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="4b585-176">La cancelación de un asistente incompleto significa que la tarea no se realiza... ¿Quién sabía?</span><span class="sxs-lookup"><span data-stu-id="4b585-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="4b585-177">**Se producen con poca frecuencia.**</span><span class="sxs-lookup"><span data-stu-id="4b585-177">**Occur infrequently.**</span></span> <span data-ttu-id="4b585-178">Las advertencias constantes pasan a ser ineficaces y molestas.</span><span class="sxs-lookup"><span data-stu-id="4b585-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="4b585-179">A menudo, los usuarios se centran más en deshacerse de la advertencia que solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="4b585-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="4b585-180">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-180">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-181">captura de pantalla de la advertencia "actualizar firmas de virus"</span><span class="sxs-lookup"><span data-stu-id="4b585-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="4b585-182">Es más probable que los usuarios se centren en deshacerse de la advertencia que solucionar el problema subyacente.</span><span class="sxs-lookup"><span data-stu-id="4b585-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="4b585-183">Un mensaje que no tenga estas características puede seguir siendo un buen mensaje, no una buena advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="4b585-184">Determinar el tipo de mensaje adecuado</span><span class="sxs-lookup"><span data-stu-id="4b585-184">Determine the appropriate message type</span></span>

<span data-ttu-id="4b585-185">Algunos problemas se pueden presentar como un error, una advertencia o información, según el énfasis y la formulación.</span><span class="sxs-lookup"><span data-stu-id="4b585-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="4b585-186">Por ejemplo, supongamos que una página web no puede cargar un control ActiveX sin firmar basado en la configuración actual de Windows Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="4b585-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="4b585-187">**Error.**</span><span class="sxs-lookup"><span data-stu-id="4b585-187">**Error.**</span></span> <span data-ttu-id="4b585-188">"Esta página no puede cargar un control ActiveX sin firmar".</span><span class="sxs-lookup"><span data-stu-id="4b585-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="4b585-189">(Frase como un problema existente).</span><span class="sxs-lookup"><span data-stu-id="4b585-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="4b585-190">**Atención.**</span><span class="sxs-lookup"><span data-stu-id="4b585-190">**Warning.**</span></span> <span data-ttu-id="4b585-191">"Es posible que esta página no se comporte de la manera esperada porque Windows Internet Explorer no está configurado para cargar controles ActiveX sin firmar".</span><span class="sxs-lookup"><span data-stu-id="4b585-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="4b585-192">o "¿desea permitir que esta página Instale un control ActiveX sin firmar?</span><span class="sxs-lookup"><span data-stu-id="4b585-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="4b585-193">Hacerlo desde orígenes que no son de confianza puede dañar el equipo ".</span><span class="sxs-lookup"><span data-stu-id="4b585-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="4b585-194">(Ambas frases como condiciones que pueden causar problemas en el futuro).</span><span class="sxs-lookup"><span data-stu-id="4b585-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="4b585-195">**Informaciones.**</span><span class="sxs-lookup"><span data-stu-id="4b585-195">**Information.**</span></span> <span data-ttu-id="4b585-196">"Ha configurado Windows Internet Explorer para bloquear los controles ActiveX sin firmar".</span><span class="sxs-lookup"><span data-stu-id="4b585-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="4b585-197">(Frase como instrucción de hecho).</span><span class="sxs-lookup"><span data-stu-id="4b585-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="4b585-198">**Para determinar el tipo de mensaje adecuado, céntrese en el aspecto más importante del problema que los usuarios necesitan conocer o actuar sobre ellos.**</span><span class="sxs-lookup"><span data-stu-id="4b585-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="4b585-199">Normalmente, si un problema impide que el usuario continúe, debe presentarlo como un error. Si el usuario puede continuar, preséntela como advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="4b585-200">Cree la [instrucción principal](text-ui.md) u otro texto correspondiente en función de ese foco y, a continuación, elija un icono ([estándar](vis-std-icons.md) o de otro tipo) que coincida con el texto.</span><span class="sxs-lookup"><span data-stu-id="4b585-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="4b585-201">Los iconos y el texto de la instrucción principal siempre deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="4b585-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="4b585-202">Ser específico</span><span class="sxs-lookup"><span data-stu-id="4b585-202">Be specific</span></span>

<span data-ttu-id="4b585-203">Las advertencias son más atractivas cuando la siguiente información es específica y clara:</span><span class="sxs-lookup"><span data-stu-id="4b585-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="4b585-204">Origen de la advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-204">The source of the warning.</span></span>
-   <span data-ttu-id="4b585-205">La condición específica y el posible problema.</span><span class="sxs-lookup"><span data-stu-id="4b585-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="4b585-206">Lo que el usuario debe hacer sobre él.</span><span class="sxs-lookup"><span data-stu-id="4b585-206">What the user should do about it.</span></span>
-   <span data-ttu-id="4b585-207">Lo que sucede si el usuario no hace nada.</span><span class="sxs-lookup"><span data-stu-id="4b585-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="4b585-208">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-208">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-209">captura de pantalla de advertencia imprecisa de riesgo significativo</span><span class="sxs-lookup"><span data-stu-id="4b585-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="4b585-210">En este ejemplo, ¿cuál es el posible problema?</span><span class="sxs-lookup"><span data-stu-id="4b585-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="4b585-211">¿Qué debe hacer el usuario, aparte de no usar el proyector a través de la red?</span><span class="sxs-lookup"><span data-stu-id="4b585-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="4b585-212">Sin información más específica, todo lo que puede hacer el usuario es un inconveniente de continuar.</span><span class="sxs-lookup"><span data-stu-id="4b585-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="4b585-213">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-213">**Correct:**</span></span>

![<span data-ttu-id="4b585-214">captura de pantalla de la advertencia del problema y las consecuencias</span><span class="sxs-lookup"><span data-stu-id="4b585-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="4b585-215">En este ejemplo, el problema y las consecuencias son claros.</span><span class="sxs-lookup"><span data-stu-id="4b585-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="4b585-216">A veces hay un problema potencial legítimo que merece la información a los usuarios, pero la solución y las consecuencias no se conocen por seguridad.</span><span class="sxs-lookup"><span data-stu-id="4b585-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="4b585-217">En lugar de proporcionar una advertencia imprecisa, sea específico proporcionando la información más probable o el ejemplo más común.</span><span class="sxs-lookup"><span data-stu-id="4b585-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="4b585-218">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-218">**Correct:**</span></span>

![<span data-ttu-id="4b585-219">captura de pantalla de la advertencia y las soluciones de error de red</span><span class="sxs-lookup"><span data-stu-id="4b585-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="4b585-220">En este ejemplo, la advertencia se realiza de forma específica proporcionando la solución más probable.</span><span class="sxs-lookup"><span data-stu-id="4b585-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="4b585-221">Sin embargo, en estos casos, use el texto que indica que hay otras posibilidades.</span><span class="sxs-lookup"><span data-stu-id="4b585-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="4b585-222">De lo contrario, los usuarios podrían ser inducidos.</span><span class="sxs-lookup"><span data-stu-id="4b585-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="4b585-223">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-223">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-224">captura de pantalla de advertencia de cable de red desconectado</span><span class="sxs-lookup"><span data-stu-id="4b585-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="4b585-225">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-225">**Correct:**</span></span>

![<span data-ttu-id="4b585-226">la captura de pantalla de cable podría estar desconectada</span><span class="sxs-lookup"><span data-stu-id="4b585-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="4b585-227">En el ejemplo incorrecto, se confundirá a los usuarios si el cable está claramente enchufado.</span><span class="sxs-lookup"><span data-stu-id="4b585-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="4b585-228">**Si solo hace dos cosas...**</span><span class="sxs-lookup"><span data-stu-id="4b585-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="4b585-229">No lo advierta.</span><span class="sxs-lookup"><span data-stu-id="4b585-229">Don't overwarn.</span></span> <span data-ttu-id="4b585-230">Limite las advertencias a condiciones que impliquen un riesgo y que sean pertinentes, procesables, no obvios e infrecuentes.</span><span class="sxs-lookup"><span data-stu-id="4b585-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="4b585-231">De lo contrario, quite o vuelva a formular el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b585-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="4b585-232">Proporcionar información específica y útil.</span><span class="sxs-lookup"><span data-stu-id="4b585-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="4b585-233">Patrones de uso</span><span class="sxs-lookup"><span data-stu-id="4b585-233">Usage patterns</span></span>

<span data-ttu-id="4b585-234">Las advertencias tienen varios patrones de uso:</span><span class="sxs-lookup"><span data-stu-id="4b585-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b585-235"><strong>Reconocimiento</strong>:</span><span class="sxs-lookup"><span data-stu-id="4b585-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="4b585-236">Haga que el usuario tenga en cuenta una condición o posible problema, pero es posible que el usuario no tenga que hacer nada ahora.</span><span class="sxs-lookup"><span data-stu-id="4b585-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="4b585-237">Ejemplos de advertencias de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="4b585-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="4b585-238">Las advertencias de reconocimiento tienen la siguiente presentación:</span><span class="sxs-lookup"><span data-stu-id="4b585-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="4b585-239"><strong>Instrucción principal:</strong> Describir la condición o el posible problema.</span><span class="sxs-lookup"><span data-stu-id="4b585-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="4b585-240"><strong>Instrucción complementaria:</strong> Explique la implicación y el motivo por el que es importante.</span><span class="sxs-lookup"><span data-stu-id="4b585-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="4b585-241"><strong>Botones de confirmación:</strong> Cercanos.</span><span class="sxs-lookup"><span data-stu-id="4b585-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b585-242"><strong>Prevención de errores</strong></span><span class="sxs-lookup"><span data-stu-id="4b585-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="4b585-243">Haga que el usuario tenga en cuenta la información que puede impedir un problema, especialmente al tomar decisiones.</span><span class="sxs-lookup"><span data-stu-id="4b585-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="4b585-244">Las advertencias de prevención de errores se presentan mejor mediante un icono de advertencia en contexto y un texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="4b585-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="4b585-245">Ejemplos de advertencias de prevención de errores.</span><span class="sxs-lookup"><span data-stu-id="4b585-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b585-246"><strong>Problema inminente</strong></span><span class="sxs-lookup"><span data-stu-id="4b585-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="4b585-247">El usuario debe hacer algo ahora para evitar un problema inminente.</span><span class="sxs-lookup"><span data-stu-id="4b585-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="4b585-248">Un ejemplo de una advertencia inminente del problema.</span><span class="sxs-lookup"><span data-stu-id="4b585-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="4b585-249">Las advertencias de problemas inminentes tienen la siguiente presentación:</span><span class="sxs-lookup"><span data-stu-id="4b585-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="4b585-250"><strong>Instrucción principal:</strong> Describa lo que el usuario debe hacer ahora.</span><span class="sxs-lookup"><span data-stu-id="4b585-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="4b585-251"><strong>Instrucción complementaria:</strong> Explique la condición y por qué es importante.</span><span class="sxs-lookup"><span data-stu-id="4b585-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="4b585-252"><strong>Botones de confirmación:</strong> Un botón de comando o vínculo de comando para cada opción, o bien aceptar si la acción se produce fuera del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4b585-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b585-253"><strong>Confirmación de acción de riesgo</strong></span><span class="sxs-lookup"><span data-stu-id="4b585-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="4b585-254">Confirme que el usuario desea continuar con una acción que tiene cierto riesgo y no se puede deshacer fácilmente.</span><span class="sxs-lookup"><span data-stu-id="4b585-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="4b585-255">Ejemplo de confirmación de acción de riesgo.</span><span class="sxs-lookup"><span data-stu-id="4b585-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="4b585-256">Las confirmaciones de acción de riesgo tienen la siguiente presentación:</span><span class="sxs-lookup"><span data-stu-id="4b585-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="4b585-257"><strong>Instrucción principal:</strong> Formule una pregunta para determinar si el usuario desea continuar.</span><span class="sxs-lookup"><span data-stu-id="4b585-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="4b585-258"><strong>Instrucción complementaria:</strong> Explique las razones no obvias por las que el usuario podría no querer continuar.</span><span class="sxs-lookup"><span data-stu-id="4b585-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="4b585-259"><strong>Botones de confirmación:</strong> Sí, no.</span><span class="sxs-lookup"><span data-stu-id="4b585-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="4b585-260">Para obtener instrucciones sobre este patrón, consulte <a href="mess-confirm.md">confirmaciones</a>.</span><span class="sxs-lookup"><span data-stu-id="4b585-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="4b585-261">Directrices</span><span class="sxs-lookup"><span data-stu-id="4b585-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="4b585-262">Presentación</span><span class="sxs-lookup"><span data-stu-id="4b585-262">Presentation</span></span>

-   <span data-ttu-id="4b585-263">**Elija la interfaz de usuario de presentación según el tipo de información:**</span><span class="sxs-lookup"><span data-stu-id="4b585-263">**Choose the presentation UI based on the type of information:**</span></span>



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b585-264">**Interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="4b585-264">**User interface**</span></span><br/> | <span data-ttu-id="4b585-265">**Mejor uso para**</span><span class="sxs-lookup"><span data-stu-id="4b585-265">**Best used for**</span></span><br/>                                                                                                           |
| <span data-ttu-id="4b585-266">Cuadros de diálogo modales</span><span class="sxs-lookup"><span data-stu-id="4b585-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="4b585-267">ADVERTENCIAS críticas (incluidas las confirmaciones) a las que los usuarios deben responder ahora.</span><span class="sxs-lookup"><span data-stu-id="4b585-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="4b585-268">En contexto</span><span class="sxs-lookup"><span data-stu-id="4b585-268">In-place</span></span><br/>           | <span data-ttu-id="4b585-269">Información que podría impedir un problema, especialmente cuando los usuarios están realizando elecciones.</span><span class="sxs-lookup"><span data-stu-id="4b585-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="4b585-270">Banners</span><span class="sxs-lookup"><span data-stu-id="4b585-270">Banners</span></span><br/>            | <span data-ttu-id="4b585-271">Información que puede impedir un problema, especialmente cuando está relacionado con la finalización de una tarea.</span><span class="sxs-lookup"><span data-stu-id="4b585-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="4b585-272">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="4b585-272">Notifications</span></span><br/>      | <span data-ttu-id="4b585-273">Eventos o Estados significativos que se pueden omitir sin ningún riesgo, al menos temporalmente.</span><span class="sxs-lookup"><span data-stu-id="4b585-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="4b585-274">Globos</span><span class="sxs-lookup"><span data-stu-id="4b585-274">Balloons</span></span><br/>           | <span data-ttu-id="4b585-275">Un control está en un estado que afecta a la entrada.</span><span class="sxs-lookup"><span data-stu-id="4b585-275">A control is in a state that affects input.</span></span> <span data-ttu-id="4b585-276">Es probable que este estado no sea el deseado y que el usuario no se vea afectado.</span><span class="sxs-lookup"><span data-stu-id="4b585-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="4b585-277">**En los cuadros de diálogo modales:**</span><span class="sxs-lookup"><span data-stu-id="4b585-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="4b585-278">**Utilice los cuadros de diálogo de tareas siempre que sea necesario para lograr una apariencia y un diseño coherentes.**</span><span class="sxs-lookup"><span data-stu-id="4b585-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="4b585-279">Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="4b585-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="4b585-280">**Muestra solo un mensaje de advertencia por condición.**</span><span class="sxs-lookup"><span data-stu-id="4b585-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="4b585-281">Por ejemplo, se muestra una advertencia única que explica completamente una condición en lugar de describirla un detalle cada vez por mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b585-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="4b585-282">Mostrar una secuencia de cuadros de diálogo de advertencia para una única condición es confuso y molesto.</span><span class="sxs-lookup"><span data-stu-id="4b585-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="4b585-283">**No mostrar una advertencia más de una vez por condición.**</span><span class="sxs-lookup"><span data-stu-id="4b585-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="4b585-284">Las advertencias constantes pasan a ser ineficaces y molestas.</span><span class="sxs-lookup"><span data-stu-id="4b585-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="4b585-285">A menudo, los usuarios se centran más en deshacerse de la advertencia que solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="4b585-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="4b585-286">Si debe advertir repetidamente para una única condición, use la [extensión progresiva](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="4b585-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="4b585-287">**No acompañe las advertencias con un efecto o bip sonoros.**</span><span class="sxs-lookup"><span data-stu-id="4b585-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="4b585-288">Hacerlo es discordante e innecesario.</span><span class="sxs-lookup"><span data-stu-id="4b585-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="4b585-289">**Excepción:** Si el usuario debe responder inmediatamente, puede usar un efecto de sonido.</span><span class="sxs-lookup"><span data-stu-id="4b585-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="4b585-290">Iconos</span><span class="sxs-lookup"><span data-stu-id="4b585-290">Icons</span></span>

-   <span data-ttu-id="4b585-291">No coloque un icono de advertencia en la barra de título de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4b585-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="4b585-292">**Use un icono de advertencia.**</span><span class="sxs-lookup"><span data-stu-id="4b585-292">**Use a warning icon.**</span></span> <span data-ttu-id="4b585-293">Excepciones:</span><span class="sxs-lookup"><span data-stu-id="4b585-293">Exceptions:</span></span>
    -   <span data-ttu-id="4b585-294">Si la advertencia es para una característica que tiene un icono, puede usar el icono de la característica con una superposición de advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="4b585-295">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-295">**Correct:**</span></span>

        ![<span data-ttu-id="4b585-296">captura de pantalla del icono de candado con la superposición de icono de advertencia</span><span class="sxs-lookup"><span data-stu-id="4b585-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="4b585-297">En este ejemplo, el icono de característica tiene una superposición de advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="4b585-298">En el caso de los cuadros de diálogo modales con una nota al pie de la advertencia, coloque el icono de advertencia en la nota al pie en lugar del área de contenido.</span><span class="sxs-lookup"><span data-stu-id="4b585-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="4b585-299">**Correcto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-299">**Correct:**</span></span>

    ![<span data-ttu-id="4b585-300">captura de pantalla del icono de advertencia en la nota al pie del cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="4b585-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="4b585-301">En este ejemplo, la nota al pie tiene el icono de advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="4b585-302">Para obtener más instrucciones y ejemplos, vea [iconos estándar](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="4b585-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="4b585-303">No volver a mostrar este mensaje</span><span class="sxs-lookup"><span data-stu-id="4b585-303">Don't show this message again</span></span>

-   <span data-ttu-id="4b585-304">**Si un cuadro de diálogo de advertencia necesita esta opción, reconsidere la advertencia y su frecuencia.**</span><span class="sxs-lookup"><span data-stu-id="4b585-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="4b585-305">Si tiene todas las características de una buena advertencia (implica un riesgo y es inmediatamente pertinente, accionable, no obvia y poco frecuente), no debe tener sentido que los usuarios lo supriman.</span><span class="sxs-lookup"><span data-stu-id="4b585-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="4b585-306">Para obtener más instrucciones, consulte [cuadros de diálogo](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="4b585-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="4b585-307">Muestra progresiva</span><span class="sxs-lookup"><span data-stu-id="4b585-307">Progressive disclosure</span></span>

-   <span data-ttu-id="4b585-308">**Si tiene que incluir información avanzada en un mensaje de advertencia, debe revelarla mediante botones de divulgación progresiva** (por ejemplo, "Mostrar detalles").</span><span class="sxs-lookup"><span data-stu-id="4b585-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="4b585-309">De este modo, se simplifica la advertencia para el uso típico.</span><span class="sxs-lookup"><span data-stu-id="4b585-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="4b585-310">No oculte la información necesaria porque es posible que los usuarios no la encuentren.</span><span class="sxs-lookup"><span data-stu-id="4b585-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="4b585-311">**No use "Mostrar detalles" a menos que realmente haya más detalles.**</span><span class="sxs-lookup"><span data-stu-id="4b585-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="4b585-312">No solo tiene que volver a indicar la información existente en un formato diferente.</span><span class="sxs-lookup"><span data-stu-id="4b585-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="4b585-313">Para obtener instrucciones de etiquetado, vea [divulgación progresiva](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4b585-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="4b585-314">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="4b585-314">Default values</span></span>

-   <span data-ttu-id="4b585-315">**Seleccione la respuesta más segura, menos destructiva o más segura como predeterminada.**</span><span class="sxs-lookup"><span data-stu-id="4b585-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="4b585-316">Texto</span><span class="sxs-lookup"><span data-stu-id="4b585-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="4b585-317">General</span><span class="sxs-lookup"><span data-stu-id="4b585-317">General</span></span>

-   <span data-ttu-id="4b585-318">**Quite el texto redundante.**</span><span class="sxs-lookup"><span data-stu-id="4b585-318">**Remove redundant text.**</span></span> <span data-ttu-id="4b585-319">Busque en los títulos, las instrucciones principales, las instrucciones adicionales, las áreas de contenido, los vínculos de comandos y los botones de confirmación.</span><span class="sxs-lookup"><span data-stu-id="4b585-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="4b585-320">Por lo general, deje texto completo en las instrucciones y los controles interactivos, y quite cualquier redundancia de los demás lugares.</span><span class="sxs-lookup"><span data-stu-id="4b585-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="4b585-321">**No use los términos "ADVERTENCIA" o "PRECAUCIÓN" en el texto.**</span><span class="sxs-lookup"><span data-stu-id="4b585-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="4b585-322">Cuando se [usa correctamente](vis-std-icons.md), el icono de advertencia comunica de forma suficiente que los usuarios deben proseguir con precaución.</span><span class="sxs-lookup"><span data-stu-id="4b585-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="4b585-323">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-323">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-324">captura de pantalla del uso innecesario de advertencia en el texto</span><span class="sxs-lookup"><span data-stu-id="4b585-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="4b585-325">En este ejemplo, el término "WARNING" no es necesario.</span><span class="sxs-lookup"><span data-stu-id="4b585-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="4b585-326">Títulos</span><span class="sxs-lookup"><span data-stu-id="4b585-326">Titles</span></span>

-   <span data-ttu-id="4b585-327">**Use el título para identificar el comando o la característica de donde procede la advertencia.**</span><span class="sxs-lookup"><span data-stu-id="4b585-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="4b585-328">Excepciones:</span><span class="sxs-lookup"><span data-stu-id="4b585-328">Exceptions:</span></span>
    -   <span data-ttu-id="4b585-329">Si se muestra una advertencia en muchos comandos diferentes, considere la posibilidad de usar el nombre del programa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4b585-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="4b585-330">Si ese título sería redundante o confuso con la instrucción principal, use en su lugar el nombre del programa.</span><span class="sxs-lookup"><span data-stu-id="4b585-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="4b585-331">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-331">**Incorrect:**</span></span>

![<span data-ttu-id="4b585-332">captura de pantalla del título del cuadro de diálogo Advertencia de seguridad</span><span class="sxs-lookup"><span data-stu-id="4b585-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="4b585-333">En este ejemplo, "ADVERTENCIA de seguridad" no identifica el comando o la característica de la que procede la advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="4b585-334">**No use el título para explicar qué hacer en el cuadro de diálogo** que es el propósito de la instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="4b585-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="4b585-335">Usar [mayúsculas y minúsculas de estilo de título](glossary.md), sin puntuación final.</span><span class="sxs-lookup"><span data-stu-id="4b585-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="4b585-336">Instrucciones principales</span><span class="sxs-lookup"><span data-stu-id="4b585-336">Main instructions</span></span>

-   <span data-ttu-id="4b585-337">La instrucción principal de una advertencia se basa en su modelo de diseño:</span><span class="sxs-lookup"><span data-stu-id="4b585-337">The main instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="4b585-338">**Patrón**</span><span class="sxs-lookup"><span data-stu-id="4b585-338">**Pattern**</span></span><br/>               | <span data-ttu-id="4b585-339">**Instrucción principal**</span><span class="sxs-lookup"><span data-stu-id="4b585-339">**Main instruction**</span></span><br/>                                      |
| <span data-ttu-id="4b585-340">Concienciación</span><span class="sxs-lookup"><span data-stu-id="4b585-340">Awareness</span></span><br/>                 | <span data-ttu-id="4b585-341">Describir la condición o el posible problema.</span><span class="sxs-lookup"><span data-stu-id="4b585-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="4b585-342">Problema inminente</span><span class="sxs-lookup"><span data-stu-id="4b585-342">Imminent problem</span></span><br/>          | <span data-ttu-id="4b585-343">Describa lo que el usuario debe hacer ahora.</span><span class="sxs-lookup"><span data-stu-id="4b585-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="4b585-344">Confirmación de acción de riesgo</span><span class="sxs-lookup"><span data-stu-id="4b585-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="4b585-345">Formule una pregunta para determinar si el usuario desea continuar.</span><span class="sxs-lookup"><span data-stu-id="4b585-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="4b585-346">captura de pantalla de una notificación de batería baja</span><span class="sxs-lookup"><span data-stu-id="4b585-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="4b585-347">En este ejemplo, la notificación de batería baja es una advertencia de reconocimiento, por lo que la instrucción principal describe la condición.</span><span class="sxs-lookup"><span data-stu-id="4b585-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="4b585-348">captura de pantalla de la advertencia de cambio de batería inmediata</span><span class="sxs-lookup"><span data-stu-id="4b585-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="4b585-349">En este ejemplo, el cuadro de diálogo de batería baja es un problema inminente, por lo que la instrucción principal describe lo que el usuario debe hacer ahora.</span><span class="sxs-lookup"><span data-stu-id="4b585-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="4b585-350">**Sea conciso usar una sola oración completa.**</span><span class="sxs-lookup"><span data-stu-id="4b585-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="4b585-351">Quite la instrucción principal de la información esencial.</span><span class="sxs-lookup"><span data-stu-id="4b585-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="4b585-352">Si debe explicar algo más, use una instrucción complementaria.</span><span class="sxs-lookup"><span data-stu-id="4b585-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="4b585-353">**Use palabras como "ahora" y "inmediatamente" si el usuario debe actuar inmediatamente.**</span><span class="sxs-lookup"><span data-stu-id="4b585-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="4b585-354">No use estas palabras si no hay urgencia.</span><span class="sxs-lookup"><span data-stu-id="4b585-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="4b585-355">**Ser específico si hay objetos implicados, asigne sus nombres completos.**</span><span class="sxs-lookup"><span data-stu-id="4b585-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="4b585-356">Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4b585-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="4b585-357">Instrucciones complementarias</span><span class="sxs-lookup"><span data-stu-id="4b585-357">Supplemental instructions</span></span>

-   <span data-ttu-id="4b585-358">La instrucción complementaria para una advertencia se basa en su modelo de diseño:</span><span class="sxs-lookup"><span data-stu-id="4b585-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b585-359">**Patrón**</span><span class="sxs-lookup"><span data-stu-id="4b585-359">**Pattern**</span></span><br/>               | <span data-ttu-id="4b585-360">**Instrucción complementaria**</span><span class="sxs-lookup"><span data-stu-id="4b585-360">**Supplemental instruction**</span></span><br/>                                            |
| <span data-ttu-id="4b585-361">Concienciación</span><span class="sxs-lookup"><span data-stu-id="4b585-361">Awareness</span></span><br/>                 | <span data-ttu-id="4b585-362">Explique la implicación y el motivo por el que es importante.</span><span class="sxs-lookup"><span data-stu-id="4b585-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="4b585-363">Problema inminente</span><span class="sxs-lookup"><span data-stu-id="4b585-363">Imminent problem</span></span><br/>          | <span data-ttu-id="4b585-364">Explique la condición y por qué es importante.</span><span class="sxs-lookup"><span data-stu-id="4b585-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="4b585-365">Confirmación de acción de riesgo</span><span class="sxs-lookup"><span data-stu-id="4b585-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="4b585-366">Explique las razones no obvias por las que el usuario podría no querer continuar.</span><span class="sxs-lookup"><span data-stu-id="4b585-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="4b585-367">**No repita la instrucción principal con un texto ligeramente diferente.**</span><span class="sxs-lookup"><span data-stu-id="4b585-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="4b585-368">En su lugar, omita la instrucción complementaria Si no hay más que agregar.</span><span class="sxs-lookup"><span data-stu-id="4b585-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="4b585-369">Use frases completas, uso de mayúsculas y minúsculas y puntuación final.</span><span class="sxs-lookup"><span data-stu-id="4b585-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="4b585-370">Botones de confirmación</span><span class="sxs-lookup"><span data-stu-id="4b585-370">Commit buttons</span></span>

-   <span data-ttu-id="4b585-371">En el caso de los cuadros de diálogo de advertencia, los botones de confirmación se basan en su modelo de diseño:</span><span class="sxs-lookup"><span data-stu-id="4b585-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b585-372">**Patrón**</span><span class="sxs-lookup"><span data-stu-id="4b585-372">**Pattern**</span></span><br/>               | <span data-ttu-id="4b585-373">**Botones de confirmación**</span><span class="sxs-lookup"><span data-stu-id="4b585-373">**Commit buttons**</span></span><br/>                                                                                   |
| <span data-ttu-id="4b585-374">Concienciación</span><span class="sxs-lookup"><span data-stu-id="4b585-374">Awareness</span></span><br/>                 | <span data-ttu-id="4b585-375">Casi.</span><span class="sxs-lookup"><span data-stu-id="4b585-375">Close.</span></span> <span data-ttu-id="4b585-376">No use aceptar porque sugiere que los posibles problemas son correctos.</span><span class="sxs-lookup"><span data-stu-id="4b585-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="4b585-377">Problema inminente</span><span class="sxs-lookup"><span data-stu-id="4b585-377">Imminent problem</span></span><br/>          | <span data-ttu-id="4b585-378">Un botón de comando o vínculo de comando para cada opción, o bien aceptar si la acción se produce fuera del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4b585-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="4b585-379">Confirmación de acción de riesgo</span><span class="sxs-lookup"><span data-stu-id="4b585-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="4b585-380">Sí, no.</span><span class="sxs-lookup"><span data-stu-id="4b585-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="4b585-381">**Incorrecto:**</span><span class="sxs-lookup"><span data-stu-id="4b585-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="4b585-382">captura de pantalla del cuadro de diálogo de advertencia con el botón Aceptar</span><span class="sxs-lookup"><span data-stu-id="4b585-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="4b585-383">Los problemas no son correctos, por lo que debe usar cerrar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4b585-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="4b585-384">Documentación</span><span class="sxs-lookup"><span data-stu-id="4b585-384">Documentation</span></span>

<span data-ttu-id="4b585-385">Al hacer referencia a las advertencias:</span><span class="sxs-lookup"><span data-stu-id="4b585-385">When referring to warnings:</span></span>

-   <span data-ttu-id="4b585-386">Si la advertencia formula una pregunta, consulte una advertencia por su pregunta; de lo contrario, use la instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="4b585-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="4b585-387">Si la pregunta o instrucción principal es larga o detallada, resume.</span><span class="sxs-lookup"><span data-stu-id="4b585-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="4b585-388">Si es necesario, puede hacer referencia a un cuadro de diálogo de advertencia como mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b585-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="4b585-389">Siempre que sea posible, dé formato al texto con negrita.</span><span class="sxs-lookup"><span data-stu-id="4b585-389">When possible, format the text using bold.</span></span> <span data-ttu-id="4b585-390">De lo contrario, coloque el texto entre comillas solo si es necesario para evitar confusiones.</span><span class="sxs-lookup"><span data-stu-id="4b585-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="4b585-391">Ejemplo: en el mensaje **¿desea mostrar los elementos no seguros?** , haga clic en sí.</span><span class="sxs-lookup"><span data-stu-id="4b585-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

