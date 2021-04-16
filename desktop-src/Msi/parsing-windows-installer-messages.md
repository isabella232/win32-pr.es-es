---
description: Un controlador de interfaz de usuario externo puede procesar la lista de mensajes de instalador especificados por el parámetro dwMessagedFilter de la función MsiSetExternalUI.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Analizar mensajes de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276166"
---
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="fcd8d-103">Analizar mensajes de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fcd8d-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="fcd8d-104">Un controlador de interfaz de usuario externo puede procesar la lista de mensajes de instalador especificados por el parámetro *dwMessagedFilter* de la función [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="fcd8d-105">Algunos de estos mensajes contienen cadenas que se pueden usar directamente, y es posible que el controlador de la interfaz de usuario externa deba analizar y procesar otros mensajes para que sean útiles.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="fcd8d-106">Es posible que el controlador de la interfaz de usuario externa solo necesite supervisar Windows Installer mensajes sin realizar ninguna operación que afecte a la instalación.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="fcd8d-107">Los siguientes mensajes de Windows Installer contienen cadenas que se pueden mostrar en un cuadro de diálogo y no necesitan ningún procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="fcd8d-108">Estos mensajes contienen una lista de botones e iconos que se mostrarán en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="fcd8d-109">Puede usar los valores **MB \_ ICONMASK**, **MB \_ DEFMASK** y **MB \_ TYPEMASK** para especificar iconos y botones.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="fcd8d-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-111">Se ha producido una terminación prematura de la instalación.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**\_error INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-113">Mensaje de error con formato.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**ADVERTENCIA de INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-115">Mensaje de advertencia con formato.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**información de INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-117">Mensaje de registro con formato.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_usuario INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-119">Mensaje de usuario con formato.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-121">Mensaje con formato que indica una condición de espacio insuficiente en disco</span><span class="sxs-lookup"><span data-stu-id="fcd8d-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="fcd8d-122">El controlador de usuario externo puede usar los siguientes mensajes de Windows Installer para supervisar una secuencia de la interfaz de usuario de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="fcd8d-123">El instalador envía estos mensajes al principio de una secuencia de interfaz de usuario Windows Installer, como se muestra cada cuadro de diálogo, y al final de la secuencia de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="fcd8d-124">No se requiere ningún procesamiento para usar estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="fcd8d-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>\_Finalizar INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="fcd8d-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-126">Este mensaje indica el final de la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="fcd8d-127">La cadena es una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE \_ inicializar</span><span class="sxs-lookup"><span data-stu-id="fcd8d-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-129">Este mensaje indica que se ha iniciado la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="fcd8d-130">La cadena es una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG</span><span class="sxs-lookup"><span data-stu-id="fcd8d-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-132">La cadena contiene el nombre del cuadro de diálogo actual.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="fcd8d-133">Los siguientes mensajes de Windows Installer requieren un procesamiento adicional por parte del controlador de la interfaz de usuario externa.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="fcd8d-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ RESOLVESOURCE**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-135">El controlador de la interfaz de usuario externa debe devolver 0 y permitir que Windows Installer controle el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="fcd8d-136">El controlador de la interfaz de usuario externa puede supervisar este mensaje, pero no debe realizar ninguna acción que afecte a la instalación.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-138">La interfaz de usuario externa debería mostrar un [cuadro de diálogo FilesInUse](filesinuse-dialog.md) en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-140">La interfaz de usuario externa debería mostrar un [cuadro de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="fcd8d-141">Disponible a partir de Windows Installer versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="fcd8d-142">Para obtener más información sobre este mensaje, consulte [uso del administrador de reinicio con una interfaz de usuario externa](using-restart-manager-with-an-external-ui-.md).</span><span class="sxs-lookup"><span data-stu-id="fcd8d-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-144">Este mensaje proporciona información acerca de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-144">This message gives information about the current action.</span></span> <span data-ttu-id="fcd8d-145">El formato es la acción \[ 1 \] : \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="fcd8d-146">\[3 \] , donde se usa un signo de dos puntos para separar el campo 1 y el campo 2 y se utiliza un punto para separar el campo 2 y el campo 3.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="fcd8d-147">El campo \[ 1 \] contiene la hora a la que se inició la acción mediante el formato de la propiedad [**Time**](time.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="fcd8d-148">El campo \[ 2 \] contiene el nombre de la acción de la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="fcd8d-149">El campo \[ 3 \] proporciona la descripción de la acción de la [tabla ActionText](actiontext-table.md) o de la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-151">El formato de esta cadena se especifica mediante el valor de [plantilla](template.md) proporcionado en la [tabla ActionText](actiontext-table.md) o la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="fcd8d-152">Puede haber un número ilimitado de mensajes de **INSTALLMESSAGE \_ ACTIONDATA** después del mensaje **\_ ACTIONSTART de INSTALLMESSAGE** .</span><span class="sxs-lookup"><span data-stu-id="fcd8d-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**</span><span class="sxs-lookup"><span data-stu-id="fcd8d-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-154">Este mensaje tiene tres subtipos: Language, Caption y CancelShow.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="fcd8d-155">La cadena puede tener tres campos delimitados por un número seguido de un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="fcd8d-156">No todos los campos son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-156">Not all fields are required.</span></span> <span data-ttu-id="fcd8d-157">El mensaje puede ser una cadena nula o vacía ("").</span><span class="sxs-lookup"><span data-stu-id="fcd8d-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="fcd8d-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo</span><span class="sxs-lookup"><span data-stu-id="fcd8d-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-159">El campo 1 contiene el valor 0 para indicar que esta cadena contiene información de idioma.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="fcd8d-160">El campo 2 contiene un valor de [idioma](language.md) que es un identificador de idioma numérico (LANGID). El campo 3 es un valor que representa una página de códigos ANSI.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Hayan</span><span class="sxs-lookup"><span data-stu-id="fcd8d-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-162">El campo 1 contiene el valor 1 para indicar que esta cadena contiene el texto de una leyenda o título.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="fcd8d-163">El campo 2 contiene texto que puede usar un controlador de interfaz de usuario externo como título de título de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="fcd8d-164">El campo 3 es NULL o una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="fcd8d-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="fcd8d-165">El campo 3 puede no estar presente en el mensaje de leyenda.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span><span class="sxs-lookup"><span data-stu-id="fcd8d-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-167">El campo 1 contiene el valor 2 para indicar que esta cadena contiene información sobre si se debe mostrar el botón Cancelar.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="fcd8d-168">Si se debe ocultar el botón Cancelar, el campo 2 contiene el valor 0.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="fcd8d-169">Si el botón Cancelar debe estar visible, el campo 2 contiene el valor 1.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fcd8d-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>progreso de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="fcd8d-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-171">Este mensaje tiene cuatro subtipos: RESET, ActionInfo, ProgressReport y ProgressAddition.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="fcd8d-172">El controlador externo no debe actuar sobre ninguno de estos mensajes hasta que se reciba el primer mensaje de progreso de restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="fcd8d-173">Esto proporciona una estimación del número total de pasos de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="fcd8d-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Determinado</span><span class="sxs-lookup"><span data-stu-id="fcd8d-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-175">El campo 1 contiene el valor 0 para indicar un restablecimiento de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="fcd8d-176">El campo 2 contiene el número total de TICs en la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="fcd8d-177">El campo 3 contiene el valor 0 para el movimiento de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="fcd8d-178">El campo 3 contiene el valor 1 para el movimiento de la barra de progreso hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="fcd8d-179">El valor 0 en el campo 4 significa que la instalación está en curso y se puede calcular el tiempo restante.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="fcd8d-180">El valor 1 en el campo 4 significa que se está ejecutando el script y que "espere..." se puede mostrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="fcd8d-181">La estimación del número total de TICs es una aproximación y puede ser incorrecta.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span><span class="sxs-lookup"><span data-stu-id="fcd8d-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-183">El campo 1 contiene el valor 1 para indicar que esta cadena contiene información de la acción.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="fcd8d-184">El campo 2 contiene el número de pasos que la barra de progreso mueve para cada mensaje ActionData enviado por la acción actual.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="fcd8d-185">Si el campo 3 contiene el valor 0, omita el campo 2.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="fcd8d-186">Si el campo 3 contiene el valor 1, incremente la barra de progreso en el número de pasos en el campo 2 para cada mensaje ActionData enviado por la acción actual.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="fcd8d-187">El campo 4 no se usa.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span><span class="sxs-lookup"><span data-stu-id="fcd8d-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-189">El campo 1 contiene el valor 2 para indicar que esta cadena contiene información de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="fcd8d-190">El campo 2 contiene el número de pasos que ha cambiado la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="fcd8d-191">El campo 3 no se usa.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-191">Field 3 is unused.</span></span> <span data-ttu-id="fcd8d-192">El campo 4 no se usa.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="fcd8d-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="fcd8d-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="fcd8d-194">El campo 1 contiene el valor 3 para indicar que una acción puede Agregar TICs en la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="fcd8d-195">El campo 2 contiene el número de pasos que se van a agregar al recuento total esperado de TICs de progreso.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="fcd8d-196">El campo 3 no se usa.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-196">Field 3 is unused.</span></span> <span data-ttu-id="fcd8d-197">El campo 4 no se usa.</span><span class="sxs-lookup"><span data-stu-id="fcd8d-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



