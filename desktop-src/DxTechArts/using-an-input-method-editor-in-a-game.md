---
title: Usar un editor de métodos de entrada en un juego
description: En este artículo se explica cómo implementar un control de edición de IME básico en una aplicación de Microsoft DirectX de pantalla completa.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119c5933aae14e2d3e45085dafa241a4dcb11e1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118680"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="67f61-103">Usar un editor de métodos de entrada en un juego</span><span class="sxs-lookup"><span data-stu-id="67f61-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="67f61-104">En este artículo se detalla cómo trabajar con el Editor de métodos de entrada (IME) de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="67f61-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="67f61-105">Se realizaron cambios en el IME para Windows Vista que no se detallan completamente en este artículo.</span><span class="sxs-lookup"><span data-stu-id="67f61-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="67f61-106">Para obtener más información sobre los cambios en el IME para Windows Vista, vea Editores de métodos de entrada [(IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) en [Windows Vista:](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) una vista Ever-Expanding de internacionalización en el Portal de desarrollo e informática global de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67f61-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="67f61-107">Un editor de métodos de entrada (IME) es un programa que permite una entrada de texto sencilla mediante un teclado estándar para idiomas de Asia Oriental, como chino, japonés, coreano y otros idiomas con caracteres complejos.</span><span class="sxs-lookup"><span data-stu-id="67f61-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="67f61-108">Por ejemplo, con imes, un usuario puede escribir caracteres complejos en un procesador de palabras o un jugador de un juego en línea multijugador masivo puede chatear con amigos en caracteres complejos.</span><span class="sxs-lookup"><span data-stu-id="67f61-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="67f61-109">En este artículo se explica cómo implementar un control de edición de IME básico en una aplicación de Microsoft DirectX de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="67f61-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="67f61-110">Las aplicaciones que aprovechan DXUT obtienen automáticamente la funcionalidad IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="67f61-111">En el caso de las aplicaciones que no usan el marco de trabajo, en este artículo se describe cómo agregar compatibilidad con IME a un control de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="67f61-112">Contenido:</span><span class="sxs-lookup"><span data-stu-id="67f61-112">Contents:</span></span>

-   [<span data-ttu-id="67f61-113">Comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="67f61-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="67f61-114">Uso de IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="67f61-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="67f61-115">Invalidar el comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="67f61-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="67f61-116">Funciones</span><span class="sxs-lookup"><span data-stu-id="67f61-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="67f61-117">Mensajes</span><span class="sxs-lookup"><span data-stu-id="67f61-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="67f61-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="67f61-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="67f61-119">CHT IME versión 4.2, 4.3 y 4.4</span><span class="sxs-lookup"><span data-stu-id="67f61-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="67f61-120">CHT IME versión 5.0</span><span class="sxs-lookup"><span data-stu-id="67f61-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="67f61-121">CHT IME versión 5.1, 5.2 y CHS IME versión 5.3</span><span class="sxs-lookup"><span data-stu-id="67f61-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="67f61-122">CHS IME versión 4.1</span><span class="sxs-lookup"><span data-stu-id="67f61-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="67f61-123">CHS IME versión 4.2</span><span class="sxs-lookup"><span data-stu-id="67f61-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="67f61-124">Mensajes IME</span><span class="sxs-lookup"><span data-stu-id="67f61-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="67f61-125">WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="67f61-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="67f61-126">WM \_ IME \_ STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="67f61-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="67f61-127">WM \_ IME \_ COMPOSITION</span><span class="sxs-lookup"><span data-stu-id="67f61-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="67f61-128">WM \_ IME \_ ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="67f61-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="67f61-129">WM \_ IME \_ NOTIFY</span><span class="sxs-lookup"><span data-stu-id="67f61-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="67f61-130">Representación</span><span class="sxs-lookup"><span data-stu-id="67f61-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="67f61-131">Indicador de configuración regional de entrada</span><span class="sxs-lookup"><span data-stu-id="67f61-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="67f61-132">Ventana Composición</span><span class="sxs-lookup"><span data-stu-id="67f61-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="67f61-133">Ventanas de lectura y candidatas</span><span class="sxs-lookup"><span data-stu-id="67f61-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="67f61-134">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="67f61-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="67f61-135">Información del Registro</span><span class="sxs-lookup"><span data-stu-id="67f61-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="67f61-136">Apéndice A: Versiones de CHT por sistema operativo</span><span class="sxs-lookup"><span data-stu-id="67f61-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="67f61-137">Información adicional</span><span class="sxs-lookup"><span data-stu-id="67f61-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="67f61-138">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="67f61-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="67f61-139">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="67f61-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="67f61-140">Comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="67f61-140">Default IME Behavior</span></span>

<span data-ttu-id="67f61-141">Los IME asignan la entrada de teclado a componentes fonéticos u otros elementos de lenguaje específicos de un idioma seleccionado.</span><span class="sxs-lookup"><span data-stu-id="67f61-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="67f61-142">En un escenario típico, el usuario tipos claves que representan la pronunciación de un carácter complejo.</span><span class="sxs-lookup"><span data-stu-id="67f61-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="67f61-143">Si el IME reconoce la pronunciación como válida, presenta al usuario una lista de candidatos de palabras o frases entre las que el usuario puede seleccionar una opción final.</span><span class="sxs-lookup"><span data-stu-id="67f61-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="67f61-144">A continuación, la palabra elegida se envía a la aplicación a través de una serie de mensajes [**WM \_ CHAR de**](/windows/desktop/inputdev/wm-char) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="67f61-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="67f61-145">Dado que el IME funciona en un nivel por debajo de la aplicación mediante la interceptación de la entrada de teclado, la presencia de un IME es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67f61-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="67f61-146">Casi todas las aplicaciones de Windows pueden aprovechar fácilmente las ventajas de los EME sin tener en cuenta su existencia y sin necesidad de codificación especial.</span><span class="sxs-lookup"><span data-stu-id="67f61-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="67f61-147">Un IME típico muestra varias ventanas para guiar al usuario a través de la entrada de caracteres, como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="67f61-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![ime muestra varias ventanas](images/ime-elements.png)

| <span data-ttu-id="67f61-149">Tipo de ventana</span><span class="sxs-lookup"><span data-stu-id="67f61-149">Window Type</span></span>                                       | <span data-ttu-id="67f61-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f61-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="67f61-151">Salida de IME</span><span class="sxs-lookup"><span data-stu-id="67f61-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="67f61-152">A.</span><span class="sxs-lookup"><span data-stu-id="67f61-152">A.</span></span> <span data-ttu-id="67f61-153">Ventana de lectura</span><span class="sxs-lookup"><span data-stu-id="67f61-153">Reading Window</span></span>                                 | <span data-ttu-id="67f61-154">Contiene pulsaciones de tecla del teclado; normalmente cambia después de cada pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="67f61-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="67f61-155">cadena de lectura</span><span class="sxs-lookup"><span data-stu-id="67f61-155">reading string</span></span>                               |
| <span data-ttu-id="67f61-156">B.</span><span class="sxs-lookup"><span data-stu-id="67f61-156">B.</span></span> <span data-ttu-id="67f61-157">Ventana Composición</span><span class="sxs-lookup"><span data-stu-id="67f61-157">Composition Window</span></span>                             | <span data-ttu-id="67f61-158">Contiene la colección de caracteres que el usuario ha compuesto con el IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="67f61-159">El IME dibuja estos caracteres en la parte superior de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67f61-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="67f61-160">Cuando el usuario notifica al IME que la cadena de composición es satisfactoria, el IME envía la cadena de composición a la aplicación a través de una serie de mensajes \_ WM CHAR.</span><span class="sxs-lookup"><span data-stu-id="67f61-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="67f61-161">cadena de composición</span><span class="sxs-lookup"><span data-stu-id="67f61-161">composition string</span></span>                           |
| <span data-ttu-id="67f61-162">C.</span><span class="sxs-lookup"><span data-stu-id="67f61-162">C.</span></span> <span data-ttu-id="67f61-163">Ventana Candidata</span><span class="sxs-lookup"><span data-stu-id="67f61-163">Candidate Window</span></span>                               | <span data-ttu-id="67f61-164">Cuando el usuario ha escrito una pronunciación válida, el IME muestra una lista de caracteres candidatos que coinciden con la pronunciación dada.</span><span class="sxs-lookup"><span data-stu-id="67f61-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="67f61-165">A continuación, el usuario selecciona el carácter deseado de esta lista y el IME agrega este carácter a la pantalla Ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="67f61-166">el siguiente carácter de la cadena de composición</span><span class="sxs-lookup"><span data-stu-id="67f61-166">the next character in the composition string</span></span> |
| <span data-ttu-id="67f61-167">D.</span><span class="sxs-lookup"><span data-stu-id="67f61-167">D.</span></span> <span data-ttu-id="67f61-168">[Indicador de configuración regional de](/windows/desktop/Intl/nls-terminology) entrada</span><span class="sxs-lookup"><span data-stu-id="67f61-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="67f61-169">Muestra el idioma que el usuario ha seleccionado para la entrada de teclado.</span><span class="sxs-lookup"><span data-stu-id="67f61-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="67f61-170">Este indicador se inserta en la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="67f61-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="67f61-171">Para seleccionar el idioma de entrada, abra el cuadro de diálogo Opciones regionales Panel de control idioma y, a continuación, haga clic en Detalles en la pestaña Idiomas.</span><span class="sxs-lookup"><span data-stu-id="67f61-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="67f61-172">Uso de IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="67f61-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="67f61-173">En DXUT, la clase CD DXTIMEEditBox implementa la funcionalidad IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="67f61-174">Esta clase se deriva de la clase CDXUTEditBox, el control de edición básico proporcionado por el marco.</span><span class="sxs-lookup"><span data-stu-id="67f61-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="67f61-175">CDMUTTIMEEditBox amplía ese control de edición para admitir los IME mediante la invalidación de los métodos CDMUTTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="67f61-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="67f61-176">Las clases están diseñadas de esta manera para ayudar a los desarrolladores a aprender lo que necesitan tomar del marco para implementar la compatibilidad con IME en sus propios controles de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="67f61-177">En el resto de este tema se explica cómo el marco de trabajo, y CDTEXTTIMEEditBox en particular, invalida un control de edición básico para implementar la funcionalidad de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="67f61-178">La mayoría de las variables específicas de IME de CDEDITTIMEEditBox se declaran como estáticas, ya que muchos búferes y estados de IME son específicos del proceso.</span><span class="sxs-lookup"><span data-stu-id="67f61-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="67f61-179">Por ejemplo, un proceso tiene solo un búfer para la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="67f61-180">Incluso si el proceso tiene diez controles de edición, todos compartirán el mismo búfer de cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="67f61-181">Por lo tanto, el búfer de cadenas de composición para CD COMPOSTIMEEditBox es estático, lo que impide que la aplicación tome espacio de memoria innecesario.</span><span class="sxs-lookup"><span data-stu-id="67f61-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="67f61-182">CD DXTIMEEditBox se implementa en el siguiente código DXUT:</span><span class="sxs-lookup"><span data-stu-id="67f61-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="67f61-183">(raíz del SDK) \\ Ejemplos \\ de D \\ \\ MALWARETgui.cpp comunes de C++</span><span class="sxs-lookup"><span data-stu-id="67f61-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="67f61-184">Invalidar el comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="67f61-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="67f61-185">Normalmente, un IME usa procedimientos estándar de Windows para crear una ventana (consulte [Uso de Windows).](/windows/desktop/winmsg/using-windows)</span><span class="sxs-lookup"><span data-stu-id="67f61-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="67f61-186">En circunstancias normales, esto produce resultados satisfactorios.</span><span class="sxs-lookup"><span data-stu-id="67f61-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="67f61-187">Sin embargo, cuando la aplicación se presenta en modo de pantalla completa, como es habitual para los juegos, las ventanas estándar ya no funcionan y es posible que no se muestren encima de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67f61-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="67f61-188">Para solucionar este problema, la aplicación debe dibujar las propias ventanas de IME en lugar de depender de Windows para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="67f61-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="67f61-189">Cuando el comportamiento predeterminado de creación de ventanas de IME no proporciona lo que requiere una aplicación, la aplicación puede invalidar el control de ventanas de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="67f61-190">Una aplicación puede lograrlo procesando mensajes relacionados con IME y llamando a [la](/windows/desktop/Intl/input-method-manager) API del Administrador de métodos de entrada (IMM).</span><span class="sxs-lookup"><span data-stu-id="67f61-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="67f61-191">Cuando un usuario interactúa con un IME para introducir caracteres complejos, IMM envía mensajes a la aplicación para notificarle eventos importantes, como iniciar una composición o mostrar la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="67f61-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="67f61-192">Normalmente, una aplicación omite estos mensajes y los pasa al controlador de mensajes predeterminado, lo que hace que el IME los controle.</span><span class="sxs-lookup"><span data-stu-id="67f61-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="67f61-193">Cuando la aplicación, en lugar del controlador predeterminado, controla los mensajes, controla exactamente lo que sucede en cada uno de los eventos de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="67f61-194">A menudo, el controlador de mensajes recupera el contenido de las distintas ventanas de IME mediante una llamada a la API de IMM.</span><span class="sxs-lookup"><span data-stu-id="67f61-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="67f61-195">Una vez que la aplicación tiene esta información, puede dibujar correctamente las propias ventanas de IME cuando necesite representarse en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="67f61-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="67f61-196">Functions</span><span class="sxs-lookup"><span data-stu-id="67f61-196">Functions</span></span>

<span data-ttu-id="67f61-197">Un IME debe obtener la cadena de lectura, ocultar la ventana de lectura y obtener la orientación de la ventana de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="67f61-198">En esta tabla se muestran las funcionalidades por versión de IME:</span><span class="sxs-lookup"><span data-stu-id="67f61-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="67f61-199">Obtención de la cadena de lectura</span><span class="sxs-lookup"><span data-stu-id="67f61-199">Getting reading string</span></span>                                                | <span data-ttu-id="67f61-200">Ocultar la ventana de lectura</span><span class="sxs-lookup"><span data-stu-id="67f61-200">Hiding reading window</span></span>                       | <span data-ttu-id="67f61-201">Orientación de la ventana de lectura</span><span class="sxs-lookup"><span data-stu-id="67f61-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="67f61-202">**Antes de la versión 6.0**</span><span class="sxs-lookup"><span data-stu-id="67f61-202">**Before version 6.0**</span></span> | <span data-ttu-id="67f61-203">A.</span><span class="sxs-lookup"><span data-stu-id="67f61-203">A.</span></span> <span data-ttu-id="67f61-204">Lectura de datos privados de IME de acceso a la ventana directamente.</span><span class="sxs-lookup"><span data-stu-id="67f61-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="67f61-205">Vea "4 Structure" (Estructura 4).</span><span class="sxs-lookup"><span data-stu-id="67f61-205">See "4 Structure"</span></span> | <span data-ttu-id="67f61-206">Captura de mensajes privados de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-206">Trap IME private messages.</span></span> <span data-ttu-id="67f61-207">Vea "3 mensajes"</span><span class="sxs-lookup"><span data-stu-id="67f61-207">See "3 Messages"</span></span> | <span data-ttu-id="67f61-208">Examine la información del Registro.</span><span class="sxs-lookup"><span data-stu-id="67f61-208">Examine registry information.</span></span> <span data-ttu-id="67f61-209">Vea "5 Información del Registro"</span><span class="sxs-lookup"><span data-stu-id="67f61-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="67f61-210">**Después de la versión 6.0**</span><span class="sxs-lookup"><span data-stu-id="67f61-210">**After version 6.0**</span></span>  | [<span data-ttu-id="67f61-211">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="67f61-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="67f61-212">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="67f61-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="67f61-213">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="67f61-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="67f61-214">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="67f61-214">Messages</span></span>

<span data-ttu-id="67f61-215">Los mensajes siguientes no tienen que procesarse para un IME más reciente que implemente [ShowReadingWindow](#showreadingwindow)().</span><span class="sxs-lookup"><span data-stu-id="67f61-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="67f61-216">El controlador de mensajes de la aplicación (es decir, no se pasa a DefWindowProc) para evitar que se muestre la ventana de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="67f61-217">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="67f61-217">Examples</span></span>

<span data-ttu-id="67f61-218">En los ejemplos siguientes se muestra cómo obtener información de cadena de lectura del IME anterior que no tiene GetReadingString().</span><span class="sxs-lookup"><span data-stu-id="67f61-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="67f61-219">El código genera las siguientes salidas:</span><span class="sxs-lookup"><span data-stu-id="67f61-219">The code generates the following outputs:</span></span>



| <span data-ttu-id="67f61-220">Output</span><span class="sxs-lookup"><span data-stu-id="67f61-220">Output</span></span>              | <span data-ttu-id="67f61-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f61-221">Description</span></span>                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67f61-222">DWORD dwlen</span><span class="sxs-lookup"><span data-stu-id="67f61-222">DWORD dwlen</span></span>  | <span data-ttu-id="67f61-223">Longitud de la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-223">Length of the reading string.</span></span>                                                          |
| <span data-ttu-id="67f61-224">DWORD dwerr</span><span class="sxs-lookup"><span data-stu-id="67f61-224">DWORD dwerr</span></span>  | <span data-ttu-id="67f61-225">Índice del carácter de error.</span><span class="sxs-lookup"><span data-stu-id="67f61-225">Index of the error character.</span></span>                                                                   |
| <span data-ttu-id="67f61-226">LPWSTR wstr</span><span class="sxs-lookup"><span data-stu-id="67f61-226">LPWSTR wstr</span></span>  | <span data-ttu-id="67f61-227">Puntero a la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-227">Pointer to the reading string.</span></span>                                                         |
| <span data-ttu-id="67f61-228">UNICODE BOOL</span><span class="sxs-lookup"><span data-stu-id="67f61-228">BOOL unicode</span></span> | <span data-ttu-id="67f61-229">Si es true, la cadena de lectura está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="67f61-229">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="67f61-230">De lo contrario, está en formato multibyte.</span><span class="sxs-lookup"><span data-stu-id="67f61-230">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="67f61-231">CHT IME versión 4.2, 4.3 y 4.4</span><span class="sxs-lookup"><span data-stu-id="67f61-231">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="67f61-232">CHT IME versión 5.0</span><span class="sxs-lookup"><span data-stu-id="67f61-232">CHT IME version 5.0</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="67f61-233">CHT IME versión 5.1, 5.2 y CHS IME versión 5.3</span><span class="sxs-lookup"><span data-stu-id="67f61-233">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a><span data-ttu-id="67f61-234">IME de CHS, versión 4.1</span><span class="sxs-lookup"><span data-stu-id="67f61-234">CHS IME version 4.1</span></span>

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a><span data-ttu-id="67f61-235">IME de CHS, versión 4.2</span><span class="sxs-lookup"><span data-stu-id="67f61-235">CHS IME version 4.2</span></span>

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a><span data-ttu-id="67f61-236">Mensajes IME</span><span class="sxs-lookup"><span data-stu-id="67f61-236">IME Messages</span></span>

<span data-ttu-id="67f61-237">Una aplicación de pantalla completa debe controlar correctamente los siguientes mensajes relacionados con IME:</span><span class="sxs-lookup"><span data-stu-id="67f61-237">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="67f61-238">WM \_ INPUTLANGCHANGE</span><span class="sxs-lookup"><span data-stu-id="67f61-238">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="67f61-239">IMM envía un mensaje DE WM INPUTLANGCHANGE a la ventana activa de una aplicación después de que el usuario haya cambiado la configuración regional de entrada con una combinación de teclas (normalmente ALT+MAYÚS) o con el indicador de configuración regional de entrada en la barra de tareas o la barra de \_ idioma.</span><span class="sxs-lookup"><span data-stu-id="67f61-239">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="67f61-240">La barra de idioma es un control en pantalla con el que el usuario puede configurar un servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="67f61-240">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="67f61-241">(Vea [Cómo mostrar la barra de idioma).](/windows/desktop/TSF/how-to-set-up-tsf) La siguiente captura de pantalla muestra una lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="67f61-241">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional](images/ime-langselection.png)

<span data-ttu-id="67f61-243">Cuando IMM envía un mensaje DE WM \_ INPUTLANGCHANGE, CDALTERTIMEEditBox debe realizar varias tareas importantes:</span><span class="sxs-lookup"><span data-stu-id="67f61-243">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="67f61-244">Se llama al método GetKeyboardLayout para devolver el identificador de configuración regional (ID) de entrada para el subproceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="67f61-244">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="67f61-245">La clase CDCOLATIMEEditBox guarda este identificador en su variable miembro estática \_ hklCurrent para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="67f61-245">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="67f61-246">Es importante que la aplicación conozca la configuración regional de entrada actual, ya que el IME de cada idioma tiene su propio comportamiento distinto.</span><span class="sxs-lookup"><span data-stu-id="67f61-246">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="67f61-247">Es posible que el desarrollador tenga que proporcionar código diferente para distintas configuraciones regionales de entrada.</span><span class="sxs-lookup"><span data-stu-id="67f61-247">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="67f61-248">CDEDITTIMEEditBox inicializa una cadena para mostrarla en el indicador de idioma del cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-248">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="67f61-249">Este indicador puede mostrar el idioma de entrada activo cuando la aplicación se ejecuta en modo de pantalla completa y ni la barra de tareas ni la barra de idioma están visibles.</span><span class="sxs-lookup"><span data-stu-id="67f61-249">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="67f61-250">Se llama al método ImmGetConversionStatus para indicar si la configuración regional de entrada está en modo de conversión nativo o no nativo.</span><span class="sxs-lookup"><span data-stu-id="67f61-250">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="67f61-251">El modo de conversión nativa permite al usuario escribir texto en el idioma elegido.</span><span class="sxs-lookup"><span data-stu-id="67f61-251">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="67f61-252">El modo de conversión no nativo hace que el teclado actúe como un teclado en inglés estándar.</span><span class="sxs-lookup"><span data-stu-id="67f61-252">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="67f61-253">Es importante proporcionar al usuario una indicación visual sobre en qué tipo de modo de conversión se encuentra el IME, para que el usuario pueda saber fácilmente qué caracteres esperar al pulsar una tecla.</span><span class="sxs-lookup"><span data-stu-id="67f61-253">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="67f61-254">CDEDITTIMEEditBox proporciona esta indicación visual con un color de indicador de idioma.</span><span class="sxs-lookup"><span data-stu-id="67f61-254">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="67f61-255">Cuando la configuración regional de entrada usa un IME con el modo de conversión nativo, la clase CDANDERTIMEEditBox dibuja el texto del indicador con el color definido por el parámetro m \_ IndicatorImeColor.</span><span class="sxs-lookup"><span data-stu-id="67f61-255">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="67f61-256">Cuando el IME está en modo de conversión no nativo o no se usa ningún IME, la clase dibuja el texto del indicador con el color definido por el parámetro m \_ IndicatorEngColor.</span><span class="sxs-lookup"><span data-stu-id="67f61-256">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="67f61-257">CDCORETIMEEditBox comprueba la configuración regional de entrada y establece la variable miembro estática s bInsertOnType en TRUE para coreano y FALSE para todos los \_ demás idiomas.</span><span class="sxs-lookup"><span data-stu-id="67f61-257">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="67f61-258">Esta marca es necesaria debido a los distintos comportamientos de los IME coreanos y de todos los demás IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-258">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="67f61-259">Al escribir caracteres en idiomas distintos del coreano, el texto escrito por el usuario se muestra en la ventana de composición y el usuario puede cambiar libremente el contenido de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-259">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="67f61-260">El usuario presiona la tecla ENTRAR cuando se satisface con la cadena de composición y la cadena de composición se envía a la aplicación como una serie de mensajes \_ WM CHAR.</span><span class="sxs-lookup"><span data-stu-id="67f61-260">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="67f61-261">Sin embargo, en los IME coreanos, cuando un usuario presiona una tecla para escribir texto, se envía inmediatamente un carácter a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67f61-261">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="67f61-262">Cuando el usuario presiona posteriormente más teclas para modificar ese carácter inicial, el carácter del cuadro de edición cambia para reflejar la entrada adicional del usuario.</span><span class="sxs-lookup"><span data-stu-id="67f61-262">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="67f61-263">Básicamente, el usuario está escribiendo caracteres en el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-263">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="67f61-264">Estos dos comportamientos son lo suficientemente diferentes como para que CD QRTIMEEditBox deba codificar para cada uno de ellos específicamente.</span><span class="sxs-lookup"><span data-stu-id="67f61-264">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="67f61-265">Se llama al método de miembro estático SetupImeApi para recuperar direcciones de dos funciones del módulo IME: GetReadingString y ShowReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="67f61-265">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="67f61-266">Si existen estas funciones, se llama a ShowReadingWindow para ocultar la ventana de lectura predeterminada para este IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-266">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="67f61-267">Dado que la aplicación representa la propia ventana de lectura, notifica al IME que deshabilite el dibujo de la ventana de lectura predeterminada para que no interfiera con la representación a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="67f61-267">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="67f61-268">IMM envía un mensaje \_ SETCONTEXT de WM IME cuando se activa una \_ ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67f61-268">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="67f61-269">El parámetro lParam de este mensaje contiene una marca que indica al IME qué ventanas se deben dibujar y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="67f61-269">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="67f61-270">Dado que la aplicación está controlando todo el dibujo, no necesita el IME para dibujar ninguna de las ventanas de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-270">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="67f61-271">Por lo tanto, el controlador de mensajes de la aplicación simplemente establece lParam en 0 y devuelve .</span><span class="sxs-lookup"><span data-stu-id="67f61-271">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="67f61-272">Para que las aplicaciones admitan IME, se necesita un procesamiento especial para el mensaje WM IME SETCONTEXT relacionado con \_ \_ IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-272">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="67f61-273">Puesto que Windows normalmente envía este mensaje a la aplicación antes de llamar al método PanoramaInitialize(), Panorama no tiene la oportunidad de procesar la interfaz de usuario para mostrar las ventanas de lista candidatas.</span><span class="sxs-lookup"><span data-stu-id="67f61-273">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="67f61-274">El siguiente fragmento de código especifica a las aplicaciones de Windows que no muestren ninguna interfaz de usuario asociada a la ventana de lista de candidatos, lo que permite a Panorama controlar específicamente esta interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="67f61-274">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="67f61-275">WM \_ IME \_ STARTCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="67f61-275">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="67f61-276">IMM envía un mensaje STARTCOMPOSITION de WM IME a la aplicación cuando una composición de IME está a punto de comenzar como resultado de pulsaciones de teclas \_ \_ por parte del usuario.</span><span class="sxs-lookup"><span data-stu-id="67f61-276">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="67f61-277">Si el IME usa la ventana de composición, muestra la cadena de composición actual en una ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-277">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="67f61-278">CDDORESTIMEEditBox controla este mensaje mediante la realización de dos tareas:</span><span class="sxs-lookup"><span data-stu-id="67f61-278">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="67f61-279">CDEDITTIMEEditBox borra el búfer de cadenas de composición y el búfer de atributos.</span><span class="sxs-lookup"><span data-stu-id="67f61-279">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="67f61-280">Estos búferes son miembros estáticos de CDEDITTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="67f61-280">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="67f61-281">CD CURSORTIMEEditBox establece la variable miembro \_ estática bHideCaret de s en TRUE.</span><span class="sxs-lookup"><span data-stu-id="67f61-281">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="67f61-282">Este miembro, definido en la clase base CDXUTEditBox, controla si el cursor del cuadro de edición debe dibujarse cuando se represente el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-282">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="67f61-283">La ventana de composición funciona de forma similar a un cuadro de edición con texto y cursor.</span><span class="sxs-lookup"><span data-stu-id="67f61-283">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="67f61-284">Para evitar confusiones cuando la ventana de composición está visible, el cuadro de edición oculta su cursor para que solo esté visible un cursor a la vez.</span><span class="sxs-lookup"><span data-stu-id="67f61-284">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="67f61-285">WM \_ IME \_ COMPOSITION</span><span class="sxs-lookup"><span data-stu-id="67f61-285">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="67f61-286">IMM envía un mensaje WM IME COMPOSITION a la aplicación cuando el usuario escribe una pulsación de \_ tecla para cambiar la cadena de \_ composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-286">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="67f61-287">El valor de lParam indica qué tipo de información puede recuperar la aplicación del Administrador de métodos de entrada (IMM).</span><span class="sxs-lookup"><span data-stu-id="67f61-287">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="67f61-288">La aplicación debe recuperar la información disponible llamando a [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) y, a continuación, debe guardar la información en su búfer privado para que pueda representar los elementos IME más adelante.</span><span class="sxs-lookup"><span data-stu-id="67f61-288">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="67f61-289">CDEDITTIMEEditBox busca y recupera los siguientes datos de cadena de composición:</span><span class="sxs-lookup"><span data-stu-id="67f61-289">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="67f61-290">[**WM \_ Valor de \_ marca iME COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam</span><span class="sxs-lookup"><span data-stu-id="67f61-290">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="67f61-291">data</span><span class="sxs-lookup"><span data-stu-id="67f61-291">Data</span></span>                           | <span data-ttu-id="67f61-292">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f61-292">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f61-293">GCS \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="67f61-293">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="67f61-294">Atributo Composition</span><span class="sxs-lookup"><span data-stu-id="67f61-294">Composition Attribute</span></span>          | <span data-ttu-id="67f61-295">Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido).</span><span class="sxs-lookup"><span data-stu-id="67f61-295">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="67f61-296">Esta información es necesaria porque CD BYTETIMEEditBox colore los caracteres de cadena de composición de forma diferente en función de sus atributos.</span><span class="sxs-lookup"><span data-stu-id="67f61-296">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="67f61-297">GCS \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="67f61-297">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="67f61-298">Información de la cláusula composition</span><span class="sxs-lookup"><span data-stu-id="67f61-298">Composition Clause Information</span></span> | <span data-ttu-id="67f61-299">Esta información de cláusula se usa cuando el IME japonés está activo.</span><span class="sxs-lookup"><span data-stu-id="67f61-299">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="67f61-300">Cuando se convierte una cadena de composición japonesa, los caracteres se pueden agrupar como una cláusula que se convierte en una sola entidad.</span><span class="sxs-lookup"><span data-stu-id="67f61-300">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="67f61-301">Cuando el usuario mueve el cursor, CD CURSORTIMEEditBox usa esta información para resaltar toda la cláusula, en lugar de un solo carácter dentro de la cláusula .</span><span class="sxs-lookup"><span data-stu-id="67f61-301">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="67f61-302">GCS \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="67f61-302">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="67f61-303">Cadena de composición</span><span class="sxs-lookup"><span data-stu-id="67f61-303">Composition String</span></span>             | <span data-ttu-id="67f61-304">Esta cadena es la cadena actualizada que está compuesta por el usuario.</span><span class="sxs-lookup"><span data-stu-id="67f61-304">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="67f61-305">También es la cadena que se muestra en la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-305">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="67f61-306">CURSORPOS \_ de GCS</span><span class="sxs-lookup"><span data-stu-id="67f61-306">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="67f61-307">Posición del cursor de composición</span><span class="sxs-lookup"><span data-stu-id="67f61-307">Composition Cursor Position</span></span>    | <span data-ttu-id="67f61-308">La ventana de composición implementa un cursor, similar al cursor de un cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-308">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="67f61-309">La aplicación puede recuperar la posición del cursor al procesar el mensaje COMPOSITION de WM \_ IME \_ para dibujar el cursor correctamente.</span><span class="sxs-lookup"><span data-stu-id="67f61-309">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="67f61-310">GCS \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="67f61-310">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="67f61-311">Cadena de resultado</span><span class="sxs-lookup"><span data-stu-id="67f61-311">Result String</span></span>                  | <span data-ttu-id="67f61-312">La cadena de resultado está disponible cuando el usuario está a punto de completar el proceso de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-312">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="67f61-313">Esta cadena se debe recuperar y los caracteres se deben enviar al cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-313">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="67f61-314">WM \_ IME \_ ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="67f61-314">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="67f61-315">IMM envía un mensaje ENDCOMPOSITION de WM IME a la aplicación cuando finaliza la operación de composición \_ \_ de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-315">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="67f61-316">Esto puede ocurrir cuando el usuario presiona la tecla ENTRAR para aprobar la cadena de composición o la tecla ESC para cancelar la composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-316">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="67f61-317">CD COMPOSTIMEEditBox controla este mensaje estableciendo el búfer de cadena de composición en vacío.</span><span class="sxs-lookup"><span data-stu-id="67f61-317">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="67f61-318">A continuación, establece bHideCaret en FALSE porque la ventana de composición está cerrada y el cursor del cuadro de edición \_ debe volver a estar visible.</span><span class="sxs-lookup"><span data-stu-id="67f61-318">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="67f61-319">El controlador de mensajes CDEDITTIMEEditBox también establece \_ bShowReadingWindow en FALSE.</span><span class="sxs-lookup"><span data-stu-id="67f61-319">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="67f61-320">Esta marca controla si la clase dibuja la ventana de lectura cuando el cuadro de edición se representa a sí mismo, por lo que debe establecerse en FALSE cuando finaliza una composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-320">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="67f61-321">WM \_ IME \_ NOTIFY</span><span class="sxs-lookup"><span data-stu-id="67f61-321">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="67f61-322">IMM envía un mensaje WM IME NOTIFY a la aplicación cada \_ vez que cambia una ventana de \_ IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-322">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="67f61-323">Una aplicación que controla el dibujo de las ventanas de IME debe procesar este mensaje para que sea consciente de cualquier actualización del contenido de la ventana.</span><span class="sxs-lookup"><span data-stu-id="67f61-323">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="67f61-324">wParam indica el comando o el cambio que se está llevando a cabo.</span><span class="sxs-lookup"><span data-stu-id="67f61-324">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="67f61-325">CDEDITTIMEEditBox controla los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="67f61-325">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67f61-326">Comando IME</span><span class="sxs-lookup"><span data-stu-id="67f61-326">IME Command</span></span></th>
<th><span data-ttu-id="67f61-327">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f61-327">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67f61-328"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="67f61-328"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="67f61-329">Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido).</span><span class="sxs-lookup"><span data-stu-id="67f61-329">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="67f61-330">Esta información es necesaria porque CD BYTETIMEEditBox colore los caracteres de cadena de composición de forma diferente en función de sus atributos.</span><span class="sxs-lookup"><span data-stu-id="67f61-330">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67f61-331"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="67f61-331"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="67f61-332">Se envía a la aplicación cuando la ventana candidata está a punto de abrirse o actualizarse, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="67f61-332">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="67f61-333">La ventana candidata se abre cuando un usuario desea cambiar la opción de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="67f61-333">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="67f61-334">La ventana se actualiza cuando un usuario mueve el indicador de selección o cambia la página.</span><span class="sxs-lookup"><span data-stu-id="67f61-334">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="67f61-335">CDEDITTIMEEditBox usa un controlador de mensajes para ambos comandos porque las tareas necesarias son exactamente las mismas:</span><span class="sxs-lookup"><span data-stu-id="67f61-335">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="67f61-336">CDSHOWTIMEEditBox establece el miembro bShowWindow de la estructura de lista de candidatos s_CandList en TRUE para indicar que la ventana candidata debe dibujarse durante la representación del marco.</span><span class="sxs-lookup"><span data-stu-id="67f61-336">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="67f61-337">CDDHTIMEEditBox recupera la lista de candidatos mediante una llamada a <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList,</strong></a>primero para obtener el tamaño de búfer necesario y, después, para obtener los datos reales.</span><span class="sxs-lookup"><span data-stu-id="67f61-337">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="67f61-338">La estructura de lista de candidatos s_CandList se inicializa con los datos candidatos recuperados.</span><span class="sxs-lookup"><span data-stu-id="67f61-338">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="67f61-339">Las cadenas candidatas se almacenan como una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="67f61-339">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="67f61-340">Se guarda el índice de la entrada seleccionada, así como el índice de página.</span><span class="sxs-lookup"><span data-stu-id="67f61-340">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="67f61-341">CDEDITTIMEEditBox comprueba si el estilo de la ventana candidata es vertical u horizontal.</span><span class="sxs-lookup"><span data-stu-id="67f61-341">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="67f61-342">Si el estilo de ventana es horizontal, se debe inicializar un búfer de cadena adicional, el miembro HoriCand de s_CandList, con todas las cadenas candidatas, con caracteres de espacio insertados entre todas las cadenas adyacentes.</span><span class="sxs-lookup"><span data-stu-id="67f61-342">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="67f61-343">Al representar una ventana candidata vertical, las cadenas candidatas individuales se dibujan de una en una, con las coordenadas y incrementadas para cada cadena.</span><span class="sxs-lookup"><span data-stu-id="67f61-343">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="67f61-344">Sin embargo, esta cadena HoriCand debe usarse al representar una ventana candidata horizontal, ya que el carácter de espacio es la mejor manera de separar dos cadenas adyacentes en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="67f61-344">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67f61-345"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="67f61-345"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="67f61-346">Se envía a la aplicación cuando una ventana candidata está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="67f61-346">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="67f61-347">Esto sucede cuando un usuario ha realizado una selección de la lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="67f61-347">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="67f61-348">CDANDERTIMEEditBox controla este comando estableciendo la marca visible de la ventana candidata en FALSE y, a continuación, borrando el búfer de cadenas candidatas.</span><span class="sxs-lookup"><span data-stu-id="67f61-348">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67f61-349">IMN_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="67f61-349">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="67f61-350">Se envía a la aplicación cuando el IME ha actualizado su cadena de lectura como resultado de que el usuario escriba o quite caracteres.</span><span class="sxs-lookup"><span data-stu-id="67f61-350">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="67f61-351">La aplicación debe recuperar la cadena de lectura y guardarla para su representación.</span><span class="sxs-lookup"><span data-stu-id="67f61-351">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="67f61-352">CDEDITTIMEEditBox tiene dos métodos para recuperar la cadena de lectura, en función de cómo se admiten las cadenas de lectura en el IME:</span><span class="sxs-lookup"><span data-stu-id="67f61-352">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="67f61-353">Si el IME admite la función GetReadingString, se llama a GetReadingString para recuperar la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-353">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="67f61-354">Si el IME no implementa GetReadingString, CDSTRINGTIMEEditBox recupera la cadena de lectura del contenido del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="67f61-354">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="67f61-355">Representación</span><span class="sxs-lookup"><span data-stu-id="67f61-355">Rendering</span></span>

<span data-ttu-id="67f61-356">La representación de los elementos y ventanas de IME es sencilla.</span><span class="sxs-lookup"><span data-stu-id="67f61-356">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="67f61-357">CDEDITTIMEEditBox permite que la clase base se represente primero porque las ventanas IME deben aparecer en la parte superior del control de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-357">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="67f61-358">Después de representar el cuadro de edición base, CDANDERTIMEEditBox comprueba la marca de visibilidad de cada ventana de IME (indicador, composición, candidato y ventana de lectura) y dibuja la ventana si debe estar visible.</span><span class="sxs-lookup"><span data-stu-id="67f61-358">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="67f61-359">Consulte Comportamiento predeterminado de IME para obtener descripciones de los diferentes tipos de ventana de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-359">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="67f61-360">Indicador de configuración regional de entrada</span><span class="sxs-lookup"><span data-stu-id="67f61-360">Input Locale Indicator</span></span>

<span data-ttu-id="67f61-361">El indicador de configuración regional de entrada se representa antes que cualquier otra ventana IME porque es un elemento que siempre se muestra.</span><span class="sxs-lookup"><span data-stu-id="67f61-361">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="67f61-362">Por lo tanto, debería aparecer debajo de otras ventanas de IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-362">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="67f61-363">CDINTEGRATIMEEditBox representa el indicador mediante una llamada al método RenderIndicator, en el que el color de fuente del indicador se determina mediante el examen de la variable estática S ImeState, que refleja el modo de conversión \_ de IME actual.</span><span class="sxs-lookup"><span data-stu-id="67f61-363">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="67f61-364">Cuando el IME está habilitado y la conversión nativa está activa, el método usa m \_ IndicatorImeColor como color del indicador.</span><span class="sxs-lookup"><span data-stu-id="67f61-364">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="67f61-365">Si el IME está deshabilitado o está en modo de conversión no nativo, se usa m \_ IndicatorImeColor para dibujar el texto del indicador.</span><span class="sxs-lookup"><span data-stu-id="67f61-365">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="67f61-366">De forma predeterminada, la propia ventana del indicador se dibuja a la derecha del cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-366">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="67f61-367">Las aplicaciones pueden cambiar este comportamiento invalidando el método RenderIndicator.</span><span class="sxs-lookup"><span data-stu-id="67f61-367">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="67f61-368">En la ilustración siguiente se muestran las distintas apariencias de un indicador de configuración regional de entrada para inglés, japonés en modo de conversión alfanumérica y japonés en modo de conversión nativa:</span><span class="sxs-lookup"><span data-stu-id="67f61-368">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![diferentes apariencias de un indicador de configuración regional de entrada para inglés y japonés](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="67f61-370">Ventana Composición</span><span class="sxs-lookup"><span data-stu-id="67f61-370">Composition Window</span></span>

<span data-ttu-id="67f61-371">El dibujo de la ventana de composición se controla en el método RenderComposition de CDCOMPOSICIÓNTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="67f61-371">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="67f61-372">La ventana de composición flota sobre el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="67f61-372">The composition window floats above the edit box.</span></span> <span data-ttu-id="67f61-373">Debe dibujarse en la posición del cursor del control de edición subyacente.</span><span class="sxs-lookup"><span data-stu-id="67f61-373">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="67f61-374">CDEDITTIMEEditBox controla la representación de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="67f61-374">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="67f61-375">Toda la cadena de composición se dibuja con los colores predeterminados de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="67f61-375">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="67f61-376">Los caracteres con determinados atributos especiales se deben dibujar en colores diferentes, por lo que CD BYTETIMEEditBox revisa los caracteres de la cadena de composición e inspecciona el atributo de cadena.</span><span class="sxs-lookup"><span data-stu-id="67f61-376">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="67f61-377">Si el atributo llama a colores diferentes, el carácter se dibuja de nuevo con los colores adecuados.</span><span class="sxs-lookup"><span data-stu-id="67f61-377">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="67f61-378">El cursor de la ventana de composición se dibuja para completar la representación.</span><span class="sxs-lookup"><span data-stu-id="67f61-378">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="67f61-379">El cursor debe parpadear para los IME coreanos, pero no para otros IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-379">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="67f61-380">RenderComposition determina si el cursor debe estar visible en función de los valores de temporizador cuando se usa el IME coreano.</span><span class="sxs-lookup"><span data-stu-id="67f61-380">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="67f61-381">Ventanas de lectura y candidatas</span><span class="sxs-lookup"><span data-stu-id="67f61-381">Reading and Candidate Windows</span></span>

<span data-ttu-id="67f61-382">Las ventanas de lectura y candidatas se representan mediante el mismo método CDOIDTIMEEditBox, RenderCandidateReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="67f61-382">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="67f61-383">Ambas ventanas contienen una matriz de cadenas para el diseño vertical o una sola cadena en el caso del diseño horizontal.</span><span class="sxs-lookup"><span data-stu-id="67f61-383">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="67f61-384">La mayor parte del código de RenderCandidateReadingWindow se usa para colocar la ventana de modo que ninguna parte de la ventana esté fuera de la ventana de la aplicación y se recorte.</span><span class="sxs-lookup"><span data-stu-id="67f61-384">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="67f61-385">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="67f61-385">Limitations</span></span>

<span data-ttu-id="67f61-386">A veces, los IME contienen características avanzadas para mejorar la facilidad de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="67f61-386">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="67f61-387">Algunas de las características que se encuentran en los IME más recientes se muestran en las cifras siguientes.</span><span class="sxs-lookup"><span data-stu-id="67f61-387">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="67f61-388">Estas características avanzadas no están presentes en DXUT.</span><span class="sxs-lookup"><span data-stu-id="67f61-388">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="67f61-389">Implementar la compatibilidad con estas características avanzadas puede ser complicado porque no hay ninguna interfaz definida para obtener la información necesaria de los IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-389">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="67f61-390">IME chino tradicional avanzado con lista de candidatos expandida:</span><span class="sxs-lookup"><span data-stu-id="67f61-390">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![ime chino tradicional avanzado con lista de candidatos expandida](images/ime-advanced1.png)

<span data-ttu-id="67f61-392">IME japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir sus significados:</span><span class="sxs-lookup"><span data-stu-id="67f61-392">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![ime japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir sus significados](images/ime-advanced2.png)

<span data-ttu-id="67f61-394">IME coreano avanzado que incluye un sistema de reconocimiento de escritura a mano:</span><span class="sxs-lookup"><span data-stu-id="67f61-394">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![ime coreano avanzado que incluye un sistema de reconocimiento de escritura a mano](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="67f61-396">Información del Registro</span><span class="sxs-lookup"><span data-stu-id="67f61-396">Registry Information</span></span>

<span data-ttu-id="67f61-397">La siguiente información del Registro se comprueba para determinar la orientación de la ventana de lectura, cuando el IME actual es un nuevo fonético CHT anterior que no implementa GetReadingString().</span><span class="sxs-lookup"><span data-stu-id="67f61-397">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="67f61-398">Key</span><span class="sxs-lookup"><span data-stu-id="67f61-398">Key</span></span>                                                           | <span data-ttu-id="67f61-399">Valor</span><span class="sxs-lookup"><span data-stu-id="67f61-399">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="67f61-400">HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ Name</span><span class="sxs-lookup"><span data-stu-id="67f61-400">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="67f61-401">asignación de teclado</span><span class="sxs-lookup"><span data-stu-id="67f61-401">keyboard mapping</span></span> |



 

<span data-ttu-id="67f61-402">Dónde: El nombre de IME es MSTCIPH si la versión del archivo IME es 5.1 o posterior; de lo contrario, el nombre \_ de IME \_ es TINTLGNT.</span><span class="sxs-lookup"><span data-stu-id="67f61-402">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="67f61-403">La orientación de la ventana de lectura es horizontal si:</span><span class="sxs-lookup"><span data-stu-id="67f61-403">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="67f61-404">El IME es la versión 5.0 y el valor de asignación de teclado es 0x22 o 0x23</span><span class="sxs-lookup"><span data-stu-id="67f61-404">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="67f61-405">El IME es la versión 5.1 o 5.2 y el valor de asignación de teclado es 0x22, 0x23 o 0x24.</span><span class="sxs-lookup"><span data-stu-id="67f61-405">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="67f61-406">Si no se cumple ninguna condición, la ventana de lectura es vertical.</span><span class="sxs-lookup"><span data-stu-id="67f61-406">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="67f61-407">Apéndice A: Versiones de CHT por sistema operativo</span><span class="sxs-lookup"><span data-stu-id="67f61-407">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="67f61-408">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="67f61-408">Operating System</span></span>           | <span data-ttu-id="67f61-409">Versión de IME de CHT</span><span class="sxs-lookup"><span data-stu-id="67f61-409">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="67f61-410">Windows 98</span><span class="sxs-lookup"><span data-stu-id="67f61-410">Windows 98</span></span>                 | <span data-ttu-id="67f61-411">4,2</span><span class="sxs-lookup"><span data-stu-id="67f61-411">4.2</span></span>             |
| <span data-ttu-id="67f61-412">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="67f61-412">Windows 2000</span></span>               | <span data-ttu-id="67f61-413">4.3</span><span class="sxs-lookup"><span data-stu-id="67f61-413">4.3</span></span>             |
| <span data-ttu-id="67f61-414">unknown</span><span class="sxs-lookup"><span data-stu-id="67f61-414">unknown</span></span>                    | <span data-ttu-id="67f61-415">4.4.</span><span class="sxs-lookup"><span data-stu-id="67f61-415">4.4</span></span>             |
| <span data-ttu-id="67f61-416">Windows ME</span><span class="sxs-lookup"><span data-stu-id="67f61-416">Windows ME</span></span>                 | <span data-ttu-id="67f61-417">5.0</span><span class="sxs-lookup"><span data-stu-id="67f61-417">5.0</span></span>             |
| <span data-ttu-id="67f61-418">Office XP</span><span class="sxs-lookup"><span data-stu-id="67f61-418">Office XP</span></span>                  | <span data-ttu-id="67f61-419">5,1</span><span class="sxs-lookup"><span data-stu-id="67f61-419">5.1</span></span>             |
| <span data-ttu-id="67f61-420">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67f61-420">Windows XP</span></span>                 | <span data-ttu-id="67f61-421">5.2</span><span class="sxs-lookup"><span data-stu-id="67f61-421">5.2</span></span>             |
| <span data-ttu-id="67f61-422">Descarga web independiente</span><span class="sxs-lookup"><span data-stu-id="67f61-422">Standalone web downloadble</span></span> | <span data-ttu-id="67f61-423">6.0</span><span class="sxs-lookup"><span data-stu-id="67f61-423">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="67f61-424">Información adicional</span><span class="sxs-lookup"><span data-stu-id="67f61-424">Further Information</span></span>

<span data-ttu-id="67f61-425">Para obtener información adicional, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="67f61-425">For additional information, see the following:</span></span>

-   [<span data-ttu-id="67f61-426">Instalación y uso de editores de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="67f61-426">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="67f61-427">Presentación de texto internacional</span><span class="sxs-lookup"><span data-stu-id="67f61-427">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="67f61-428">El consorcio Unicode</span><span class="sxs-lookup"><span data-stu-id="67f61-428">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="67f61-429">Desarrollo de software internacional.</span><span class="sxs-lookup"><span data-stu-id="67f61-429">Developing International Software.</span></span> <span data-ttu-id="67f61-430">Dr. International.</span><span class="sxs-lookup"><span data-stu-id="67f61-430">Dr. International.</span></span> <span data-ttu-id="67f61-431">Segundo ed.</span><span class="sxs-lookup"><span data-stu-id="67f61-431">2nd ed.</span></span> <span data-ttu-id="67f61-432">Redmond, WA: Microsoft Press, 2003.</span><span class="sxs-lookup"><span data-stu-id="67f61-432">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="67f61-433">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="67f61-433">GetReadingString</span></span>

<span data-ttu-id="67f61-434">Obtiene información de cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-434">Gets reading string information.</span></span>

<span data-ttu-id="67f61-435">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="67f61-435">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="67f61-436"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="67f61-436"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-437">\[en \] contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="67f61-437">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-438"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span><span class="sxs-lookup"><span data-stu-id="67f61-438"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="67f61-439">\[en \] Longitud de lpwReadingBuf, en WCHAR.</span><span class="sxs-lookup"><span data-stu-id="67f61-439">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="67f61-440">Si es cero, significa que la longitud del búfer de lectura de consultas.</span><span class="sxs-lookup"><span data-stu-id="67f61-440">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-441"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span><span class="sxs-lookup"><span data-stu-id="67f61-441"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-442">\[out \] Devuelve la cadena de lectura (no el extremo cero).</span><span class="sxs-lookup"><span data-stu-id="67f61-442">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="67f61-443"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span><span class="sxs-lookup"><span data-stu-id="67f61-443"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-444">\[out \] Devuelve el índice del carácter de error en la cadena de lectura si lo hay.</span><span class="sxs-lookup"><span data-stu-id="67f61-444">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-445"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span><span class="sxs-lookup"><span data-stu-id="67f61-445"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-446">\[out \] Si es TRUE, la lectura de la interfaz de usuario es vertical.</span><span class="sxs-lookup"><span data-stu-id="67f61-446">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="67f61-447">De lo contrario, puMaxReadingLen horizontal.</span><span class="sxs-lookup"><span data-stu-id="67f61-447">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-448"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span><span class="sxs-lookup"><span data-stu-id="67f61-448"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-449">\[out \] Longitud de la interfaz de usuario de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-449">\[out\] The reading UI length.</span></span> <span data-ttu-id="67f61-450">La longitud máxima de lectura no es fija; depende no solo del diseño del teclado, sino también del modo de entrada (por ejemplo, código interno o entrada suplente).</span><span class="sxs-lookup"><span data-stu-id="67f61-450">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="67f61-451">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="67f61-451">**Return Values**</span></span>

<span data-ttu-id="67f61-452">Longitud de la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-452">The reading string length.</span></span>

<span data-ttu-id="67f61-453">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="67f61-453">**Remarks**</span></span>

<span data-ttu-id="67f61-454">Si el valor devuelto es mayor que el valor de uReadingBufLen, todos los parámetros de salida no están definidos.</span><span class="sxs-lookup"><span data-stu-id="67f61-454">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="67f61-455">Esta función se implementa en CHT IME 6.0 o posterior y GetProcAddress puede adquirirla en un identificador de módulo IME; ImmGetIMEFileName y LoadLibrary pueden adquirir el identificador del módulo IME.</span><span class="sxs-lookup"><span data-stu-id="67f61-455">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="67f61-456">**Requisitos**</span><span class="sxs-lookup"><span data-stu-id="67f61-456">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="67f61-457"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Rúbrica**</span><span class="sxs-lookup"><span data-stu-id="67f61-457"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="67f61-458">Declarado en Imm.h.</span><span class="sxs-lookup"><span data-stu-id="67f61-458">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-459"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**</span><span class="sxs-lookup"><span data-stu-id="67f61-459"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="67f61-460">Use Imm.lib.</span><span class="sxs-lookup"><span data-stu-id="67f61-460">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="67f61-461">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="67f61-461">ShowReadingWindow</span></span>

<span data-ttu-id="67f61-462">Mostrar (u ocultar) la ventana de lectura.</span><span class="sxs-lookup"><span data-stu-id="67f61-462">Show (or hide) the reading window.</span></span>

<span data-ttu-id="67f61-463">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="67f61-463">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="67f61-464"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="67f61-464"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-465">\[en \] contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="67f61-465">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-466"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="67f61-466"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="67f61-467">\[en \] Establecer en TRUE para mostrar la ventana de lectura (o FALSE para ocultarla).</span><span class="sxs-lookup"><span data-stu-id="67f61-467">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="67f61-468">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="67f61-468">**Return Values**</span></span>

<span data-ttu-id="67f61-469">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="67f61-469">**Remarks**</span></span>

<span data-ttu-id="67f61-470">Devuelve TRUE si se realiza correctamente o FALSE si no es así.</span><span class="sxs-lookup"><span data-stu-id="67f61-470">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="67f61-471">**Requisitos**</span><span class="sxs-lookup"><span data-stu-id="67f61-471">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="67f61-472"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Rúbrica**</span><span class="sxs-lookup"><span data-stu-id="67f61-472"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="67f61-473">Declarado en Imm.h.</span><span class="sxs-lookup"><span data-stu-id="67f61-473">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="67f61-474"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**</span><span class="sxs-lookup"><span data-stu-id="67f61-474"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="67f61-475">Use Imm.lib.</span><span class="sxs-lookup"><span data-stu-id="67f61-475">Use Imm.lib.</span></span>

</dd> </dl>