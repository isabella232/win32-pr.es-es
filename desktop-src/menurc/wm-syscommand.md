---
title: Mensaje de WM_SYSCOMMAND (Winuser. h)
description: Una ventana recibe este mensaje cuando el usuario elige un comando en el menú ventana (anteriormente conocido como el menú del sistema o el control) o cuando el usuario elige el botón maximizar, el botón minimizar, el botón Restaurar o el botón Cerrar.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699960"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="956cb-104">Mensaje de SYSCOMMAND de WM \_</span><span class="sxs-lookup"><span data-stu-id="956cb-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="956cb-105">Una ventana recibe este mensaje cuando el usuario elige un comando en el menú **ventana** (anteriormente conocido como el menú del sistema o el control) o cuando el usuario elige el botón maximizar, el botón minimizar, el botón Restaurar o el botón Cerrar.</span><span class="sxs-lookup"><span data-stu-id="956cb-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="956cb-106">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="956cb-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="956cb-107">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) en github.</span><span class="sxs-lookup"><span data-stu-id="956cb-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="956cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="956cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="956cb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="956cb-110">El tipo de comando del sistema solicitado.</span><span class="sxs-lookup"><span data-stu-id="956cb-110">The type of system command requested.</span></span> <span data-ttu-id="956cb-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="956cb-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="956cb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="956cb-112">Value</span></span></th>
<th><span data-ttu-id="956cb-113">Significado</span><span class="sxs-lookup"><span data-stu-id="956cb-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="956cb-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-115">Cierra la ventana.</span><span class="sxs-lookup"><span data-stu-id="956cb-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="956cb-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-117">Cambia el cursor a un signo de interrogación con un puntero.</span><span class="sxs-lookup"><span data-stu-id="956cb-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="956cb-118">Si el usuario hace clic en un control en el cuadro de diálogo, el control recibe un mensaje de <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="956cb-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="956cb-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-120">Selecciona el elemento predeterminado; el usuario hizo doble clic en el menú ventana.</span><span class="sxs-lookup"><span data-stu-id="956cb-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="956cb-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-122">Activa la ventana asociada a la tecla de acceso rápido especificada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="956cb-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="956cb-123">El parámetro <em>lParam</em> identifica la ventana que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="956cb-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="956cb-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-125">Se desplaza horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="956cb-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="956cb-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-127">Indica si el protector de pantalla es seguro.</span><span class="sxs-lookup"><span data-stu-id="956cb-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="956cb-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-129">Recupera el menú ventana como resultado de una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="956cb-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="956cb-130">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="956cb-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="956cb-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-132">Maximiza la ventana.</span><span class="sxs-lookup"><span data-stu-id="956cb-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="956cb-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-134">Minimiza la ventana.</span><span class="sxs-lookup"><span data-stu-id="956cb-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="956cb-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-136">Establece el estado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="956cb-136">Sets the state of the display.</span></span> <span data-ttu-id="956cb-137">Este comando admite dispositivos que tienen características de ahorro de energía, como un equipo personal con batería.</span><span class="sxs-lookup"><span data-stu-id="956cb-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="956cb-138">El parámetro <em>lParam</em> puede tener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="956cb-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="956cb-139">-1 (la pantalla se enciende)</span><span class="sxs-lookup"><span data-stu-id="956cb-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="956cb-140">1 (la pantalla va a baja energía)</span><span class="sxs-lookup"><span data-stu-id="956cb-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="956cb-141">2 (la pantalla se está apagando)</span><span class="sxs-lookup"><span data-stu-id="956cb-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="956cb-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-143">Recupera el menú ventana como resultado de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="956cb-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="956cb-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-145">Mueve la ventana.</span><span class="sxs-lookup"><span data-stu-id="956cb-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="956cb-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-147">Se desplaza a la ventana siguiente.</span><span class="sxs-lookup"><span data-stu-id="956cb-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="956cb-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-149">Se desplaza a la ventana anterior.</span><span class="sxs-lookup"><span data-stu-id="956cb-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="956cb-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-151">Restaura la ventana a su posición y tamaño normales.</span><span class="sxs-lookup"><span data-stu-id="956cb-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="956cb-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-153">Ejecuta la aplicación de protector de pantalla especificada en la sección [boot] del archivo de System.ini.</span><span class="sxs-lookup"><span data-stu-id="956cb-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="956cb-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-155">Ajusta el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="956cb-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="956cb-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-157">Activa el menú <strong>Inicio</strong> .</span><span class="sxs-lookup"><span data-stu-id="956cb-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="956cb-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span><span class="sxs-lookup"><span data-stu-id="956cb-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="956cb-159">Se desplaza verticalmente.</span><span class="sxs-lookup"><span data-stu-id="956cb-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="956cb-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="956cb-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="956cb-161">La palabra de orden inferior especifica la posición horizontal del cursor, en coordenadas de la pantalla, si se elige un comando de menú de ventana con el mouse.</span><span class="sxs-lookup"><span data-stu-id="956cb-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="956cb-162">De lo contrario, este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="956cb-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="956cb-163">La palabra de orden superior especifica la posición vertical del cursor, en coordenadas de pantalla, si se elige un comando de menú de ventana con el mouse.</span><span class="sxs-lookup"><span data-stu-id="956cb-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="956cb-164">Este parámetro es 1 si se elige el comando con un acelerador del sistema, o bien, cero si se usa una tecla de método abreviado.</span><span class="sxs-lookup"><span data-stu-id="956cb-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956cb-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="956cb-165">Return value</span></span>

<span data-ttu-id="956cb-166">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="956cb-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="956cb-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="956cb-167">Remarks</span></span>

<span data-ttu-id="956cb-168">Para obtener las coordenadas de posición en coordenadas de pantalla, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="956cb-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="956cb-169">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) lleva a cabo la solicitud de menú ventana para las acciones predefinidas especificadas en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="956cb-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="956cb-170">En los mensajes de **\_ SYSCOMMAND de WM** , el sistema usa internamente los cuatro bits de orden inferior del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="956cb-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="956cb-171">Para obtener el resultado correcto al probar el valor de *wParam*, una aplicación debe combinar el valor 0xFFF0 con el valor *wParam* mediante el operador and bit a bit.</span><span class="sxs-lookup"><span data-stu-id="956cb-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="956cb-172">Los elementos de menú de un menú ventana se pueden modificar mediante las funciones [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)y [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="956cb-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="956cb-173">Las aplicaciones que modifican el menú ventana deben procesar los mensajes de **WM \_ SYSCOMMAND** .</span><span class="sxs-lookup"><span data-stu-id="956cb-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="956cb-174">Una aplicación puede llevar a cabo cualquier comando del sistema en cualquier momento si se pasa un mensaje de **WM \_ SYSCOMMAND** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="956cb-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="956cb-175">Cualquier mensaje de **\_ SYSCOMMAND de WM** no controlado por la aplicación debe pasarse a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="956cb-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="956cb-176">Los valores de comando agregados por una aplicación deben ser procesados por la aplicación y no se pueden pasar a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="956cb-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="956cb-177">Si la Directiva habilita la protección con contraseña, se inicia el protector de pantalla independientemente de lo que hace una aplicación con la notificación **SC \_ SCREENSAVE** aunque no se pase a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="956cb-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="956cb-178">Las teclas de aceleración definidas para elegir elementos en el menú ventana se traducen en mensajes de **WM \_ SYSCOMMAND** ; todas las demás pulsaciones de teclas de aceleración se traducen en mensajes de [**\_ comandos de WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="956cb-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="956cb-179">Si el *wParam* es **SC \_ KEYMENU**, *lParam* contiene el código de carácter de la tecla que se usa con la tecla Alt para mostrar el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="956cb-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="956cb-180">Por ejemplo, si presiona ALT + F para mostrar el archivo emergente, se producirá un **\_ SYSCOMMAND de WM** con *wParam* igual a **SC \_ KEYMENU** y *lParam* igual a "F".</span><span class="sxs-lookup"><span data-stu-id="956cb-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="956cb-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="956cb-181">Requirements</span></span>



| <span data-ttu-id="956cb-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="956cb-182">Requirement</span></span> | <span data-ttu-id="956cb-183">Value</span><span class="sxs-lookup"><span data-stu-id="956cb-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="956cb-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="956cb-184">Minimum supported client</span></span><br/> | <span data-ttu-id="956cb-185">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="956cb-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="956cb-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="956cb-186">Minimum supported server</span></span><br/> | <span data-ttu-id="956cb-187">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="956cb-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="956cb-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="956cb-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="956cb-189"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="956cb-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956cb-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="956cb-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="956cb-191">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="956cb-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="956cb-192">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="956cb-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="956cb-193">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="956cb-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="956cb-194">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="956cb-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="956cb-195">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="956cb-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="956cb-196">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="956cb-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="956cb-197">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="956cb-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="956cb-198">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="956cb-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="956cb-199">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="956cb-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="956cb-200">**Vista**</span><span class="sxs-lookup"><span data-stu-id="956cb-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="956cb-201">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="956cb-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

