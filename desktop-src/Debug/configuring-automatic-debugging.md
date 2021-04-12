---
description: Los usuarios pueden configurar la depuración automática para ayudarles a determinar por qué el sistema o una aplicación han dejado de responder.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configuración de la depuración automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152745"
---
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="53ee5-103">Configuración de la depuración automática</span><span class="sxs-lookup"><span data-stu-id="53ee5-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="53ee5-104">Los usuarios pueden configurar la depuración automática para ayudarles a determinar por qué el sistema o una aplicación han dejado de responder.</span><span class="sxs-lookup"><span data-stu-id="53ee5-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="53ee5-105">Configurar la depuración automática para los bloqueos del sistema</span><span class="sxs-lookup"><span data-stu-id="53ee5-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="53ee5-106">Para configurar el equipo de destino para que genere un archivo de volcado cuando el sistema deje de responder, use la aplicación **sistema** en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="53ee5-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="53ee5-107">Haga clic en **Configuración avanzada del sistema**, que muestra el cuadro de diálogo **propiedades del sistema** .</span><span class="sxs-lookup"><span data-stu-id="53ee5-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="53ee5-108">En la pestaña **Opciones avanzadas** de ese cuadro, haga clic en **configuración** en **Inicio y recuperación** y, a continuación, use las opciones de recuperación adecuadas.</span><span class="sxs-lookup"><span data-stu-id="53ee5-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="53ee5-109">Como alternativa, puede configurar las opciones de volcado de memoria con la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="53ee5-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="53ee5-110">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local CrashControl</span><span class="sxs-lookup"><span data-stu-id="53ee5-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="53ee5-111">El archivo que se puede especificar es el archivo de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="53ee5-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="53ee5-112">Su nombre predeterminado es Memory. DMP.</span><span class="sxs-lookup"><span data-stu-id="53ee5-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="53ee5-113">Puede depurar un volcado de memoria con un depurador en modo kernel, como WinDbg o KD.</span><span class="sxs-lookup"><span data-stu-id="53ee5-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="53ee5-114">Para obtener más información, vea la documentación que se incluye con el depurador.</span><span class="sxs-lookup"><span data-stu-id="53ee5-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="53ee5-115">Configuración de la depuración automática para bloqueos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="53ee5-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="53ee5-116">Cuando una aplicación deja de responder (por ejemplo, después de una infracción de acceso), el sistema invoca automáticamente un depurador que se especifica en el registro para la depuración de postmortem, el identificador de proceso y el identificador de evento se pasan al depurador si la línea de comandos está configurada correctamente.</span><span class="sxs-lookup"><span data-stu-id="53ee5-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="53ee5-117">En el procedimiento siguiente se describe cómo especificar un depurador en el registro.</span><span class="sxs-lookup"><span data-stu-id="53ee5-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="53ee5-118">**Para establecer un depurador como el depurador de postmortem**</span><span class="sxs-lookup"><span data-stu-id="53ee5-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="53ee5-119">Vaya a la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="53ee5-119">Go to the following registry key:</span></span>

    <span data-ttu-id="53ee5-120">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**</span><span class="sxs-lookup"><span data-stu-id="53ee5-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="53ee5-121">Agregue o edite el valor del **depurador** mediante una cadena de reg \_ SZ que especifica la línea de comandos para el depurador.</span><span class="sxs-lookup"><span data-stu-id="53ee5-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="53ee5-122">La cadena debe incluir la ruta de acceso completa al archivo ejecutable del depurador.</span><span class="sxs-lookup"><span data-stu-id="53ee5-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="53ee5-123">Indique el identificador de proceso y el identificador de evento con los parámetros "% LD" en la línea de comandos del depurador.</span><span class="sxs-lookup"><span data-stu-id="53ee5-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="53ee5-124">Los depuradores diferentes pueden tener sus propias sintaxis de parámetros para indicar estos valores.</span><span class="sxs-lookup"><span data-stu-id="53ee5-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="53ee5-125">Cuando se invoca el depurador, el primer "% LD" se reemplaza por el identificador del proceso y el segundo "% LD" se reemplaza por el identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="53ee5-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="53ee5-126">El siguiente texto es un ejemplo de cómo configurar WinDbg como el depurador.</span><span class="sxs-lookup"><span data-stu-id="53ee5-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="53ee5-127">Si desea que el depurador se invoque sin interacción del usuario, agregue o edite el valor **auto** mediante una \_ cadena de reg SZ que especifica si el sistema debe mostrar un cuadro de diálogo al usuario antes de que se invoque el depurador.</span><span class="sxs-lookup"><span data-stu-id="53ee5-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="53ee5-128">La cadena "1" deshabilita el cuadro de diálogo; la cadena "0" habilita el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="53ee5-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="53ee5-129">Excluir una aplicación de la depuración automática</span><span class="sxs-lookup"><span data-stu-id="53ee5-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="53ee5-130">En el procedimiento siguiente se describe cómo excluir una aplicación de la depuración automática después de que el valor **auto** en la clave **AEDebug** se haya establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="53ee5-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="53ee5-131">**Para excluir una aplicación de la depuración automática**</span><span class="sxs-lookup"><span data-stu-id="53ee5-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="53ee5-132">Vaya a la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="53ee5-132">Go to the following registry key:</span></span>

    <span data-ttu-id="53ee5-133">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AEDebug**</span><span class="sxs-lookup"><span data-stu-id="53ee5-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="53ee5-134">Agregue un \_ valor de REG DWORD a la subclave **AutoExclusionList** , donde name es el nombre del archivo ejecutable y el valor es 1.</span><span class="sxs-lookup"><span data-stu-id="53ee5-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="53ee5-135">De forma predeterminada, el Administrador de ventanas de escritorio (Dwm.exe) se excluye de la depuración automática porque, de lo contrario, se puede producir un interbloqueo del sistema si Dwm.exe deja de responder (el usuario no puede ver la interfaz que muestra el depurador porque Dwm.exe no responde y Dwm.exe no puede finalizar porque está retenida por el depurador).</span><span class="sxs-lookup"><span data-stu-id="53ee5-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="53ee5-136">**Windows Server 2003 y Windows XP:** La subclave **AutoExclusionList** no está disponible; por lo tanto, no puede excluir ninguna aplicación, incluido Dwm.exe, de la depuración automática.</span><span class="sxs-lookup"><span data-stu-id="53ee5-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="53ee5-137">Las entradas del registro de **AEDebug** predeterminadas se pueden representar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="53ee5-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a><span data-ttu-id="53ee5-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53ee5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ee5-139">Habilitar la depuración de postmortem con WinDbg</span><span class="sxs-lookup"><span data-stu-id="53ee5-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
