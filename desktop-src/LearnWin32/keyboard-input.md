---
title: Entrada de teclado (introducción a Win32 y C++)
description: Entrada de teclado
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105678611"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="6b2e1-103">Entrada de teclado (introducción a Win32 y C++)</span><span class="sxs-lookup"><span data-stu-id="6b2e1-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="6b2e1-104">El teclado se usa para varios tipos de entrada distintos, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="6b2e1-105">Entrada de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-105">Character input.</span></span> <span data-ttu-id="6b2e1-106">Texto que el usuario escribe en un documento o cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="6b2e1-107">Métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-107">Keyboard shortcuts.</span></span> <span data-ttu-id="6b2e1-108">Trazos de tecla que invocan funciones de aplicación. por ejemplo, CTRL + O para abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="6b2e1-109">Comandos del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-109">System commands.</span></span> <span data-ttu-id="6b2e1-110">Trazos de tecla que invocan funciones del sistema; por ejemplo, ALT + TAB para cambiar de ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="6b2e1-111">Al pensar en la entrada de teclado, es importante recordar que un trazo de tecla no es lo mismo que un carácter.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="6b2e1-112">Por ejemplo, al presionar la tecla se podría producir cualquiera de los siguientes caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="6b2e1-113">a</span><span class="sxs-lookup"><span data-stu-id="6b2e1-113">a</span></span>
-   <span data-ttu-id="6b2e1-114">A</span><span class="sxs-lookup"><span data-stu-id="6b2e1-114">A</span></span>
-   <span data-ttu-id="6b2e1-115">á (si el teclado admite la combinación de signos diacríticos)</span><span class="sxs-lookup"><span data-stu-id="6b2e1-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="6b2e1-116">Además, si se mantiene presionada la tecla ALT, al presionar la tecla se produce ALT + A, que el sistema no trata como un carácter, sino como un comando del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="6b2e1-117">Códigos de tecla</span><span class="sxs-lookup"><span data-stu-id="6b2e1-117">Key Codes</span></span>

<span data-ttu-id="6b2e1-118">Al presionar una tecla, el hardware genera un *código de digitalización*.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="6b2e1-119">Los códigos de análisis varían de un teclado a otro, y hay códigos de exploración independientes para los eventos de clave y de clave.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="6b2e1-120">Casi nunca le interesarán los códigos de examen.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="6b2e1-121">El controlador de teclado traduce los códigos de análisis en *códigos de tecla virtual*.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="6b2e1-122">Los códigos de tecla virtual son independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="6b2e1-123">Al presionar la tecla de cualquier teclado, se genera el mismo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="6b2e1-124">En general, los códigos de tecla virtual no corresponden a códigos ASCII ni a ningún otro estándar de codificación de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="6b2e1-125">Esto es obvio si se piensa en él, ya que la misma clave puede generar caracteres diferentes (a, A, á á) y algunas teclas, como las teclas de función, no se corresponden con ningún carácter.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="6b2e1-126">Dicho esto, los siguientes códigos de clave virtual se asignan a equivalentes ASCII:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="6b2e1-127">de 0 a 9 claves = ASCII ' 0 ' – ' 9 ' (0x30 – 0x39)</span><span class="sxs-lookup"><span data-stu-id="6b2e1-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="6b2e1-128">De la a a la Z = ASCII ' A ' – ' Z ' (0x41 – 0x5A)</span><span class="sxs-lookup"><span data-stu-id="6b2e1-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="6b2e1-129">En algunos aspectos esta asignación es inestable, ya que nunca debe pensar en los códigos de tecla virtual como caracteres, por los motivos descritos.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="6b2e1-130">El archivo de encabezado WinUser. h define constantes para la mayoría de los códigos de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="6b2e1-131">Por ejemplo, el código de tecla virtual de la tecla de dirección izquierda es **VK \_ izquierdo** (0x25).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="6b2e1-132">Para obtener una lista completa de los códigos de tecla virtual, consulte [**códigos de clave virtual**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="6b2e1-133">No se ha definido ninguna constante para los códigos de tecla virtual que coincidan con los valores ASCII.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="6b2e1-134">Por ejemplo, el código de tecla virtual de una clave es 0x41, pero no hay ninguna constante denominada **VK \_ A**.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="6b2e1-135">En su lugar, basta con usar el valor numérico.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="6b2e1-136">Mensajes de Key-Down y Key-Up</span><span class="sxs-lookup"><span data-stu-id="6b2e1-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="6b2e1-137">Al presionar una tecla, la ventana que tiene el foco de teclado recibe uno de los mensajes siguientes.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="6b2e1-138">**SYSKEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b2e1-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="6b2e1-139">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b2e1-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="6b2e1-140">El mensaje de [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) indica una *clave del sistema*, que es un trazo de clave que invoca un comando del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="6b2e1-141">Hay dos tipos de clave del sistema:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-141">There are two types of system key:</span></span>

-   <span data-ttu-id="6b2e1-142">ALT + cualquier tecla</span><span class="sxs-lookup"><span data-stu-id="6b2e1-142">ALT + any key</span></span>
-   <span data-ttu-id="6b2e1-143">F10</span><span class="sxs-lookup"><span data-stu-id="6b2e1-143">F10</span></span>

<span data-ttu-id="6b2e1-144">La tecla F10 activa la barra de menús de una ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="6b2e1-145">Varias combinaciones de teclas ALT invocan comandos del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="6b2e1-146">Por ejemplo, ALT + TAB cambia a una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="6b2e1-147">Además, si una ventana tiene un menú, se puede utilizar la tecla ALT para activar los elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="6b2e1-148">Algunas combinaciones de teclas ALT no hacen nada.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="6b2e1-149">El resto de los trazos de clave se consideran claves que no son del sistema y generan el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="6b2e1-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="6b2e1-150">Esto incluye las teclas de función que no son F10.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="6b2e1-151">Cuando se libera una clave, el sistema envía un mensaje de tecla arriba correspondiente:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="6b2e1-152">**KEYUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b2e1-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="6b2e1-153">**SYSKEYUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6b2e1-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="6b2e1-154">Si mantiene presionada una tecla suficiente para iniciar la característica de repetición del teclado, el sistema envía varios mensajes de tecla presionada, seguidos de un único mensaje de tecla.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="6b2e1-155">En los cuatro mensajes de teclado descritos hasta el momento, el parámetro *wParam* contiene el código de la clave virtual de la clave.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="6b2e1-156">El parámetro *lParam* contiene información diversa empaquetada en 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="6b2e1-157">Normalmente no se necesita la información en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="6b2e1-158">Una marca que podría ser útil es el bit 30, la marca "estado de la clave anterior", que se establece en 1 para los mensajes de tecla presionados repetidos.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="6b2e1-159">Como implica el nombre, los trazos de clave del sistema están pensados principalmente para su uso por parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="6b2e1-160">Si intercepta el mensaje [**de \_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) , llame a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) después.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="6b2e1-161">De lo contrario, impedirá que el sistema operativo controle el comando.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="6b2e1-162">Mensajes de caracteres</span><span class="sxs-lookup"><span data-stu-id="6b2e1-162">Character Messages</span></span>

<span data-ttu-id="6b2e1-163">Los trazos de clave se convierten en caracteres por la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , que primero vimos en el [módulo 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="6b2e1-164">Esta función examina los mensajes de tecla presionada y los convierte en caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="6b2e1-165">Para cada carácter que se genera, la función **TranslateMessage** coloca un mensaje de [**WM \_ Char**](/windows/desktop/inputdev/wm-char) o [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) en la cola de mensajes de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="6b2e1-166">El parámetro *wParam* del mensaje contiene el carácter UTF-16.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="6b2e1-167">Como puede imaginar, los mensajes de los [**\_ caracteres de WM**](/windows/desktop/inputdev/wm-char) se generan a partir de mensajes [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) , mientras que los mensajes de [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) se generan a partir de mensajes [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) .</span><span class="sxs-lookup"><span data-stu-id="6b2e1-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="6b2e1-168">Por ejemplo, supongamos que el usuario presiona la tecla Mayús seguida de una tecla.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="6b2e1-169">Suponiendo una distribución de teclado estándar, obtendría la siguiente secuencia de mensajes:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="6b2e1-170">**WM \_ KEYDOWN**: Shift</span><span class="sxs-lookup"><span data-stu-id="6b2e1-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="6b2e1-171">**WM \_ KEYDOWN**: A</span><span class="sxs-lookup"><span data-stu-id="6b2e1-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="6b2e1-172">**WM \_ CARÁCTER**: ' A '</span><span class="sxs-lookup"><span data-stu-id="6b2e1-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="6b2e1-173">Por otro lado, la combinación ALT + P generaría:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="6b2e1-174">**WM \_ SYSKEYDOWN**: \_ menú VK</span><span class="sxs-lookup"><span data-stu-id="6b2e1-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="6b2e1-175">**WM \_ SYSKEYDOWN**: 0x50</span><span class="sxs-lookup"><span data-stu-id="6b2e1-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="6b2e1-176">**WM \_ SYSCHAR**: ' p '</span><span class="sxs-lookup"><span data-stu-id="6b2e1-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="6b2e1-177">**WM \_ SYSKEYUP**: 0x50</span><span class="sxs-lookup"><span data-stu-id="6b2e1-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="6b2e1-178">**WM \_ KEYUP**: \_ menú VK</span><span class="sxs-lookup"><span data-stu-id="6b2e1-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="6b2e1-179">(El código de la clave virtual para la tecla ALT se denomina VK \_ MENÚ para motivos históricos.)</span><span class="sxs-lookup"><span data-stu-id="6b2e1-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="6b2e1-180">El mensaje de [**\_ SYSCHAR de WM**](/windows/desktop/menurc/wm-syschar) indica un carácter del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="6b2e1-181">Al igual que con [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), normalmente debe pasar este mensaje directamente a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="6b2e1-182">De lo contrario, puede interferir con los comandos estándar del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="6b2e1-183">En concreto, no trate **WM \_ SYSCHAR** como texto que el usuario ha escrito.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="6b2e1-184">El mensaje de carácter de [**WM \_**](/windows/desktop/inputdev/wm-char) es lo que se suele considerar como entrada de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="6b2e1-185">El tipo de datos para el carácter es **WCHAR \_ t**, que representa un carácter Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="6b2e1-186">La entrada de caracteres puede incluir caracteres fuera del intervalo ASCII, especialmente con distribuciones de teclado que se usan habitualmente fuera del Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="6b2e1-187">Puede probar diferentes distribuciones de teclado si instala un teclado regional y, a continuación, usa la característica de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="6b2e1-188">Los usuarios también pueden instalar un editor de métodos de entrada (IME) para escribir scripts complejos, como caracteres japoneses, con un teclado estándar.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="6b2e1-189">Por ejemplo, si se usa un IME japonés para escribir el carácter katakana カ (ka), es posible que aparezcan los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="6b2e1-190">**WM \_ KEYDOWN**: VK \_ PROCESSKEY (tecla proceso de IME)</span><span class="sxs-lookup"><span data-stu-id="6b2e1-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="6b2e1-191">**WM \_ KEYUP**: 0x4B</span><span class="sxs-lookup"><span data-stu-id="6b2e1-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="6b2e1-192">**WM \_ KEYDOWN**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="6b2e1-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="6b2e1-193">**WM \_ KEYUP**: 0x41</span><span class="sxs-lookup"><span data-stu-id="6b2e1-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="6b2e1-194">**WM \_ KEYDOWN**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="6b2e1-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="6b2e1-195">**WM \_ CHAR**: カ</span><span class="sxs-lookup"><span data-stu-id="6b2e1-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="6b2e1-196">**WM \_ KEYUP**: VK \_ Return</span><span class="sxs-lookup"><span data-stu-id="6b2e1-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="6b2e1-197">Algunas combinaciones de teclas CTRL se traducen en caracteres de control ASCII.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="6b2e1-198">Por ejemplo, CTRL + A se convierte en el carácter ASCII Ctrl-A (SOH) (valor ASCII 0x01).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="6b2e1-199">En el caso de la entrada de texto, normalmente debería filtrar los caracteres de control.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="6b2e1-200">Además, evite usar [**WM \_ Char**](/windows/desktop/inputdev/wm-char) para implementar métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="6b2e1-201">En su lugar, use mensajes [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) o, incluso mejor, use una tabla de aceleradores.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="6b2e1-202">Las tablas de aceleradores se describen en el tema siguiente, [tablas de aceleradores](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="6b2e1-203">En el código siguiente se muestran los mensajes de teclado principales en el depurador.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="6b2e1-204">Pruebe a jugar con diferentes combinaciones de teclas y vea qué mensajes se generan.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="6b2e1-205">Mensajes de teclado Misceláneos</span><span class="sxs-lookup"><span data-stu-id="6b2e1-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="6b2e1-206">La mayoría de las aplicaciones pueden pasar por alto otros mensajes de teclado sin ningún riesgo.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="6b2e1-207">El mensaje de [**\_ DEADCHAR de WM**](/windows/desktop/inputdev/wm-deadchar) se envía para una clave combinada, como un diacrítico.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="6b2e1-208">Por ejemplo, en un teclado de idioma español, si escribe acento (') seguido de E, se genera el carácter é.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="6b2e1-209">El **\_ DEADCHAR de WM** se envía para el carácter de acento.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="6b2e1-210">El mensaje de [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="6b2e1-211">Permite a los programas ANSI recibir entradas de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="6b2e1-212">El carácter de carácter [**\_ \_ IME de WM**](/windows/desktop/Intl/wm-ime-char) se envía cuando un IME traduce una secuencia de teclas en caracteres.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="6b2e1-213">Se envía además del mensaje de [**\_ carácter**](/windows/desktop/inputdev/wm-char) normal de WM.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="6b2e1-214">Estado del teclado</span><span class="sxs-lookup"><span data-stu-id="6b2e1-214">Keyboard State</span></span>

<span data-ttu-id="6b2e1-215">Los mensajes del teclado están orientados a eventos.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="6b2e1-216">Es decir, recibe un mensaje cuando se produce algo interesante, como una pulsación de tecla, y el mensaje le indica lo que ha sucedido.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="6b2e1-217">Pero también puede probar el estado de una clave en cualquier momento llamando a la función [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="6b2e1-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="6b2e1-218">Por ejemplo, considere la posibilidad de detectar la combinación de hacer clic con el botón primario y la tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="6b2e1-219">Puede realizar un seguimiento del estado de la tecla ALT escuchando los mensajes de traza de teclas y almacenando una marca, pero [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) le evita los problemas.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="6b2e1-220">Cuando reciba el mensaje [**de \_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) , simplemente llame a **GetKeyState** como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6b2e1-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="6b2e1-221">El mensaje [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) toma un código de clave virtual como entrada y devuelve un conjunto de marcas de bits (en realidad, solo dos marcadores).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="6b2e1-222">El valor 0x8000 contiene la marca de bits que comprueba si la tecla está presionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="6b2e1-223">La mayoría de los teclados tienen dos teclas ALT, izquierda y derecha.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="6b2e1-224">En el ejemplo anterior se comprueba si alguna de ellas está presionada.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="6b2e1-225">También puede usar [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) para distinguir entre las instancias izquierda y derecha de las teclas Alt, Mayús o Ctrl.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="6b2e1-226">Por ejemplo, el código siguiente comprueba si se presiona la tecla ALT derecha.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="6b2e1-227">La función [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) es interesante porque informa de un estado de teclado *virtual* .</span><span class="sxs-lookup"><span data-stu-id="6b2e1-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="6b2e1-228">Este estado virtual se basa en el contenido de la cola de mensajes y se actualiza a medida que se quitan los mensajes de la cola.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="6b2e1-229">Cuando el programa procesa los mensajes de ventana, **GetKeyState** le proporciona una instantánea del teclado en el momento en que se puso en cola cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="6b2e1-230">Por ejemplo, si el último mensaje de la cola era [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** notifica el estado del teclado en el momento en que el usuario hizo clic con el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="6b2e1-231">Dado que [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) se basa en la cola de mensajes, también omite la entrada del teclado que se envió a otro programa.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="6b2e1-232">Si el usuario cambia a otro programa, **GetKeyState** omite cualquier pulsación de tecla que se envíe a ese programa.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="6b2e1-233">Si realmente desea conocer el estado físico inmediato del teclado, hay una función para eso: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="6b2e1-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="6b2e1-234">Sin embargo, para la mayoría del código de interfaz de usuario, la función correcta es **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="6b2e1-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="6b2e1-235">Siguientes</span><span class="sxs-lookup"><span data-stu-id="6b2e1-235">Next</span></span>

[<span data-ttu-id="6b2e1-236">Tablas de aceleradores</span><span class="sxs-lookup"><span data-stu-id="6b2e1-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
