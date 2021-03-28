---
description: Hay muchas situaciones en las que la ejecución automática puede tener que estar deshabilitada de forma temporal o permanente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Habilitar y deshabilitar la ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423723"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="20ac9-103">Habilitar y deshabilitar la ejecución automática</span><span class="sxs-lookup"><span data-stu-id="20ac9-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="20ac9-104">Hay muchas situaciones en las que la ejecución automática puede tener que estar deshabilitada de forma temporal o permanente.</span><span class="sxs-lookup"><span data-stu-id="20ac9-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="20ac9-105">Por ejemplo, la ejecución automática podría interferir con el funcionamiento de una aplicación en ejecución y debe deshabilitarse mientras dure.</span><span class="sxs-lookup"><span data-stu-id="20ac9-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="20ac9-106">El sistema proporciona varias formas de deshabilitar la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="20ac9-107">Suprimir la ejecución automática mediante programación</span><span class="sxs-lookup"><span data-stu-id="20ac9-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="20ac9-108">Usar el registro para deshabilitar la ejecución automática</span><span class="sxs-lookup"><span data-stu-id="20ac9-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="20ac9-109">Ejecución automática para otros tipos de medios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="20ac9-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="20ac9-110">Suprimir la ejecución automática mediante programación</span><span class="sxs-lookup"><span data-stu-id="20ac9-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="20ac9-111">Hay varias situaciones en las que es posible que sea necesario suprimir la ejecución automática mediante programación.</span><span class="sxs-lookup"><span data-stu-id="20ac9-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="20ac9-112">Dos ejemplos son:</span><span class="sxs-lookup"><span data-stu-id="20ac9-112">Two examples are:</span></span>

-   <span data-ttu-id="20ac9-113">La aplicación tiene un programa de instalación que requiere que el usuario inserte otro disco que puede contener un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="20ac9-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="20ac9-114">Durante el funcionamiento de la aplicación, es posible que el usuario tenga que insertar otro disco que pueda contener un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="20ac9-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="20ac9-115">En cualquier caso, normalmente no querrá iniciar otra aplicación mientras el original está en curso.</span><span class="sxs-lookup"><span data-stu-id="20ac9-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="20ac9-116">Los usuarios pueden suprimir manualmente la ejecución automática manteniendo presionada la tecla Mayús al insertar el CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="20ac9-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="20ac9-117">Sin embargo, suele ser preferible controlar esta operación mediante programación en lugar de depender del usuario.</span><span class="sxs-lookup"><span data-stu-id="20ac9-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="20ac9-118">Con los sistemas que tienen la versión de Shell [4,70](versions.md) y versiones posteriores, Windows envía un mensaje "QueryCancelAutoPlay" a la ventana de primer plano.</span><span class="sxs-lookup"><span data-stu-id="20ac9-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="20ac9-119">La aplicación puede responder a este mensaje para suprimir la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="20ac9-120">Las utilidades del sistema utilizan este enfoque, como el cuadro de diálogo [abrir](../dlgbox/open-and-save-as-dialog-boxes.md) común para deshabilitar la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="20ac9-121">Los fragmentos de código siguientes muestran cómo configurar y controlar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="20ac9-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="20ac9-122">La aplicación debe ejecutarse en la ventana de primer plano.</span><span class="sxs-lookup"><span data-stu-id="20ac9-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="20ac9-123">En primer lugar, registre "QueryCancelAutoPlay" como mensaje de Windows:</span><span class="sxs-lookup"><span data-stu-id="20ac9-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="20ac9-124">La ventana de la aplicación debe estar en primer plano para recibir este mensaje.</span><span class="sxs-lookup"><span data-stu-id="20ac9-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="20ac9-125">El controlador de mensajes debe devolver **true** para cancelar la ejecución automática y **false** para habilitarla.</span><span class="sxs-lookup"><span data-stu-id="20ac9-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="20ac9-126">En el fragmento de código siguiente se muestra cómo utilizar este mensaje para deshabilitar la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="20ac9-127">Si la aplicación usa un cuadro de diálogo y necesita responder a un mensaje "QueryCancelAutoPlay", no puede devolver simplemente **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="20ac9-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="20ac9-128">En su lugar, llame a [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) con *NIndex* establecido en **DWL \_ MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="20ac9-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="20ac9-129">Establezca el parámetro *dwNewLong* en **true** para cancelar la ejecución automática y **false** para habilitarla.</span><span class="sxs-lookup"><span data-stu-id="20ac9-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="20ac9-130">Por ejemplo, el procedimiento de cuadro de diálogo de ejemplo siguiente cancela la ejecución automática cuando recibe un mensaje "QueryCancelAutoPlay".</span><span class="sxs-lookup"><span data-stu-id="20ac9-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="20ac9-131">Usar el registro para deshabilitar la ejecución automática</span><span class="sxs-lookup"><span data-stu-id="20ac9-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="20ac9-132">Hay dos valores de registro que se pueden usar para deshabilitar de forma persistente la ejecución automática: NoDriveAutoRun y NoDriveTypeAutoRun.</span><span class="sxs-lookup"><span data-stu-id="20ac9-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="20ac9-133">El primer valor deshabilita la ejecución automática de las letras de unidad especificadas y la segunda deshabilita la ejecución automática para una clase de unidades.</span><span class="sxs-lookup"><span data-stu-id="20ac9-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="20ac9-134">Si alguno de estos valores se establece para deshabilitar la ejecución automática de un dispositivo determinado, se deshabilitará.</span><span class="sxs-lookup"><span data-stu-id="20ac9-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="20ac9-135">Vea el artículo de Knowledge base [cómo deshabilitar la funcionalidad de ejecución automática en Windows](https://support.microsoft.com/kb/967715) para obtener más información sobre cómo deshabilitar la funcionalidad de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="20ac9-136">En este artículo se enumeran las diferentes actualizaciones que debe tener instaladas para deshabilitar correctamente la funcionalidad de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="20ac9-137">Los valores de NoDriveAutoRun y NoDriveTypeAutoRun solo deben ser modificados por los administradores del sistema para cambiar el valor de todo el sistema con fines de prueba o administrativos.</span><span class="sxs-lookup"><span data-stu-id="20ac9-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="20ac9-138">Las aplicaciones no deben modificar estos valores, ya que no hay ninguna manera de restaurarlos de forma confiable a sus valores originales.</span><span class="sxs-lookup"><span data-stu-id="20ac9-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="20ac9-139">El valor NoDriveAutoRun deshabilita la ejecución automática de las letras de unidad especificadas.</span><span class="sxs-lookup"><span data-stu-id="20ac9-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="20ac9-140">Es un valor de \_ datos de REG DWORD, que se encuentra en la clave siguiente:</span><span class="sxs-lookup"><span data-stu-id="20ac9-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="20ac9-141">El primer bit del valor corresponde a la unidad a:, la segunda a B:, etc.</span><span class="sxs-lookup"><span data-stu-id="20ac9-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="20ac9-142">Para deshabilitar la ejecución automática de una o varias letras de unidad, establezca los bits correspondientes.</span><span class="sxs-lookup"><span data-stu-id="20ac9-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="20ac9-143">Por ejemplo, para deshabilitar las unidades A: y C:, establezca NoDriveAutoRun en `0x00000005` .</span><span class="sxs-lookup"><span data-stu-id="20ac9-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="20ac9-144">El valor NoDriveTypeAutoRun deshabilita AutoRun para una clase de unidades.</span><span class="sxs-lookup"><span data-stu-id="20ac9-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="20ac9-145">Es un valor de \_ datos binario de REG DWORD o de 4 bytes \_ , que se encuentra en la misma clave.</span><span class="sxs-lookup"><span data-stu-id="20ac9-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="20ac9-146">Al establecer los bits del primer byte de este valor, se pueden excluir las diferentes unidades de trabajo con la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="20ac9-147">En la tabla siguiente se proporcionan las constantes de bits y máscara de bits que se pueden establecer en el primer byte de NoDriveTypeAutoRun para deshabilitar la ejecución automática de un tipo de unidad determinado.</span><span class="sxs-lookup"><span data-stu-id="20ac9-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="20ac9-148">Debe reiniciar el explorador de Windows para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="20ac9-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="20ac9-149">Número de bits</span><span class="sxs-lookup"><span data-stu-id="20ac9-149">Bit Number</span></span> | <span data-ttu-id="20ac9-150">Constante de máscara de máscara</span><span class="sxs-lookup"><span data-stu-id="20ac9-150">Bitmask Constant</span></span>      | <span data-ttu-id="20ac9-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="20ac9-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="20ac9-152">0x04</span><span class="sxs-lookup"><span data-stu-id="20ac9-152">0x04</span></span>       | <span data-ttu-id="20ac9-153">**UNIDAD que se \_ va a cambiar**</span><span class="sxs-lookup"><span data-stu-id="20ac9-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="20ac9-154">El disco se puede quitar de la unidad (por ejemplo, un disquete).</span><span class="sxs-lookup"><span data-stu-id="20ac9-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="20ac9-155">0x08</span><span class="sxs-lookup"><span data-stu-id="20ac9-155">0x08</span></span>       | <span data-ttu-id="20ac9-156">**UNIDAD \_ fija**</span><span class="sxs-lookup"><span data-stu-id="20ac9-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="20ac9-157">No se puede quitar el disco de la unidad (un disco duro).</span><span class="sxs-lookup"><span data-stu-id="20ac9-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="20ac9-158">0x10</span><span class="sxs-lookup"><span data-stu-id="20ac9-158">0x10</span></span>       | <span data-ttu-id="20ac9-159">**UNIDAD \_ remota**</span><span class="sxs-lookup"><span data-stu-id="20ac9-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="20ac9-160">Unidad de red.</span><span class="sxs-lookup"><span data-stu-id="20ac9-160">Network drive.</span></span>                                          |
| <span data-ttu-id="20ac9-161">0x20</span><span class="sxs-lookup"><span data-stu-id="20ac9-161">0x20</span></span>       | <span data-ttu-id="20ac9-162">**UNIDAD \_ CDROM**</span><span class="sxs-lookup"><span data-stu-id="20ac9-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="20ac9-163">Unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="20ac9-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="20ac9-164">0x40</span><span class="sxs-lookup"><span data-stu-id="20ac9-164">0x40</span></span>       | <span data-ttu-id="20ac9-165">**DISCO \_ ramdisk**</span><span class="sxs-lookup"><span data-stu-id="20ac9-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="20ac9-166">Disco RAM.</span><span class="sxs-lookup"><span data-stu-id="20ac9-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="20ac9-167">Ejecución automática para otros tipos de medios de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="20ac9-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="20ac9-168">La ejecución automática está pensada principalmente para la distribución pública de aplicaciones en CD-ROM y DVD-ROM, y no se recomienda su uso en otros medios de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="20ac9-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="20ac9-169">Sin embargo, a menudo resulta útil habilitar la ejecución automática en otros tipos de medios de almacenamiento extraíbles.</span><span class="sxs-lookup"><span data-stu-id="20ac9-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="20ac9-170">Esta característica se usa normalmente para simplificar la depuración de archivos AutoRun. inf.</span><span class="sxs-lookup"><span data-stu-id="20ac9-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="20ac9-171">La ejecución automática solo funciona en dispositivos de almacenamiento extraíbles cuando se cumplen los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="20ac9-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="20ac9-172">El dispositivo debe tener controladores compatibles con AutoRun.</span><span class="sxs-lookup"><span data-stu-id="20ac9-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="20ac9-173">Para que sea compatible con la ejecución automática, un controlador debe notificar al sistema que se ha insertado un disco mediante el envío de un mensaje de [**\_ DEVICECHANGE de WM**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="20ac9-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="20ac9-174">El directorio raíz del medio insertado debe contener un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="20ac9-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="20ac9-175">El dispositivo no debe tener la ejecución automática deshabilitada a través del [registro](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="20ac9-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="20ac9-176">La aplicación en primer plano no ha [suprimido](#suppressing-autorun-programmatically) la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="20ac9-177">Esta característica no debe usarse para distribuir aplicaciones en medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="20ac9-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="20ac9-178">Dado que la implementación de la ejecución automática en medios extraíbles proporciona una manera sencilla de propagar los virus informáticos, los usuarios deben ser sospechosos de cualquier disquete distribuido públicamente que contenga un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="20ac9-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="20ac9-179">Normalmente, la ejecución automática se inicia automáticamente, pero también se puede iniciar manualmente.</span><span class="sxs-lookup"><span data-stu-id="20ac9-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="20ac9-180">Si el dispositivo cumple los criterios indicados anteriormente, el menú contextual de la letra de la unidad incluirá un comando de **reproducción automática** .</span><span class="sxs-lookup"><span data-stu-id="20ac9-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="20ac9-181">Para ejecutar la ejecución automática manualmente, haga clic con el botón derecho en el icono de la unidad y seleccione **reproducción automática** en el menú contextual o haga doble clic en el icono de la unidad.</span><span class="sxs-lookup"><span data-stu-id="20ac9-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="20ac9-182">Si los controladores no son compatibles con la ejecución automática, el menú contextual no tendrá un elemento **reproducción automática** y no se podrá iniciar la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="20ac9-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="20ac9-183">Los controladores compatibles con AutoRun se proporcionan con algunas unidades de disco extraíbles, así como otros tipos de medios extraíbles, como tarjetas CompactFlash.</span><span class="sxs-lookup"><span data-stu-id="20ac9-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="20ac9-184">La ejecución automática también funciona con las unidades de red asignadas a una letra de unidad con el explorador de Windows o montadas con [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span><span class="sxs-lookup"><span data-stu-id="20ac9-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="20ac9-185">Al igual que con el hardware montado, una unidad de red montada debe tener un archivo Autorun. inf en el directorio raíz y no debe deshabilitarse a través del [registro](#using-the-registry-to-disable-autorun).</span><span class="sxs-lookup"><span data-stu-id="20ac9-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
