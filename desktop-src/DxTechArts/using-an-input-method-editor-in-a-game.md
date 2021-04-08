---
title: Usar un editor de métodos de entrada en un juego
description: En este artículo se explica cómo se puede implementar un control básico de edición de IME en una aplicación Microsoft DirectX de pantalla completa.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104003744"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="27a19-103">Usar un editor de métodos de entrada en un juego</span><span class="sxs-lookup"><span data-stu-id="27a19-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="27a19-104">En este artículo se describe cómo trabajar con el editor de métodos de entrada (IME) de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27a19-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="27a19-105">Se realizaron cambios en el IME para Windows Vista que no están totalmente detallados en este artículo.</span><span class="sxs-lookup"><span data-stu-id="27a19-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="27a19-106">Para obtener más información acerca de los cambios en el IME para Windows Vista, consulte [editores de métodos de entrada (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) en [Windows Vista: una Ever-Expanding vista de internacionalización](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) en el portal de desarrollo y informática global de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27a19-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="27a19-107">Un editor de métodos de entrada (IME) es un programa que permite una entrada de texto sencilla mediante un teclado estándar para idiomas asiáticos orientales, como el chino, el japonés, el coreano y otros idiomas con caracteres complejos.</span><span class="sxs-lookup"><span data-stu-id="27a19-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="27a19-108">Por ejemplo, con los IME, un usuario puede escribir caracteres complejos en un procesador de textos o un jugador de un juego en línea multijugador masivo puede conversar con amigos en caracteres complejos.</span><span class="sxs-lookup"><span data-stu-id="27a19-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="27a19-109">En este artículo se explica cómo se puede implementar un control básico de edición de IME en una aplicación Microsoft DirectX de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="27a19-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="27a19-110">Las aplicaciones que aprovechan DXUT obtienen automáticamente la funcionalidad IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="27a19-111">En el caso de las aplicaciones que no usan el marco de trabajo, en este artículo se describe cómo agregar compatibilidad con IME a un control de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="27a19-112">Contenido:</span><span class="sxs-lookup"><span data-stu-id="27a19-112">Contents:</span></span>

-   [<span data-ttu-id="27a19-113">Comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="27a19-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="27a19-114">Uso de IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="27a19-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="27a19-115">Invalidar el comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="27a19-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="27a19-116">Funciones</span><span class="sxs-lookup"><span data-stu-id="27a19-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="27a19-117">Mensajes</span><span class="sxs-lookup"><span data-stu-id="27a19-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="27a19-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="27a19-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="27a19-119">CHT IME versión 4,2, 4,3 y 4,4</span><span class="sxs-lookup"><span data-stu-id="27a19-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="27a19-120">CHT IME versión 5,0</span><span class="sxs-lookup"><span data-stu-id="27a19-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="27a19-121">Chino tradicional versión 5,1, 5,2 y CHS IME versión 5,3</span><span class="sxs-lookup"><span data-stu-id="27a19-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="27a19-122">CHS IME versión 4,1</span><span class="sxs-lookup"><span data-stu-id="27a19-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="27a19-123">CHS IME versión 4,2</span><span class="sxs-lookup"><span data-stu-id="27a19-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="27a19-124">Mensajes IME</span><span class="sxs-lookup"><span data-stu-id="27a19-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="27a19-125">INPUTLANGCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="27a19-126">\_STARTCOMPOSITION de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="27a19-127">\_composición del IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="27a19-128">\_ENDCOMPOSITION de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="27a19-129">\_notificación de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="27a19-130">Representación</span><span class="sxs-lookup"><span data-stu-id="27a19-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="27a19-131">Indicador de configuración regional de entrada</span><span class="sxs-lookup"><span data-stu-id="27a19-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="27a19-132">Ventana composición</span><span class="sxs-lookup"><span data-stu-id="27a19-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="27a19-133">Lecturas y ventanas candidatas</span><span class="sxs-lookup"><span data-stu-id="27a19-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="27a19-134">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="27a19-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="27a19-135">Información del registro</span><span class="sxs-lookup"><span data-stu-id="27a19-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="27a19-136">Apéndice A: versiones CHT por sistema operativo</span><span class="sxs-lookup"><span data-stu-id="27a19-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="27a19-137">Información adicional</span><span class="sxs-lookup"><span data-stu-id="27a19-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="27a19-138">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="27a19-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="27a19-139">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="27a19-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="27a19-140">Comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="27a19-140">Default IME Behavior</span></span>

<span data-ttu-id="27a19-141">Los IME asignan entradas de teclado a componentes fonéticos u otros elementos de lenguaje específicos de un idioma seleccionado.</span><span class="sxs-lookup"><span data-stu-id="27a19-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="27a19-142">En un escenario típico, el usuario escribe claves que representan la Pronunciación de un carácter complejo.</span><span class="sxs-lookup"><span data-stu-id="27a19-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="27a19-143">Si el IME reconoce la pronunciación como válida, presenta al usuario una lista de candidatos de palabra o frase desde los que el usuario puede seleccionar una opción final.</span><span class="sxs-lookup"><span data-stu-id="27a19-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="27a19-144">La palabra elegida se envía a la aplicación a través de una serie de mensajes de tipo [**\_ Char**](/windows/desktop/inputdev/wm-char) de Microsoft Windows WM.</span><span class="sxs-lookup"><span data-stu-id="27a19-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="27a19-145">Dado que el IME funciona en un nivel por debajo de la aplicación mediante la interceptación de la entrada del teclado, la presencia de un IME es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27a19-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="27a19-146">Casi todas las aplicaciones de Windows pueden aprovechar fácilmente los IME sin tener en cuenta su existencia y sin necesidad de codificación especial.</span><span class="sxs-lookup"><span data-stu-id="27a19-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="27a19-147">Un IME típico muestra varias ventanas para guiar al usuario a través de la entrada de caracteres, tal y como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="27a19-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![IME muestra varias ventanas](images/ime-elements.png)

| <span data-ttu-id="27a19-149">Tipo de ventana</span><span class="sxs-lookup"><span data-stu-id="27a19-149">Window Type</span></span>                                       | <span data-ttu-id="27a19-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a19-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="27a19-151">Salida de IME</span><span class="sxs-lookup"><span data-stu-id="27a19-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="27a19-152">A.</span><span class="sxs-lookup"><span data-stu-id="27a19-152">A.</span></span> <span data-ttu-id="27a19-153">Ventana de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-153">Reading Window</span></span>                                 | <span data-ttu-id="27a19-154">Contiene pulsaciones de teclas del teclado; Normalmente, los cambios después de cada pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="27a19-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="27a19-155">cadena de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-155">reading string</span></span>                               |
| <span data-ttu-id="27a19-156">B.</span><span class="sxs-lookup"><span data-stu-id="27a19-156">B.</span></span> <span data-ttu-id="27a19-157">Ventana composición</span><span class="sxs-lookup"><span data-stu-id="27a19-157">Composition Window</span></span>                             | <span data-ttu-id="27a19-158">Contiene la colección de caracteres que el usuario ha compuesto con el IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="27a19-159">El IME dibuja estos caracteres en la parte superior de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27a19-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="27a19-160">Cuando el usuario notifica al IME que la cadena de composición es satisfactoria, el IME envía la cadena de composición a la aplicación a través de una serie de mensajes de tipo char de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="27a19-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="27a19-161">cadena de composición</span><span class="sxs-lookup"><span data-stu-id="27a19-161">composition string</span></span>                           |
| <span data-ttu-id="27a19-162">C.</span><span class="sxs-lookup"><span data-stu-id="27a19-162">C.</span></span> <span data-ttu-id="27a19-163">Ventana candidata</span><span class="sxs-lookup"><span data-stu-id="27a19-163">Candidate Window</span></span>                               | <span data-ttu-id="27a19-164">Cuando el usuario ha escrito una pronunciación válida, el IME muestra una lista de caracteres candidatos que coinciden con la pronunciación indicada.</span><span class="sxs-lookup"><span data-stu-id="27a19-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="27a19-165">A continuación, el usuario selecciona el carácter previsto en esta lista y el IME agrega este carácter a la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="27a19-166">carácter siguiente de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-166">the next character in the composition string</span></span> |
| <span data-ttu-id="27a19-167">D.</span><span class="sxs-lookup"><span data-stu-id="27a19-167">D.</span></span> <span data-ttu-id="27a19-168">Indicador de [configuración regional de entrada](/windows/desktop/Intl/nls-terminology)</span><span class="sxs-lookup"><span data-stu-id="27a19-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="27a19-169">Muestra el idioma seleccionado por el usuario para la entrada de teclado.</span><span class="sxs-lookup"><span data-stu-id="27a19-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="27a19-170">Este indicador está incrustado en la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="27a19-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="27a19-171">Para seleccionar el idioma de entrada, abra el panel de control configuración regional y de idioma y, a continuación, haga clic en detalles en la pestaña idiomas.</span><span class="sxs-lookup"><span data-stu-id="27a19-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="27a19-172">Uso de IME con DXUT</span><span class="sxs-lookup"><span data-stu-id="27a19-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="27a19-173">En DXUT, la clase CDXUTIMEEditBox implementa la funcionalidad del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="27a19-174">Esta clase se deriva de la clase CDXUTEditBox, el control básico de edición proporcionado por el marco de trabajo.</span><span class="sxs-lookup"><span data-stu-id="27a19-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="27a19-175">CDXUTIMEEditBox extiende ese control de edición para admitir los IME mediante la invalidación de los métodos CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="27a19-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="27a19-176">Las clases están diseñadas de esta manera para ayudar a los desarrolladores a saber lo que necesitan tomar de la plataforma para implementar la compatibilidad con el IME en sus propios controles de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="27a19-177">En el resto de este tema se explica cómo el marco de trabajo y CDXUTIMEEditBox en concreto reemplazan a un control de edición básico para implementar la funcionalidad de IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="27a19-178">La mayoría de las variables específicas del IME en CDXUTIMEEditBox se declaran como estáticas, ya que muchos de los búferes y Estados IME son específicos del proceso.</span><span class="sxs-lookup"><span data-stu-id="27a19-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="27a19-179">Por ejemplo, un proceso solo tiene un búfer para la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="27a19-180">Aunque el proceso tenga diez controles de edición, todos ellos compartirán el mismo búfer de cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="27a19-181">Por lo tanto, el búfer de cadena de composición para CDXUTIMEEditBox es estático, lo que impide que la aplicación ocupe espacio de memoria innecesario.</span><span class="sxs-lookup"><span data-stu-id="27a19-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="27a19-182">CDXUTIMEEditBox se implementa en el siguiente código de DXUT:</span><span class="sxs-lookup"><span data-stu-id="27a19-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="27a19-183">(Raíz del SDK) \\ Ejemplos \\ C++ \\ común \\ DXUTgui. cpp</span><span class="sxs-lookup"><span data-stu-id="27a19-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="27a19-184">Invalidar el comportamiento predeterminado de IME</span><span class="sxs-lookup"><span data-stu-id="27a19-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="27a19-185">Normalmente, un IME usa los procedimientos estándar de Windows para crear una ventana (consulte [uso de Windows](/windows/desktop/winmsg/using-windows)).</span><span class="sxs-lookup"><span data-stu-id="27a19-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="27a19-186">En circunstancias normales, esto produce resultados satisfactorios.</span><span class="sxs-lookup"><span data-stu-id="27a19-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="27a19-187">Sin embargo, cuando la aplicación presenta el modo de pantalla completa, como es habitual para los juegos, las ventanas estándar ya no funcionan y es posible que no se muestren en la parte superior de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27a19-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="27a19-188">Para solucionar este problema, la aplicación debe dibujar las ventanas del IME en lugar de basarse en Windows para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="27a19-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="27a19-189">Cuando el comportamiento de creación de la ventana del IME predeterminado no proporciona lo que una aplicación requiere, la aplicación puede invalidar el control de ventanas del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="27a19-190">Una aplicación puede lograr esto mediante el procesamiento de mensajes relacionados con el IME y la llamada a la API del [Administrador de métodos de entrada](/windows/desktop/Intl/input-method-manager) (IMM).</span><span class="sxs-lookup"><span data-stu-id="27a19-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="27a19-191">Cuando un usuario interactúa con un IME para escribir caracteres complejos, el IMM envía mensajes a la aplicación para notificarle eventos importantes, como iniciar una composición o Mostrar la ventana candidata.</span><span class="sxs-lookup"><span data-stu-id="27a19-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="27a19-192">Normalmente, una aplicación omite estos mensajes y los pasa al controlador de mensajes predeterminado, lo que hace que el IME los controle.</span><span class="sxs-lookup"><span data-stu-id="27a19-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="27a19-193">Cuando la aplicación, en lugar del controlador predeterminado, controla los mensajes, controla exactamente lo que sucede en cada uno de los eventos del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="27a19-194">A menudo, el controlador de mensajes recupera el contenido de las distintas ventanas del IME mediante una llamada a la API de IMM.</span><span class="sxs-lookup"><span data-stu-id="27a19-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="27a19-195">Una vez que la aplicación tenga esta información, puede dibujar correctamente las propias ventanas del IME cuando sea necesario representarlas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="27a19-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="27a19-196">Functions</span><span class="sxs-lookup"><span data-stu-id="27a19-196">Functions</span></span>

<span data-ttu-id="27a19-197">Un IME debe obtener la cadena de lectura, ocultar la ventana de lectura y obtener la orientación de la ventana de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="27a19-198">En esta tabla se muestran las funcionalidades por versión de IME:</span><span class="sxs-lookup"><span data-stu-id="27a19-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="27a19-199">Obteniendo cadena de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-199">Getting reading string</span></span>                                                | <span data-ttu-id="27a19-200">Ocultar la ventana de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-200">Hiding reading window</span></span>                       | <span data-ttu-id="27a19-201">Orientación de la ventana de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="27a19-202">Antes de la versión 6,0</span><span class="sxs-lookup"><span data-stu-id="27a19-202">Before version 6.0</span></span> | <span data-ttu-id="27a19-203">A.</span><span class="sxs-lookup"><span data-stu-id="27a19-203">A.</span></span> <span data-ttu-id="27a19-204">Leer datos privados del IME de acceso a la ventana directamente.</span><span class="sxs-lookup"><span data-stu-id="27a19-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="27a19-205">Vea "4 Structure"</span><span class="sxs-lookup"><span data-stu-id="27a19-205">See "4 Structure"</span></span> | <span data-ttu-id="27a19-206">Interceptar mensajes privados del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-206">Trap IME private messages.</span></span> <span data-ttu-id="27a19-207">Vea "3 mensajes"</span><span class="sxs-lookup"><span data-stu-id="27a19-207">See "3 Messages"</span></span> | <span data-ttu-id="27a19-208">Examine la información del registro.</span><span class="sxs-lookup"><span data-stu-id="27a19-208">Examine registry information.</span></span> <span data-ttu-id="27a19-209">Consulte "5 información del registro"</span><span class="sxs-lookup"><span data-stu-id="27a19-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="27a19-210">Después de la versión 6,0</span><span class="sxs-lookup"><span data-stu-id="27a19-210">After version 6.0</span></span>  | [<span data-ttu-id="27a19-211">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="27a19-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="27a19-212">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="27a19-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="27a19-213">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="27a19-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="27a19-214">error de Hadoop</span><span class="sxs-lookup"><span data-stu-id="27a19-214">Messages</span></span>

<span data-ttu-id="27a19-215">No es necesario procesar los siguientes mensajes para el IME más reciente que implementa [ShowReadingWindow](#showreadingwindow)().</span><span class="sxs-lookup"><span data-stu-id="27a19-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="27a19-216">Los mensajes siguientes se capturan mediante el controlador de mensajes de la aplicación (es decir, no se pasan a DefWindowProc) para impedir que se muestre la ventana de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="27a19-217">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="27a19-217">Examples</span></span>

<span data-ttu-id="27a19-218">En los siguientes ejemplos se muestra cómo obtener información de cadena de lectura de IME anterior que no tiene GetReadingString ().</span><span class="sxs-lookup"><span data-stu-id="27a19-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="27a19-219">El código genera las siguientes salidas:</span><span class="sxs-lookup"><span data-stu-id="27a19-219">The code generates the following outputs:</span></span>



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27a19-220">DWORD dwlen</span><span class="sxs-lookup"><span data-stu-id="27a19-220">DWORD dwlen</span></span>  | <span data-ttu-id="27a19-221">Longitud de la cadena de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-221">Length of the reading string</span></span>                                                          |
| <span data-ttu-id="27a19-222">DWORD dwerr</span><span class="sxs-lookup"><span data-stu-id="27a19-222">DWORD dwerr</span></span>  | <span data-ttu-id="27a19-223">Índice de carácter de error</span><span class="sxs-lookup"><span data-stu-id="27a19-223">Index of error char</span></span>                                                                   |
| <span data-ttu-id="27a19-224">LPWSTR wstr</span><span class="sxs-lookup"><span data-stu-id="27a19-224">LPWSTR wstr</span></span>  | <span data-ttu-id="27a19-225">Puntero a la cadena de lectura</span><span class="sxs-lookup"><span data-stu-id="27a19-225">Pointer to the reading string</span></span>                                                         |
| <span data-ttu-id="27a19-226">BOOL Unicode</span><span class="sxs-lookup"><span data-stu-id="27a19-226">BOOL unicode</span></span> | <span data-ttu-id="27a19-227">Si es true, la cadena de lectura está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="27a19-227">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="27a19-228">En caso contrario, tiene el formato multibyte.</span><span class="sxs-lookup"><span data-stu-id="27a19-228">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="27a19-229">CHT IME versión 4,2, 4,3 y 4,4</span><span class="sxs-lookup"><span data-stu-id="27a19-229">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="27a19-230">CHT IME versión 5,0</span><span class="sxs-lookup"><span data-stu-id="27a19-230">CHT IME version 5.0</span></span>

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

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="27a19-231">Chino tradicional versión 5,1, 5,2 y CHS IME versión 5,3</span><span class="sxs-lookup"><span data-stu-id="27a19-231">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

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

### <a name="chs-ime-version-41"></a><span data-ttu-id="27a19-232">CHS IME versión 4,1</span><span class="sxs-lookup"><span data-stu-id="27a19-232">CHS IME version 4.1</span></span>

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

### <a name="chs-ime-version-42"></a><span data-ttu-id="27a19-233">CHS IME versión 4,2</span><span class="sxs-lookup"><span data-stu-id="27a19-233">CHS IME version 4.2</span></span>

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

## <a name="ime-messages"></a><span data-ttu-id="27a19-234">Mensajes IME</span><span class="sxs-lookup"><span data-stu-id="27a19-234">IME Messages</span></span>

<span data-ttu-id="27a19-235">Una aplicación de pantalla completa debe administrar correctamente los siguientes mensajes relacionados con el IME:</span><span class="sxs-lookup"><span data-stu-id="27a19-235">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="27a19-236">INPUTLANGCHANGE de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-236">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="27a19-237">El IMM envía un \_ mensaje de WM INPUTLANGCHANGE a la ventana activa de una aplicación después de que el usuario haya cambiado la configuración regional de entrada con una combinación de teclas (normalmente Alt + Mayús) o con el indicador de configuración regional de entrada en la barra de tareas o en la barra de idioma.</span><span class="sxs-lookup"><span data-stu-id="27a19-237">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="27a19-238">La barra de idioma es un control en pantalla con el que el usuario puede configurar un servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="27a19-238">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="27a19-239">(Vea [Cómo mostrar la barra de idioma](/windows/desktop/TSF/how-to-set-up-tsf)). En la captura de pantalla siguiente se muestra una lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="27a19-239">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![lista de selección de idioma que se muestra cuando el usuario hace clic en el indicador de configuración regional](images/ime-langselection.png)

<span data-ttu-id="27a19-241">Cuando el IMM envía un mensaje de WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox debe realizar varias tareas importantes:</span><span class="sxs-lookup"><span data-stu-id="27a19-241">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="27a19-242">Se llama al método GetKeyboardLayout para devolver el identificador de configuración regional (ID.) de entrada para el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27a19-242">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="27a19-243">La clase CDXUTIMEEditBox guarda este identificador en su variable miembro estática s \_ hklCurrent para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="27a19-243">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="27a19-244">Es importante que la aplicación Conozca la configuración regional de entrada actual, ya que el IME para cada idioma tiene su propio comportamiento distinto.</span><span class="sxs-lookup"><span data-stu-id="27a19-244">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="27a19-245">El desarrollador puede tener que proporcionar un código diferente para las diferentes configuraciones regionales de entrada.</span><span class="sxs-lookup"><span data-stu-id="27a19-245">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="27a19-246">CDXUTIMEEditBox Inicializa una cadena para mostrarla en el indicador de idioma del cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-246">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="27a19-247">Este indicador puede mostrar el idioma de entrada activo cuando la aplicación se ejecuta en modo de pantalla completa y no está visible la barra de tareas ni la barra de idioma.</span><span class="sxs-lookup"><span data-stu-id="27a19-247">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="27a19-248">Se llama al método ImmGetConversionStatus para indicar si la configuración regional de entrada está en modo de conversión nativo o no nativo.</span><span class="sxs-lookup"><span data-stu-id="27a19-248">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="27a19-249">El modo de conversión nativo permite al usuario escribir texto en el idioma elegido.</span><span class="sxs-lookup"><span data-stu-id="27a19-249">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="27a19-250">El modo de conversión no nativo hace que el teclado actúe como un teclado estándar en inglés.</span><span class="sxs-lookup"><span data-stu-id="27a19-250">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="27a19-251">Es importante proporcionar una indicación visual al usuario sobre el tipo de modo de conversión en el que se encuentra el IME, de modo que el usuario pueda saber fácilmente qué caracteres se deben esperar al golpear una tecla.</span><span class="sxs-lookup"><span data-stu-id="27a19-251">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="27a19-252">CDXUTIMEEditBox proporciona esta indicación visual con un color de indicador de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="27a19-252">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="27a19-253">Cuando la configuración regional de entrada usa un IME con el modo de conversión nativo, la clase CDXUTIMEEditBox dibuja el texto del indicador con el color definido por el \_ parámetro m IndicatorImeColor.</span><span class="sxs-lookup"><span data-stu-id="27a19-253">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="27a19-254">Cuando el IME está en modo de conversión no nativo, o no se usa ningún IME, la clase dibuja el texto del indicador con el color definido por el \_ parámetro m IndicatorEngColor.</span><span class="sxs-lookup"><span data-stu-id="27a19-254">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="27a19-255">CDXUTIMEEditBox comprueba la configuración regional de entrada y establece el valor de la variable miembro estática s \_ bInsertOnType en true para coreano y false para todos los demás idiomas.</span><span class="sxs-lookup"><span data-stu-id="27a19-255">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="27a19-256">Esta marca es necesaria debido a los distintos comportamientos de los IME de Coreano y de todos los demás IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-256">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="27a19-257">Al escribir caracteres en idiomas distintos del coreano, el texto escrito por el usuario se muestra en la ventana de composición y el usuario puede cambiar libremente el contenido de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-257">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="27a19-258">El usuario presiona la tecla entrar cuando está satisfecho con la cadena de composición y la cadena de composición se envía a la aplicación como una serie de mensajes de tipo char de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="27a19-258">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="27a19-259">Sin embargo, en los IME de Coreano, cuando un usuario presiona una tecla para escribir texto, se envía inmediatamente un carácter a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27a19-259">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="27a19-260">Cuando el usuario presiona más teclas para modificar el carácter inicial, el carácter del cuadro de edición cambia para reflejar entradas adicionales del usuario.</span><span class="sxs-lookup"><span data-stu-id="27a19-260">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="27a19-261">Esencialmente, el usuario está creando caracteres en el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-261">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="27a19-262">Estos dos comportamientos son lo suficientemente diferentes como para que CDXUTIMEEditBox deba codificar cada uno de ellos de forma específica.</span><span class="sxs-lookup"><span data-stu-id="27a19-262">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="27a19-263">Se llama al método miembro estático SetupImeApi para recuperar direcciones de dos funciones del módulo IME: GetReadingString y ShowReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="27a19-263">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="27a19-264">Si estas funciones existen, se llama a ShowReadingWindow para ocultar la ventana de lectura predeterminada para este IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-264">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="27a19-265">Dado que la aplicación representa la propia ventana de lectura, notifica al IME que deshabilite el dibujo de la ventana de lectura predeterminada para que no interfiera con la representación a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="27a19-265">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="27a19-266">El IMM envía un \_ mensaje de de WM IME en el que \_ se activa una ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27a19-266">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="27a19-267">El parámetro lParam de este mensaje contiene una marca que indica al IME Qué ventanas se deben dibujar y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="27a19-267">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="27a19-268">Dado que la aplicación controla todo el dibujo, no es necesario que el IME dibuje ninguna de las ventanas del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-268">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="27a19-269">Por lo tanto, el controlador de mensajes de la aplicación simplemente establece lParam en 0 y devuelve.</span><span class="sxs-lookup"><span data-stu-id="27a19-269">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="27a19-270">Para que las aplicaciones admitan el IME, se necesita un procesamiento especial para el mensaje relacionado con el IME de WM \_ IME \_ .</span><span class="sxs-lookup"><span data-stu-id="27a19-270">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="27a19-271">Puesto que Windows normalmente envía este mensaje a la aplicación antes de llamar al método PanoramaInitialize (), panorama no tiene la oportunidad de procesar la interfaz de usuario para mostrar las ventanas de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="27a19-271">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="27a19-272">El siguiente fragmento de código especifica a las aplicaciones de Windows que no muestren ninguna interfaz de usuario asociada a la ventana de lista de candidatos, lo que permite que panorama controle específicamente esta interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="27a19-272">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="27a19-273">\_STARTCOMPOSITION de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-273">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="27a19-274">El IMM envía un \_ \_ mensaje STARTCOMPOSITION del IME de WM a la aplicación cuando la composición del IME está a punto de comenzar como resultado de las pulsaciones de tecla del usuario.</span><span class="sxs-lookup"><span data-stu-id="27a19-274">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="27a19-275">Si el IME usa la ventana de composición, muestra la cadena de composición actual en una ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-275">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="27a19-276">CDXUTIMEEditBox controla este mensaje mediante la realización de dos tareas:</span><span class="sxs-lookup"><span data-stu-id="27a19-276">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="27a19-277">CDXUTIMEEditBox borra el búfer de la cadena de composición y el búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="27a19-277">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="27a19-278">Estos búferes son miembros estáticos de CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="27a19-278">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="27a19-279">CDXUTIMEEditBox establece la \_ variable de miembro estático s bHideCaret en true.</span><span class="sxs-lookup"><span data-stu-id="27a19-279">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="27a19-280">Este miembro, definido en la clase base CDXUTEditBox, controla si se debe dibujar el cursor en el cuadro de edición cuando se represente el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-280">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="27a19-281">La ventana composición funciona de forma similar a un cuadro de edición con texto y cursor.</span><span class="sxs-lookup"><span data-stu-id="27a19-281">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="27a19-282">Para evitar confusiones cuando la ventana de composición está visible, el cuadro de edición oculta su cursor para que solo un cursor esté visible a la vez.</span><span class="sxs-lookup"><span data-stu-id="27a19-282">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="27a19-283">\_composición del IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-283">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="27a19-284">El IMM envía un \_ mensaje de \_ composición del IME de WM a la aplicación cuando el usuario escribe una pulsación de tecla para cambiar la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-284">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="27a19-285">El valor de lParam indica qué tipo de información puede recuperar la aplicación del administrador de métodos de entrada (IMM).</span><span class="sxs-lookup"><span data-stu-id="27a19-285">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="27a19-286">La aplicación debe recuperar la información disponible mediante una llamada a [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) y, a continuación, debe guardar la información en su búfer privado para que pueda representar los elementos IME más adelante.</span><span class="sxs-lookup"><span data-stu-id="27a19-286">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="27a19-287">CDXUTIMEEditBox comprueba y recupera los datos de la cadena de composición siguientes:</span><span class="sxs-lookup"><span data-stu-id="27a19-287">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="27a19-288">[**WM \_ Valor \_**](/windows/desktop/Intl/wm-ime-composition) de marca lParam de composición de IME</span><span class="sxs-lookup"><span data-stu-id="27a19-288">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="27a19-289">data</span><span class="sxs-lookup"><span data-stu-id="27a19-289">Data</span></span>                           | <span data-ttu-id="27a19-290">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a19-290">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a19-291">GC \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="27a19-291">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="27a19-292">Atributo de composición</span><span class="sxs-lookup"><span data-stu-id="27a19-292">Composition Attribute</span></span>          | <span data-ttu-id="27a19-293">Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido).</span><span class="sxs-lookup"><span data-stu-id="27a19-293">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="27a19-294">Esta información es necesaria porque CDXUTIMEEditBox colorea los caracteres de cadena de composición de manera diferente en función de sus atributos.</span><span class="sxs-lookup"><span data-stu-id="27a19-294">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="27a19-295">GC \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="27a19-295">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="27a19-296">Información de la cláusula de composición</span><span class="sxs-lookup"><span data-stu-id="27a19-296">Composition Clause Information</span></span> | <span data-ttu-id="27a19-297">Esta información de la cláusula se utiliza cuando el IME japonés está activo.</span><span class="sxs-lookup"><span data-stu-id="27a19-297">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="27a19-298">Cuando se convierte una cadena de composición en japonés, los caracteres se pueden agrupar como una cláusula que se convierte en una sola entidad.</span><span class="sxs-lookup"><span data-stu-id="27a19-298">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="27a19-299">Cuando el usuario mueve el cursor, CDXUTIMEEditBox usa esta información para resaltar la cláusula completa, en lugar de simplemente un carácter único dentro de la cláusula.</span><span class="sxs-lookup"><span data-stu-id="27a19-299">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="27a19-300">GC \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="27a19-300">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="27a19-301">Cadena de composición</span><span class="sxs-lookup"><span data-stu-id="27a19-301">Composition String</span></span>             | <span data-ttu-id="27a19-302">Esta cadena es la cadena actualizada que está compuesta por el usuario.</span><span class="sxs-lookup"><span data-stu-id="27a19-302">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="27a19-303">Esta es también la cadena mostrada en la ventana de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-303">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="27a19-304">GC \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="27a19-304">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="27a19-305">Posición del cursor de composición</span><span class="sxs-lookup"><span data-stu-id="27a19-305">Composition Cursor Position</span></span>    | <span data-ttu-id="27a19-306">La ventana composición implementa un cursor, similar al cursor en un cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-306">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="27a19-307">La aplicación puede recuperar la posición del cursor al procesar el \_ \_ mensaje de composición del IME de WM para dibujar el cursor correctamente.</span><span class="sxs-lookup"><span data-stu-id="27a19-307">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="27a19-308">RESULTSTR de GC \_</span><span class="sxs-lookup"><span data-stu-id="27a19-308">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="27a19-309">Cadena de resultado</span><span class="sxs-lookup"><span data-stu-id="27a19-309">Result String</span></span>                  | <span data-ttu-id="27a19-310">La cadena de resultado está disponible cuando el usuario está a punto de completar el proceso de composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-310">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="27a19-311">Esta cadena debe recuperarse y los caracteres deben enviarse al cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-311">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="27a19-312">\_ENDCOMPOSITION de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-312">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="27a19-313">El IMM envía un \_ \_ mensaje ENDCOMPOSITION del IME de WM a la aplicación cuando finaliza la operación de composición del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-313">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="27a19-314">Esto puede ocurrir cuando el usuario presiona la tecla entrar para aprobar la cadena de composición o la tecla ESC para cancelar la composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-314">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="27a19-315">CDXUTIMEEditBox controla este mensaje estableciendo el búfer de cadena de composición en blanco.</span><span class="sxs-lookup"><span data-stu-id="27a19-315">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="27a19-316">A continuación, establece s \_ bHideCaret en false porque la ventana de composición está cerrada y el cursor en el cuadro de edición debe estar visible de nuevo.</span><span class="sxs-lookup"><span data-stu-id="27a19-316">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="27a19-317">El controlador de mensajes CDXUTIMEEditBox también establece s \_ bShowReadingWindow en false.</span><span class="sxs-lookup"><span data-stu-id="27a19-317">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="27a19-318">Esta marca controla si la clase dibuja la ventana de lectura cuando el cuadro de edición se representa a sí mismo, por lo que debe establecerse en FALSE cuando finaliza una composición.</span><span class="sxs-lookup"><span data-stu-id="27a19-318">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="27a19-319">\_notificación de IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="27a19-319">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="27a19-320">El IMM envía un \_ mensaje de notificación del IME de WM \_ a la aplicación cada vez que cambia una ventana del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-320">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="27a19-321">Una aplicación que controla el dibujo de las ventanas del IME debe procesar este mensaje para que sea consciente de cualquier actualización del contenido de la ventana.</span><span class="sxs-lookup"><span data-stu-id="27a19-321">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="27a19-322">WParam indica el comando o el cambio que se está llevando a cabo.</span><span class="sxs-lookup"><span data-stu-id="27a19-322">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="27a19-323">CDXUTIMEEditBox controla los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="27a19-323">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27a19-324">Comando IME</span><span class="sxs-lookup"><span data-stu-id="27a19-324">IME Command</span></span></th>
<th><span data-ttu-id="27a19-325">Descripción</span><span class="sxs-lookup"><span data-stu-id="27a19-325">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27a19-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="27a19-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="27a19-327">Este atributo contiene información como el estado de cada carácter de la cadena de composición (por ejemplo, convertido o no convertido).</span><span class="sxs-lookup"><span data-stu-id="27a19-327">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="27a19-328">Esta información es necesaria porque CDXUTIMEEditBox colorea los caracteres de cadena de composición de manera diferente en función de sus atributos.</span><span class="sxs-lookup"><span data-stu-id="27a19-328">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27a19-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="27a19-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="27a19-330">Se envía a la aplicación cuando la ventana candidata está a punto de abrirse o actualizarse, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="27a19-330">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="27a19-331">La ventana candidata se abre cuando un usuario desea cambiar la opción de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="27a19-331">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="27a19-332">La ventana se actualiza cuando un usuario mueve el indicador de selección o cambia la página.</span><span class="sxs-lookup"><span data-stu-id="27a19-332">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="27a19-333">CDXUTIMEEditBox usa un controlador de mensajes para ambos comandos, ya que las tareas necesarias son exactamente iguales:</span><span class="sxs-lookup"><span data-stu-id="27a19-333">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="27a19-334">CDXUTIMEEditBox establece el miembro bShowWindow de la estructura de la lista de candidatos s_CandList en TRUE para indicar que la ventana candidata debe dibujarse durante la representación del marco.</span><span class="sxs-lookup"><span data-stu-id="27a19-334">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="27a19-335">CDXUTIMEEditBox recupera la lista de candidatos llamando a <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, primero para obtener el tamaño de búfer necesario y, después, de nuevo para obtener los datos reales.</span><span class="sxs-lookup"><span data-stu-id="27a19-335">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="27a19-336">La estructura de la lista de candidatos privados s_CandList se inicializa con los datos candidatos recuperados.</span><span class="sxs-lookup"><span data-stu-id="27a19-336">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="27a19-337">Las cadenas candidatas se almacenan como una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="27a19-337">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="27a19-338">Se guarda el índice de la entrada seleccionada, así como el índice de la página.</span><span class="sxs-lookup"><span data-stu-id="27a19-338">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="27a19-339">CDXUTIMEEditBox comprueba si el estilo de ventana candidata es vertical u horizontal.</span><span class="sxs-lookup"><span data-stu-id="27a19-339">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="27a19-340">Si el estilo de ventana es horizontal, se debe inicializar un búfer de cadena adicional, el miembro HoriCand de s_CandList, con todas las cadenas candidatas, con caracteres de espacio insertados entre todas las cadenas adyacentes.</span><span class="sxs-lookup"><span data-stu-id="27a19-340">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="27a19-341">Al representar una ventana de candidato vertical, las cadenas candidatas individuales se dibujan de una en una, con las coordenadas y incrementadas para cada cadena.</span><span class="sxs-lookup"><span data-stu-id="27a19-341">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="27a19-342">Sin embargo, esta cadena HoriCand se debe usar al representar una ventana candidata horizontal, porque el carácter de espacio es la mejor manera de separar dos cadenas adyacentes en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="27a19-342">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27a19-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="27a19-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="27a19-344">Se envía a la aplicación cuando una ventana candidata está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="27a19-344">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="27a19-345">Esto sucede cuando un usuario ha realizado una selección de la lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="27a19-345">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="27a19-346">CDXUTIMEEditBox controla este comando estableciendo la marca visible de la ventana candidata en FALSE y, a continuación, borrando el búfer de la cadena candidata.</span><span class="sxs-lookup"><span data-stu-id="27a19-346">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27a19-347">IMN_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="27a19-347">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="27a19-348">Se envía a la aplicación cuando el IME ha actualizado su cadena de lectura como resultado de que el usuario escriba o quite caracteres.</span><span class="sxs-lookup"><span data-stu-id="27a19-348">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="27a19-349">La aplicación debe recuperar la cadena de lectura y guardarla para su representación.</span><span class="sxs-lookup"><span data-stu-id="27a19-349">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="27a19-350">CDXUTIMEEditBox tiene dos métodos para recuperar la cadena de lectura, en función de cómo se admiten las cadenas de lectura en el IME:</span><span class="sxs-lookup"><span data-stu-id="27a19-350">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="27a19-351">Si el IME admite la función GetReadingString, se llama a GetReadingString para recuperar la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-351">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="27a19-352">Si el IME no implementa GetReadingString, CDXUTIMEEditBox recupera la cadena de lectura del contenido del contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="27a19-352">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="27a19-353">Representación</span><span class="sxs-lookup"><span data-stu-id="27a19-353">Rendering</span></span>

<span data-ttu-id="27a19-354">La representación de los elementos y ventanas del IME es sencilla.</span><span class="sxs-lookup"><span data-stu-id="27a19-354">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="27a19-355">CDXUTIMEEditBox permite que la clase base se represente primero porque las ventanas de IME deben aparecer encima del control de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-355">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="27a19-356">Una vez representado el cuadro de edición base, CDXUTIMEEditBox comprueba la marca de visibilidad de cada ventana del IME (indicador, composición, candidato y ventana de lectura) y dibuja la ventana si debe estar visible.</span><span class="sxs-lookup"><span data-stu-id="27a19-356">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="27a19-357">Consulte comportamiento predeterminado del IME para obtener descripciones de los distintos tipos de ventana del IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-357">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="27a19-358">Indicador de configuración regional de entrada</span><span class="sxs-lookup"><span data-stu-id="27a19-358">Input Locale Indicator</span></span>

<span data-ttu-id="27a19-359">El indicador de configuración regional de entrada se representa antes que cualquier otra ventana de IME porque es un elemento que siempre se muestra.</span><span class="sxs-lookup"><span data-stu-id="27a19-359">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="27a19-360">Por lo tanto, debe aparecer debajo de otras ventanas IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-360">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="27a19-361">CDXUTIMEEditBox representa el indicador llamando al método RenderIndicator, en el que el color de la fuente del indicador se determina examinando la \_ variable estática de s, que refleja el modo de conversión del IME actual.</span><span class="sxs-lookup"><span data-stu-id="27a19-361">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="27a19-362">Cuando el IME está habilitado y la conversión nativa está activa, el método usa m \_ IndicatorImeColor como el color del indicador.</span><span class="sxs-lookup"><span data-stu-id="27a19-362">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="27a19-363">Si el IME está deshabilitado o está en modo de conversión no nativo, \_ se usa m IndicatorImeColor para dibujar el texto del indicador.</span><span class="sxs-lookup"><span data-stu-id="27a19-363">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="27a19-364">De forma predeterminada, la ventana de indicador en sí se dibuja a la derecha del cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-364">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="27a19-365">Las aplicaciones pueden cambiar este comportamiento invalidando el método RenderIndicator.</span><span class="sxs-lookup"><span data-stu-id="27a19-365">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="27a19-366">En la siguiente ilustración se muestran las distintas apariencias de un indicador de configuración regional de entrada para inglés, Japonés en modo de conversión alfanumérica y japonés en modo de conversión nativo:</span><span class="sxs-lookup"><span data-stu-id="27a19-366">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![diferentes aspectos de un indicador de configuración regional de entrada para inglés y japonés](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="27a19-368">Ventana composición</span><span class="sxs-lookup"><span data-stu-id="27a19-368">Composition Window</span></span>

<span data-ttu-id="27a19-369">El dibujo de la ventana de composición se controla en el método RenderComposition de CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="27a19-369">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="27a19-370">La ventana de composición flota sobre el cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="27a19-370">The composition window floats above the edit box.</span></span> <span data-ttu-id="27a19-371">Debe dibujarse en la posición del cursor del control de edición subyacente.</span><span class="sxs-lookup"><span data-stu-id="27a19-371">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="27a19-372">CDXUTIMEEditBox controla la representación de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="27a19-372">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="27a19-373">Toda la cadena de composición se dibuja utilizando los colores de la cadena de composición predeterminados.</span><span class="sxs-lookup"><span data-stu-id="27a19-373">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="27a19-374">Los caracteres con ciertos atributos especiales deben dibujarse en colores diferentes, por lo que CDXUTIMEEditBox revisa los caracteres de la cadena de composición e inspecciona el atributo de cadena.</span><span class="sxs-lookup"><span data-stu-id="27a19-374">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="27a19-375">Si el atributo llama a para distintos colores, el carácter se dibuja de nuevo con los colores adecuados.</span><span class="sxs-lookup"><span data-stu-id="27a19-375">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="27a19-376">Se dibuja el cursor de la ventana de composición para completar la representación.</span><span class="sxs-lookup"><span data-stu-id="27a19-376">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="27a19-377">El cursor debe parpadear en los IME de Coreano, pero no en otros IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-377">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="27a19-378">RenderComposition determina si el cursor debe ser visible en función de los valores de temporizador cuando se usa el IME Coreano.</span><span class="sxs-lookup"><span data-stu-id="27a19-378">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="27a19-379">Lecturas y ventanas candidatas</span><span class="sxs-lookup"><span data-stu-id="27a19-379">Reading and Candidate Windows</span></span>

<span data-ttu-id="27a19-380">Las ventanas de lectura y de candidatos se representan mediante el mismo método CDXUTIMEEditBox, RenderCandidateReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="27a19-380">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="27a19-381">Ambas ventanas contienen una matriz de cadenas para el diseño vertical o una sola cadena en el caso del diseño horizontal.</span><span class="sxs-lookup"><span data-stu-id="27a19-381">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="27a19-382">La mayor parte del código de RenderCandidateReadingWindow se usa para colocar la ventana de forma que ninguna parte de la ventana esté fuera de la ventana de la aplicación y se recorte.</span><span class="sxs-lookup"><span data-stu-id="27a19-382">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="27a19-383">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="27a19-383">Limitations</span></span>

<span data-ttu-id="27a19-384">A veces, los IME contienen características avanzadas para mejorar la facilidad de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="27a19-384">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="27a19-385">Algunas de las características que se encuentran en los IME más recientes se muestran en las siguientes figuras.</span><span class="sxs-lookup"><span data-stu-id="27a19-385">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="27a19-386">Estas características avanzadas no están presentes en DXUT.</span><span class="sxs-lookup"><span data-stu-id="27a19-386">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="27a19-387">La implementación de la compatibilidad con estas características avanzadas puede ser complicada, ya que no hay ninguna interfaz definida para obtener la información necesaria de los IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-387">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="27a19-388">IME de chino tradicional avanzado con lista de candidatos ampliada:</span><span class="sxs-lookup"><span data-stu-id="27a19-388">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![IME de chino tradicional avanzado con lista de candidatos ampliada](images/ime-advanced1.png)

<span data-ttu-id="27a19-390">IME japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir su significado:</span><span class="sxs-lookup"><span data-stu-id="27a19-390">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![IME japonés avanzado con algunas entradas candidatas que contienen texto adicional para describir su significado](images/ime-advanced2.png)

<span data-ttu-id="27a19-392">IME Coreano avanzado que incluye un sistema de reconocimiento de escritura a mano:</span><span class="sxs-lookup"><span data-stu-id="27a19-392">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![IME Coreano avanzado que incluye un sistema de reconocimiento de escritura a mano](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="27a19-394">Información del registro</span><span class="sxs-lookup"><span data-stu-id="27a19-394">Registry Information</span></span>

<span data-ttu-id="27a19-395">La siguiente información del registro se comprueba para determinar la orientación de la ventana de lectura, cuando el IME actual es anterior CHT nuevo Phonetic que no implementa GetReadingString ().</span><span class="sxs-lookup"><span data-stu-id="27a19-395">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="27a19-396">Clave</span><span class="sxs-lookup"><span data-stu-id="27a19-396">Key</span></span>                                                           | <span data-ttu-id="27a19-397">Value</span><span class="sxs-lookup"><span data-stu-id="27a19-397">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="27a19-398">HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ Name</span><span class="sxs-lookup"><span data-stu-id="27a19-398">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="27a19-399">asignación de teclado</span><span class="sxs-lookup"><span data-stu-id="27a19-399">keyboard mapping</span></span> |



 

<span data-ttu-id="27a19-400">Donde: \_ el nombre del IME es MSTCIPH si la versión del archivo IME es 5,1 o posterior; en caso contrario, el nombre del IME \_ es TINTLGNT.</span><span class="sxs-lookup"><span data-stu-id="27a19-400">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="27a19-401">La orientación de la ventana de lectura es horizontal si:</span><span class="sxs-lookup"><span data-stu-id="27a19-401">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="27a19-402">El IME tiene la versión 5,0 y el valor de asignación de teclado es 0x22 o 0x23</span><span class="sxs-lookup"><span data-stu-id="27a19-402">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="27a19-403">El IME es la versión 5,1 o la versión 5,2 y el valor de asignación de teclado es 0x22, 0x23 o 0x24.</span><span class="sxs-lookup"><span data-stu-id="27a19-403">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="27a19-404">Si no se cumple ninguna de las condiciones, la ventana de lectura es vertical.</span><span class="sxs-lookup"><span data-stu-id="27a19-404">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="27a19-405">Apéndice A: versiones CHT por sistema operativo</span><span class="sxs-lookup"><span data-stu-id="27a19-405">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="27a19-406">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="27a19-406">Operating System</span></span>           | <span data-ttu-id="27a19-407">Versión de IME de CHT</span><span class="sxs-lookup"><span data-stu-id="27a19-407">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="27a19-408">Windows 98</span><span class="sxs-lookup"><span data-stu-id="27a19-408">Windows 98</span></span>                 | <span data-ttu-id="27a19-409">4,2</span><span class="sxs-lookup"><span data-stu-id="27a19-409">4.2</span></span>             |
| <span data-ttu-id="27a19-410">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="27a19-410">Windows 2000</span></span>               | <span data-ttu-id="27a19-411">4.3</span><span class="sxs-lookup"><span data-stu-id="27a19-411">4.3</span></span>             |
| <span data-ttu-id="27a19-412">unknown</span><span class="sxs-lookup"><span data-stu-id="27a19-412">unknown</span></span>                    | <span data-ttu-id="27a19-413">4.4.</span><span class="sxs-lookup"><span data-stu-id="27a19-413">4.4</span></span>             |
| <span data-ttu-id="27a19-414">Windows ME</span><span class="sxs-lookup"><span data-stu-id="27a19-414">Windows ME</span></span>                 | <span data-ttu-id="27a19-415">5.0</span><span class="sxs-lookup"><span data-stu-id="27a19-415">5.0</span></span>             |
| <span data-ttu-id="27a19-416">Office XP</span><span class="sxs-lookup"><span data-stu-id="27a19-416">Office XP</span></span>                  | <span data-ttu-id="27a19-417">5,1</span><span class="sxs-lookup"><span data-stu-id="27a19-417">5.1</span></span>             |
| <span data-ttu-id="27a19-418">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27a19-418">Windows XP</span></span>                 | <span data-ttu-id="27a19-419">5.2</span><span class="sxs-lookup"><span data-stu-id="27a19-419">5.2</span></span>             |
| <span data-ttu-id="27a19-420">Downloadble web independiente</span><span class="sxs-lookup"><span data-stu-id="27a19-420">Standalone web downloadble</span></span> | <span data-ttu-id="27a19-421">6.0</span><span class="sxs-lookup"><span data-stu-id="27a19-421">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="27a19-422">Información adicional</span><span class="sxs-lookup"><span data-stu-id="27a19-422">Further Information</span></span>

<span data-ttu-id="27a19-423">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="27a19-423">For additional information, see the following:</span></span>

-   [<span data-ttu-id="27a19-424">Instalación y uso de editores de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="27a19-424">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="27a19-425">Presentación de texto internacional</span><span class="sxs-lookup"><span data-stu-id="27a19-425">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="27a19-426">El consorcio Unicode</span><span class="sxs-lookup"><span data-stu-id="27a19-426">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="27a19-427">Desarrollo de software internacional.</span><span class="sxs-lookup"><span data-stu-id="27a19-427">Developing International Software.</span></span> <span data-ttu-id="27a19-428">Dr. International.</span><span class="sxs-lookup"><span data-stu-id="27a19-428">Dr. International.</span></span> <span data-ttu-id="27a19-429">2a ed.</span><span class="sxs-lookup"><span data-stu-id="27a19-429">2nd ed.</span></span> <span data-ttu-id="27a19-430">Redmond, WA: Microsoft Press, 2003.</span><span class="sxs-lookup"><span data-stu-id="27a19-430">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="27a19-431">GetReadingString</span><span class="sxs-lookup"><span data-stu-id="27a19-431">GetReadingString</span></span>

<span data-ttu-id="27a19-432">Obtiene la información de la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-432">Gets reading string information.</span></span>

<span data-ttu-id="27a19-433">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="27a19-433">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="27a19-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="27a19-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-435">\[en el \] contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="27a19-435">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span><span class="sxs-lookup"><span data-stu-id="27a19-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="27a19-437">\[en la \] longitud de lpwReadingBuf, en WCHAR.</span><span class="sxs-lookup"><span data-stu-id="27a19-437">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="27a19-438">Si es cero, significa que la longitud del búfer de lectura de consulta es.</span><span class="sxs-lookup"><span data-stu-id="27a19-438">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span><span class="sxs-lookup"><span data-stu-id="27a19-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-440">\[out \] devuelve una cadena de lectura (no un extremo cero).</span><span class="sxs-lookup"><span data-stu-id="27a19-440">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="27a19-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span><span class="sxs-lookup"><span data-stu-id="27a19-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-442">\[out \] devuelve el índice del carácter de error en la cadena de lectura si existe.</span><span class="sxs-lookup"><span data-stu-id="27a19-442">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span><span class="sxs-lookup"><span data-stu-id="27a19-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-444">\[\]si es true, la lectura de la interfaz de usuario es vertical.</span><span class="sxs-lookup"><span data-stu-id="27a19-444">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="27a19-445">De lo contrario, puMaxReadingLen horizontal.</span><span class="sxs-lookup"><span data-stu-id="27a19-445">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span><span class="sxs-lookup"><span data-stu-id="27a19-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-447">\[\]la longitud de la interfaz de usuario de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-447">\[out\] The reading UI length.</span></span> <span data-ttu-id="27a19-448">La longitud de lectura máxima no es fija. no depende solo de la distribución del teclado, sino también en el modo de entrada (por ejemplo, código interno, entrada suplente).</span><span class="sxs-lookup"><span data-stu-id="27a19-448">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="27a19-449">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="27a19-449">**Return Values**</span></span>

<span data-ttu-id="27a19-450">La longitud de la cadena de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-450">The reading string length.</span></span>

<span data-ttu-id="27a19-451">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="27a19-451">**Remarks**</span></span>

<span data-ttu-id="27a19-452">Si el valor devuelto es mayor que el valor de uReadingBufLen, todos los parámetros de salida no están definidos.</span><span class="sxs-lookup"><span data-stu-id="27a19-452">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="27a19-453">Esta función se implementa en la versión CHT de IME 6,0 o posterior, y la puede adquirir GetProcAddress en un identificador de módulo IME; ImmGetIMEFileName y LoadLibrary pueden adquirir el identificador del módulo IME.</span><span class="sxs-lookup"><span data-stu-id="27a19-453">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="27a19-454">**Requisitos**</span><span class="sxs-lookup"><span data-stu-id="27a19-454">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="27a19-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Encabezado**</span><span class="sxs-lookup"><span data-stu-id="27a19-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="27a19-456">Declarado en IMM. h.</span><span class="sxs-lookup"><span data-stu-id="27a19-456">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**</span><span class="sxs-lookup"><span data-stu-id="27a19-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="27a19-458">Use IMM. lib.</span><span class="sxs-lookup"><span data-stu-id="27a19-458">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="27a19-459">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="27a19-459">ShowReadingWindow</span></span>

<span data-ttu-id="27a19-460">Mostrar u ocultar la ventana de lectura.</span><span class="sxs-lookup"><span data-stu-id="27a19-460">Show (or hide) the reading window.</span></span>

<span data-ttu-id="27a19-461">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="27a19-461">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="27a19-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="27a19-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-463">\[en el \] contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="27a19-463">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="27a19-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="27a19-465">\[en \] establecido en true para mostrar la ventana de lectura (o false para ocultarla).</span><span class="sxs-lookup"><span data-stu-id="27a19-465">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="27a19-466">**Valores devueltos**</span><span class="sxs-lookup"><span data-stu-id="27a19-466">**Return Values**</span></span>

<span data-ttu-id="27a19-467">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="27a19-467">**Remarks**</span></span>

<span data-ttu-id="27a19-468">Devuelve TRUE si es correcto o FALSE si no lo está.</span><span class="sxs-lookup"><span data-stu-id="27a19-468">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="27a19-469">**Requisitos**</span><span class="sxs-lookup"><span data-stu-id="27a19-469">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="27a19-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Encabezado**</span><span class="sxs-lookup"><span data-stu-id="27a19-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="27a19-471">Declarado en IMM. h.</span><span class="sxs-lookup"><span data-stu-id="27a19-471">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="27a19-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importación**</span><span class="sxs-lookup"><span data-stu-id="27a19-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="27a19-473">Use IMM. lib.</span><span class="sxs-lookup"><span data-stu-id="27a19-473">Use Imm.lib.</span></span>

</dd> </dl>