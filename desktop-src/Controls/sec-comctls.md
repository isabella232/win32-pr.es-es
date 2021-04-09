---
title: Consideraciones de seguridad controles de Microsoft Windows
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con los controles de Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149703"
---
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="77d64-103">Consideraciones de seguridad: controles de Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="77d64-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="77d64-104">En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con los controles de Windows.</span><span class="sxs-lookup"><span data-stu-id="77d64-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="77d64-105">La información de este tema no proporciona todo lo que necesita saber acerca de los problemas de seguridad: Úselo como punto de partida y referencia para esta área tecnológica.</span><span class="sxs-lookup"><span data-stu-id="77d64-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="77d64-106">La interconectividad entre equipos es común; la principal preocupación del desarrollador debe ser la seguridad de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="77d64-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="77d64-107">En las secciones siguientes se describen algunos posibles problemas de seguridad que se deben tener en cuenta al programar controles de Windows.</span><span class="sxs-lookup"><span data-stu-id="77d64-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="77d64-108">Mensajes de control terminados en null</span><span class="sxs-lookup"><span data-stu-id="77d64-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="77d64-109">Uso de cadenas</span><span class="sxs-lookup"><span data-stu-id="77d64-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="77d64-110">Validación de entrada</span><span class="sxs-lookup"><span data-stu-id="77d64-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="77d64-111">Uso de contraseñas</span><span class="sxs-lookup"><span data-stu-id="77d64-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="77d64-112">alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="77d64-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="77d64-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77d64-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="77d64-114">Mensajes de control terminados en null</span><span class="sxs-lookup"><span data-stu-id="77d64-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="77d64-115">Muchos de los mensajes y macros de control tienen parámetros de cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="77d64-116">A menudo, estos mensajes no validan las cadenas de entrada, en particular, no comprueban si hay una terminación `'\0'` .</span><span class="sxs-lookup"><span data-stu-id="77d64-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="77d64-117">Cuando se llama a un mensaje que utiliza una cadena como parámetro, especifique explícitamente que la cadena termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="77d64-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="77d64-118">Uso de cadenas</span><span class="sxs-lookup"><span data-stu-id="77d64-118">String Use</span></span>

<span data-ttu-id="77d64-119">Cuando se programan controles de Windows, es necesario manipular cadenas.</span><span class="sxs-lookup"><span data-stu-id="77d64-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="77d64-120">Casi todos los controles requieren que se inserte texto.</span><span class="sxs-lookup"><span data-stu-id="77d64-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="77d64-121">Por ejemplo, para rellenar un cuadro de lista, debe cargar las cadenas en el control.</span><span class="sxs-lookup"><span data-stu-id="77d64-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="77d64-122">Dado que el uso incorrecto de cadenas suele provocar saturaciones de búfer, tome precauciones para evitar este riesgo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77d64-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="77d64-123">Para obtener más información sobre las saturaciones del búfer, vea *escribir código seguro* de Michael Howard y David LeBlanc, Microsoft Press, 2002 y [prácticas recomendadas para las API de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="77d64-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="77d64-124">Validación de entrada</span><span class="sxs-lookup"><span data-stu-id="77d64-124">Input Validation</span></span>

<span data-ttu-id="77d64-125">Los siguientes mensajes de control pueden presentar problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77d64-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="77d64-126">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="77d64-127">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="77d64-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="77d64-128">**GETTEXT de SB \_**</span><span class="sxs-lookup"><span data-stu-id="77d64-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="77d64-129">**SB \_ GETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="77d64-130">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="77d64-131">**TTM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="77d64-132">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="77d64-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="77d64-133">Si el texto cambia entre la llamada para obtener la longitud del texto y la hora en que se muestra o se usa el texto, se puede producir una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="77d64-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="77d64-134">Para evitar esto, debe validar la cadena antes de usarla.</span><span class="sxs-lookup"><span data-stu-id="77d64-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="77d64-135">Además, los mensajes que recuperan Text, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)y [**TTM \_ GETTEXT**](ttm-gettext.md), no tienen ningún parámetro de tamaño de búfer que presente el potencial de una saturación del búfer.</span><span class="sxs-lookup"><span data-stu-id="77d64-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="77d64-136">Cuando use [**CB \_ GETLBTEXT**](cb-getlbtext.md) o [**SB \_ GETTEXT**](sb-gettext.md), primero debe llamar a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) o [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="77d64-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="77d64-137">Algunos de estos mensajes, [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)y [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md), se pueden llamar con un valor de parámetro **null** para obtener la longitud de la cadena antes de invocar el mensaje para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="77d64-138">Un mensaje que debe prestar especial atención a es el mensaje de [**\_ GETTIPTEXT de SB**](sb-gettiptext.md) de la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="77d64-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="77d64-139">Este mensaje no proporciona ninguna manera de consultar la longitud de la cadena que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="77d64-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="77d64-140">Uso de contraseñas</span><span class="sxs-lookup"><span data-stu-id="77d64-140">Password Use</span></span>

<span data-ttu-id="77d64-141">Si usa controles de edición protegidos con contraseña ([**es \_**](edit-control-styles.md) decir, el estilo de contraseña), el búfer que contiene el texto recuperado debe establecerse en cero lo antes posible para evitar exponer la contraseña del usuario en la memoria.</span><span class="sxs-lookup"><span data-stu-id="77d64-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="77d64-142">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="77d64-142">Security Alerts</span></span>

<span data-ttu-id="77d64-143">En la tabla siguiente se enumeran las características que, si se usan incorrectamente, pueden poner en peligro la seguridad de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="77d64-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="77d64-144">Los mensajes que se enumeran aquí no proporcionan un parámetro que especifique el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="77d64-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="77d64-145">Característica</span><span class="sxs-lookup"><span data-stu-id="77d64-145">Feature</span></span>                                               | <span data-ttu-id="77d64-146">Mitigación</span><span class="sxs-lookup"><span data-stu-id="77d64-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d64-147">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="77d64-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="77d64-148">Asegúrese de que se puede escribir en el búfer usado por la función y que está terminado en NULL.</span><span class="sxs-lookup"><span data-stu-id="77d64-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="77d64-149">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="77d64-150">Llame a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obtener el tamaño del búfer y, a continuación, llame a [**CB \_ GETLBTEXT**](cb-getlbtext.md) para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="77d64-151">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="77d64-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="77d64-152">Llame al mensaje con un valor de parámetro **null** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="77d64-153">**GETTEXT de SB \_**</span><span class="sxs-lookup"><span data-stu-id="77d64-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="77d64-154">Llame a [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el tamaño del búfer y, a continuación, llame a la [**\_ GETTEXT de SB**](sb-gettext.md) para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="77d64-155">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="77d64-156">Llame al mensaje con un valor de parámetro **null** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="77d64-157">**TTM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="77d64-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="77d64-158">Este mensaje no proporciona una manera de conocer o especificar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="77d64-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="77d64-159">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="77d64-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="77d64-160">Llame al mensaje pasando un valor de parámetro **null** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.</span><span class="sxs-lookup"><span data-stu-id="77d64-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="77d64-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77d64-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="77d64-162">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="77d64-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="77d64-163">Seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="77d64-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="77d64-164">Seguridad</span><span class="sxs-lookup"><span data-stu-id="77d64-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="77d64-165">Recursos de seguridad de TechNet</span><span class="sxs-lookup"><span data-stu-id="77d64-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="77d64-166">Prácticas recomendadas para las API de seguridad</span><span class="sxs-lookup"><span data-stu-id="77d64-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 