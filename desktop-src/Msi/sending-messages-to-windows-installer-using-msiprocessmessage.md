---
description: Los mensajes enviados mediante MsiProcessMessage son los mismos que los recibidos por la función de \_ devolución de llamada del controlador INSTALLUI si se llamó a MsiSetExternalUI.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Envío de mensajes a Windows Installer mediante MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003039"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="04591-103">Envío de mensajes a Windows Installer mediante MsiProcessMessage</span><span class="sxs-lookup"><span data-stu-id="04591-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="04591-104">Los mensajes enviados mediante [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) son los mismos que los recibidos por la función de devolución de llamada del [**\_ controlador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) si se llamó a [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="04591-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="04591-105">De lo contrario, Windows Installer controla los mensajes.</span><span class="sxs-lookup"><span data-stu-id="04591-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="04591-106">Para obtener más información, consulte [análisis de mensajes de Windows Installer](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="04591-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="04591-107">Por ejemplo, para enviar un \_ mensaje de error INSTALLMESSAGE con el \_ icono MB ICONWARNING y los \_ botones ABORTRETRYCANCEL MB:</span><span class="sxs-lookup"><span data-stu-id="04591-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="04591-108">Donde *hInstall* es el identificador de la instalación, proporcionado a una acción personalizada o al identificador *hProduct* de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), y *hRec* es el registro que contiene la información de error que se va a formatear.</span><span class="sxs-lookup"><span data-stu-id="04591-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="04591-109">Para obtener información sobre cómo se realiza el formato, vea [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span><span class="sxs-lookup"><span data-stu-id="04591-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="04591-110">De forma predeterminada, si \_ se envía un mensaje de error INSTALLMESSAGE o INSTALLMESSAGE \_ FATALEXIT sin especificar tipos de botón o de icono, \_ se usan MB OK, no Icon y MB \_ DEFBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="04591-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="04591-111">Windows Installer no etiqueta el botón **anular** con la cadena "Abort" al mostrar un cuadro de mensajes con la \_ especificación del botón MB ABORTRETRYIGNORE, en su lugar, etiqueta el botón con la cadena "Cancel".</span><span class="sxs-lookup"><span data-stu-id="04591-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="04591-112">Todos los mensajes de error abstenerse de usar la palabra "Abort" y, en su lugar, usan la palabra "Cancel".</span><span class="sxs-lookup"><span data-stu-id="04591-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="04591-113">El parámetro *hRecord* de la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende del tipo de mensaje enviado al [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="04591-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="04591-114">En la siguiente lista se detallan los requisitos del registro en relación con el tipo de mensaje:</span><span class="sxs-lookup"><span data-stu-id="04591-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="04591-115">INSTALLMESSAGE \_ FATALEXIT</span><span class="sxs-lookup"><span data-stu-id="04591-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="04591-116">información de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="04591-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="04591-117">INSTALLMESSAGE \_ OUTOFDISKSPACE</span><span class="sxs-lookup"><span data-stu-id="04591-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="04591-118">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-118">Field</span></span>         | <span data-ttu-id="04591-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04591-120">0</span><span class="sxs-lookup"><span data-stu-id="04591-120">0</span></span>             | <span data-ttu-id="04591-121">Plantilla para el formato de la cadena resultante.</span><span class="sxs-lookup"><span data-stu-id="04591-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="04591-122">Vea [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="04591-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="04591-123">Se hace referencia a los campos del registro usando \[ 1 \] en el campo 1, \[ 2 \] para el campo 2, etc.</span><span class="sxs-lookup"><span data-stu-id="04591-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="04591-124">de 1 a *n*</span><span class="sxs-lookup"><span data-stu-id="04591-124">1 through *n*</span></span> | <span data-ttu-id="04591-125">Todos los campos siguientes están directamente relacionados con los campos a los que hace referencia la plantilla en el campo 0.</span><span class="sxs-lookup"><span data-stu-id="04591-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="04591-126">Si el campo 0 es null, la cadena recibida por el controlador de la interfaz de usuario tiene el formato: 1: \[ datos del campo 1 \] 2: los \[ datos del campo 2 \] significa que para cada campo del registro, la cadena contiene el número de campo seguido de los datos almacenados en el campo.</span><span class="sxs-lookup"><span data-stu-id="04591-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="04591-127">Los mensajes de información de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) se registran cuando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), la [opción de línea de comandos](command-line-options.md)'/l ' o la [Directiva de registro](logging.md) especifican ' I ' o INSTALLLOGMODE \_ info.</span><span class="sxs-lookup"><span data-stu-id="04591-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="04591-128">\_error INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="04591-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="04591-129">ADVERTENCIA de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="04591-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="04591-130">\_usuario INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="04591-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="04591-131">Para utilizar un mensaje de la tabla de errores.</span><span class="sxs-lookup"><span data-stu-id="04591-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="04591-132">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-132">Field</span></span>         | <span data-ttu-id="04591-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="04591-134">0</span><span class="sxs-lookup"><span data-stu-id="04591-134">0</span></span>             | <span data-ttu-id="04591-135">Debe ser null.</span><span class="sxs-lookup"><span data-stu-id="04591-135">Must be null.</span></span>                                         |
| <span data-ttu-id="04591-136">1</span><span class="sxs-lookup"><span data-stu-id="04591-136">1</span></span>             | <span data-ttu-id="04591-137">Número de mensaje en la [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="04591-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="04591-138">de 2 a *n*</span><span class="sxs-lookup"><span data-stu-id="04591-138">2 through *n*</span></span> | <span data-ttu-id="04591-139">Relacionado con el mensaje especificado en la tabla de errores.</span><span class="sxs-lookup"><span data-stu-id="04591-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="04591-140">Por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="04591-140">For example.</span></span>



| <span data-ttu-id="04591-141">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-141">Field</span></span> | <span data-ttu-id="04591-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="04591-142">Type</span></span>   | <span data-ttu-id="04591-143">Datos</span><span class="sxs-lookup"><span data-stu-id="04591-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="04591-144">0</span><span class="sxs-lookup"><span data-stu-id="04591-144">0</span></span>     | <span data-ttu-id="04591-145">string</span><span class="sxs-lookup"><span data-stu-id="04591-145">string</span></span> | <span data-ttu-id="04591-146">null</span><span class="sxs-lookup"><span data-stu-id="04591-146">null</span></span>       |
| <span data-ttu-id="04591-147">1</span><span class="sxs-lookup"><span data-stu-id="04591-147">1</span></span>     | <span data-ttu-id="04591-148">int</span><span class="sxs-lookup"><span data-stu-id="04591-148">int</span></span>    | <span data-ttu-id="04591-149">1304</span><span class="sxs-lookup"><span data-stu-id="04591-149">1304</span></span>       |
| <span data-ttu-id="04591-150">2</span><span class="sxs-lookup"><span data-stu-id="04591-150">2</span></span>     | <span data-ttu-id="04591-151">string</span><span class="sxs-lookup"><span data-stu-id="04591-151">string</span></span> | <span data-ttu-id="04591-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="04591-152">Myfile.txt</span></span> |



 

<span data-ttu-id="04591-153">El mensaje resultante recibido del controlador de la interfaz de usuario es:</span><span class="sxs-lookup"><span data-stu-id="04591-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="04591-154">Error 1304.</span><span class="sxs-lookup"><span data-stu-id="04591-154">Error 1304.</span></span> <span data-ttu-id="04591-155">Error al escribir en el archivo: Myfile.txt.</span><span class="sxs-lookup"><span data-stu-id="04591-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="04591-156">Compruebe que tiene acceso a ese directorio.</span><span class="sxs-lookup"><span data-stu-id="04591-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="04591-157">Si el campo 0 no es null, se invalida el mensaje de la tabla de errores.</span><span class="sxs-lookup"><span data-stu-id="04591-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="04591-158">En su lugar, la plantilla de campo 0 determina el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="04591-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="04591-159">El mensaje también puede especificar los botones, incluido el botón predeterminado, y el icono para usarlo con el mensaje, como se mencionó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="04591-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="04591-160">Los tipos de icono y botón se enumeran en el [**\_ controlador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span><span class="sxs-lookup"><span data-stu-id="04591-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="04591-161">INSTALLMESSAGE \_ COMMONDATA</span><span class="sxs-lookup"><span data-stu-id="04591-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="04591-162">Este mensaje se envía para habilitar o deshabilitar el botón **Cancelar** en un cuadro de diálogo de progreso.</span><span class="sxs-lookup"><span data-stu-id="04591-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="04591-163">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-163">Field</span></span> | <span data-ttu-id="04591-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04591-165">0</span><span class="sxs-lookup"><span data-stu-id="04591-165">0</span></span>     | <span data-ttu-id="04591-166">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="04591-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="04591-167">1</span><span class="sxs-lookup"><span data-stu-id="04591-167">1</span></span>     | <span data-ttu-id="04591-168">2 hace referencia al botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="04591-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="04591-169">2</span><span class="sxs-lookup"><span data-stu-id="04591-169">2</span></span>     | <span data-ttu-id="04591-170">Un valor de 1 indica que el botón **Cancelar** debe estar visible.</span><span class="sxs-lookup"><span data-stu-id="04591-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="04591-171">Un valor de 0 indica que el botón **Cancelar** debe ser invisible.</span><span class="sxs-lookup"><span data-stu-id="04591-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="04591-172">Por ejemplo, para deshabilitar u ocultar el botón **Cancelar** , el registro tendría el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="04591-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="04591-173">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-173">Field</span></span> | <span data-ttu-id="04591-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="04591-174">Type</span></span>   | <span data-ttu-id="04591-175">Datos</span><span class="sxs-lookup"><span data-stu-id="04591-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="04591-176">0</span><span class="sxs-lookup"><span data-stu-id="04591-176">0</span></span>     | <span data-ttu-id="04591-177">string</span><span class="sxs-lookup"><span data-stu-id="04591-177">string</span></span> | <span data-ttu-id="04591-178">null</span><span class="sxs-lookup"><span data-stu-id="04591-178">null</span></span> |
| <span data-ttu-id="04591-179">1</span><span class="sxs-lookup"><span data-stu-id="04591-179">1</span></span>     | <span data-ttu-id="04591-180">int</span><span class="sxs-lookup"><span data-stu-id="04591-180">int</span></span>    | <span data-ttu-id="04591-181">2</span><span class="sxs-lookup"><span data-stu-id="04591-181">2</span></span>    |
| <span data-ttu-id="04591-182">2</span><span class="sxs-lookup"><span data-stu-id="04591-182">2</span></span>     | <span data-ttu-id="04591-183">int</span><span class="sxs-lookup"><span data-stu-id="04591-183">int</span></span>    | <span data-ttu-id="04591-184">0</span><span class="sxs-lookup"><span data-stu-id="04591-184">0</span></span>    |



 

<span data-ttu-id="04591-185">INSTALLMESSAGE \_ ACTIONSTART</span><span class="sxs-lookup"><span data-stu-id="04591-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="04591-186">INSTALLMESSAGE \_ ACTIONDATA</span><span class="sxs-lookup"><span data-stu-id="04591-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="04591-187">El \_ registro ACTIONSTART de INSTALLMESSAGE determina el formato del registro ActionData.</span><span class="sxs-lookup"><span data-stu-id="04591-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="04591-188">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-188">Field</span></span> | <span data-ttu-id="04591-189">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04591-190">0</span><span class="sxs-lookup"><span data-stu-id="04591-190">0</span></span>     | <span data-ttu-id="04591-191">null</span><span class="sxs-lookup"><span data-stu-id="04591-191">null</span></span>                                                                                                          |
| <span data-ttu-id="04591-192">1</span><span class="sxs-lookup"><span data-stu-id="04591-192">1</span></span>     | <span data-ttu-id="04591-193">Nombre de la acción.</span><span class="sxs-lookup"><span data-stu-id="04591-193">Action name.</span></span> <span data-ttu-id="04591-194">El nombre de este campo no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="04591-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="04591-195">2</span><span class="sxs-lookup"><span data-stu-id="04591-195">2</span></span>     | <span data-ttu-id="04591-196">Descripción de la acción.</span><span class="sxs-lookup"><span data-stu-id="04591-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="04591-197">3</span><span class="sxs-lookup"><span data-stu-id="04591-197">3</span></span>     | <span data-ttu-id="04591-198">Plantilla de acción.</span><span class="sxs-lookup"><span data-stu-id="04591-198">Action template.</span></span> <span data-ttu-id="04591-199">Se usa para el ActionData cuyo mensaje se está formateando según esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="04591-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="04591-200">No haga referencia al campo 0 en el mensaje de la plantilla de acción.</span><span class="sxs-lookup"><span data-stu-id="04591-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="04591-201">El registro de INSTALLMESSAGE \_ ACTIONDATA tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="04591-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="04591-202">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-202">Field</span></span>         | <span data-ttu-id="04591-203">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04591-204">0</span><span class="sxs-lookup"><span data-stu-id="04591-204">0</span></span>             | <span data-ttu-id="04591-205">null</span><span class="sxs-lookup"><span data-stu-id="04591-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="04591-206">de 1 a *n*</span><span class="sxs-lookup"><span data-stu-id="04591-206">1 through *n*</span></span> | <span data-ttu-id="04591-207">Depende del campo 3 del \_ mensaje ACTIONSTART INSTALLMESSAGE correspondiente o de la plantilla especificada en la [tabla ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="04591-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="04591-208">Por ejemplo, el \_ registro INSTALLMESSAGE ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="04591-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="04591-209">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-209">Field</span></span> | <span data-ttu-id="04591-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="04591-210">Type</span></span>   | <span data-ttu-id="04591-211">Datos</span><span class="sxs-lookup"><span data-stu-id="04591-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="04591-212">0</span><span class="sxs-lookup"><span data-stu-id="04591-212">0</span></span>     | <span data-ttu-id="04591-213">string</span><span class="sxs-lookup"><span data-stu-id="04591-213">string</span></span> | <span data-ttu-id="04591-214">null</span><span class="sxs-lookup"><span data-stu-id="04591-214">null</span></span>                                                            |
| <span data-ttu-id="04591-215">1</span><span class="sxs-lookup"><span data-stu-id="04591-215">1</span></span>     | <span data-ttu-id="04591-216">string</span><span class="sxs-lookup"><span data-stu-id="04591-216">string</span></span> | <span data-ttu-id="04591-217">OnAction</span><span class="sxs-lookup"><span data-stu-id="04591-217">MyAction</span></span>                                                        |
| <span data-ttu-id="04591-218">2</span><span class="sxs-lookup"><span data-stu-id="04591-218">2</span></span>     | <span data-ttu-id="04591-219">string</span><span class="sxs-lookup"><span data-stu-id="04591-219">string</span></span> | <span data-ttu-id="04591-220">Esta es la descripción de "OnAction"</span><span class="sxs-lookup"><span data-stu-id="04591-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="04591-221">3</span><span class="sxs-lookup"><span data-stu-id="04591-221">3</span></span>     | <span data-ttu-id="04591-222">string</span><span class="sxs-lookup"><span data-stu-id="04591-222">string</span></span> | <span data-ttu-id="04591-223">Plantilla OnAction: los datos de Campo1 son \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="04591-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="04591-224">los datos del campo 2 son \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="04591-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="04591-225">La plantilla para INSTALLMESSAGE \_ ACTIONSTART (campo 3) hace referencia a los campos 1 y 2, el \_ registro INSTALLMESSAGE ACTIONDATA debe tener 2 campos que contengan los datos garantizados.</span><span class="sxs-lookup"><span data-stu-id="04591-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="04591-226">Los campos pueden ser campos de cadena o de entero.</span><span class="sxs-lookup"><span data-stu-id="04591-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="04591-227">INSTALLMESSAGE \_ ACTIONDATA.</span><span class="sxs-lookup"><span data-stu-id="04591-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="04591-228">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-228">Field</span></span> | <span data-ttu-id="04591-229">Tipo</span><span class="sxs-lookup"><span data-stu-id="04591-229">Type</span></span>   | <span data-ttu-id="04591-230">Datos</span><span class="sxs-lookup"><span data-stu-id="04591-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="04591-231">0</span><span class="sxs-lookup"><span data-stu-id="04591-231">0</span></span>     | <span data-ttu-id="04591-232">string</span><span class="sxs-lookup"><span data-stu-id="04591-232">string</span></span> | <span data-ttu-id="04591-233">null</span><span class="sxs-lookup"><span data-stu-id="04591-233">null</span></span>                    |
| <span data-ttu-id="04591-234">1</span><span class="sxs-lookup"><span data-stu-id="04591-234">1</span></span>     | <span data-ttu-id="04591-235">int</span><span class="sxs-lookup"><span data-stu-id="04591-235">int</span></span>    | <span data-ttu-id="04591-236">2</span><span class="sxs-lookup"><span data-stu-id="04591-236">2</span></span>                       |
| <span data-ttu-id="04591-237">2</span><span class="sxs-lookup"><span data-stu-id="04591-237">2</span></span>     | <span data-ttu-id="04591-238">string</span><span class="sxs-lookup"><span data-stu-id="04591-238">string</span></span> | <span data-ttu-id="04591-239">ActionData para OnAction</span><span class="sxs-lookup"><span data-stu-id="04591-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="04591-240">INSTALLMESSAGE \_ FILESINUSE</span><span class="sxs-lookup"><span data-stu-id="04591-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="04591-241">El registro FILESINUSE es un registro de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="04591-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="04591-242">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-242">Field</span></span> | <span data-ttu-id="04591-243">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04591-244">0</span><span class="sxs-lookup"><span data-stu-id="04591-244">0</span></span>     | <span data-ttu-id="04591-245">Este campo puede ser null.</span><span class="sxs-lookup"><span data-stu-id="04591-245">This field can be null.</span></span> <span data-ttu-id="04591-246">En el caso de una instalación con una interfaz de usuario básica, este campo puede especificar texto estático para su presentación en el [control ListBox](listbox-control.md) del [cuadro de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="04591-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="04591-247">En el caso de una instalación con una interfaz de usuario completa, este campo no tiene ningún efecto porque el texto se especifica mediante la creación del cuadro de diálogo FilesInUse personalizado.</span><span class="sxs-lookup"><span data-stu-id="04591-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="04591-248">1</span><span class="sxs-lookup"><span data-stu-id="04591-248">1</span></span>     | <span data-ttu-id="04591-249">Nombre del archivo en uso.</span><span class="sxs-lookup"><span data-stu-id="04591-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="04591-250">2</span><span class="sxs-lookup"><span data-stu-id="04591-250">2</span></span>     | <span data-ttu-id="04591-251">Este campo identifica el proceso que contiene el archivo en uso. **Windows Installer versión 4,0:** El identificador de proceso (PID) del proceso o el título de la ventana para el proceso.</span><span class="sxs-lookup"><span data-stu-id="04591-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="04591-252">**Windows Installer versión 3,1 y versiones anteriores:** Este campo debe ser el ID. de proceso (PID) del proceso.</span><span class="sxs-lookup"><span data-stu-id="04591-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="04591-253">Por ejemplo, para enviar un mensaje FilesInUse que muestre dos archivos en uso, red.exe y blue.exe, el registro tiene cuatro campos más el campo 0.</span><span class="sxs-lookup"><span data-stu-id="04591-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="04591-254">El formato del registro sería como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="04591-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="04591-255">Este ejemplo requiere Windows Installer versión 4,0.</span><span class="sxs-lookup"><span data-stu-id="04591-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="04591-256">**Windows Installer versión 3,1 y versiones anteriores:** Los campos 2 y 4 del siguiente ejemplo deben contener los PID de los procesos que contienen red.exe y blue.exe en uso.</span><span class="sxs-lookup"><span data-stu-id="04591-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="04591-257">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-257">Field</span></span> | <span data-ttu-id="04591-258">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="04591-259">0</span><span class="sxs-lookup"><span data-stu-id="04591-259">0</span></span>     | <span data-ttu-id="04591-260">null</span><span class="sxs-lookup"><span data-stu-id="04591-260">null</span></span>              |
| <span data-ttu-id="04591-261">1</span><span class="sxs-lookup"><span data-stu-id="04591-261">1</span></span>     | <span data-ttu-id="04591-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="04591-262">Red.exe</span></span>           |
| <span data-ttu-id="04591-263">2</span><span class="sxs-lookup"><span data-stu-id="04591-263">2</span></span>     | <span data-ttu-id="04591-264">Título de la ventana roja</span><span class="sxs-lookup"><span data-stu-id="04591-264">Red Window Title</span></span>  |
| <span data-ttu-id="04591-265">3</span><span class="sxs-lookup"><span data-stu-id="04591-265">3</span></span>     | <span data-ttu-id="04591-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="04591-266">Blue.exe</span></span>          |
| <span data-ttu-id="04591-267">4</span><span class="sxs-lookup"><span data-stu-id="04591-267">4</span></span>     | <span data-ttu-id="04591-268">Título de la ventana azul</span><span class="sxs-lookup"><span data-stu-id="04591-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="04591-269">En Windows Installer versión 4,0, si el PID pasado desde el servicio no tiene un título de ventana, como una aplicación de bandeja del sistema, el archivo no se mostrará y el registro detallado contendrá los mensajes siguientes.</span><span class="sxs-lookup"><span data-stu-id="04591-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="04591-270">INSTALLMESSAGE \_ RESOLVESOURCE</span><span class="sxs-lookup"><span data-stu-id="04591-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="04591-271">El registro de INSTALLMESSAGE \_ RESOLVESOURCE tiene siete campos.</span><span class="sxs-lookup"><span data-stu-id="04591-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="04591-272">Para \_ que INSTALLMESSAGE RESOLVESOURCE funcione correctamente, es posible que un controlador de interfaz de usuario externo no controle el \_ mensaje INSTALLMESSAGE RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="04591-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="04591-273">Windows Installer debe controlar el \_ mensaje RESOLVESOURCE de INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="04591-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="04591-274">Es decir, el controlador de la interfaz de usuario externa devuelve 0 para indicar que no se ha realizado ninguna acción al filtrar el \_ mensaje RESOLVESOURCE de INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="04591-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="04591-275">El procedimiento recomendado es evitar el envío de un mensaje RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="04591-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="04591-276">Campo</span><span class="sxs-lookup"><span data-stu-id="04591-276">Field</span></span> | <span data-ttu-id="04591-277">Descripción</span><span class="sxs-lookup"><span data-stu-id="04591-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04591-278">0</span><span class="sxs-lookup"><span data-stu-id="04591-278">0</span></span>     | <span data-ttu-id="04591-279">null</span><span class="sxs-lookup"><span data-stu-id="04591-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="04591-280">1</span><span class="sxs-lookup"><span data-stu-id="04591-280">1</span></span>     | <span data-ttu-id="04591-281">null</span><span class="sxs-lookup"><span data-stu-id="04591-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="04591-282">2</span><span class="sxs-lookup"><span data-stu-id="04591-282">2</span></span>     | <span data-ttu-id="04591-283">Nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="04591-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="04591-284">3</span><span class="sxs-lookup"><span data-stu-id="04591-284">3</span></span>     | <span data-ttu-id="04591-285">Código de producto.</span><span class="sxs-lookup"><span data-stu-id="04591-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="04591-286">4</span><span class="sxs-lookup"><span data-stu-id="04591-286">4</span></span>     | <span data-ttu-id="04591-287">Ruta de acceso relativa, si se conoce, puede ser null.</span><span class="sxs-lookup"><span data-stu-id="04591-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="04591-288">5</span><span class="sxs-lookup"><span data-stu-id="04591-288">5</span></span>     | <span data-ttu-id="04591-289">0</span><span class="sxs-lookup"><span data-stu-id="04591-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="04591-290">6</span><span class="sxs-lookup"><span data-stu-id="04591-290">6</span></span>     | <span data-ttu-id="04591-291">Indica si se debe validar el código de paquete.</span><span class="sxs-lookup"><span data-stu-id="04591-291">Whether to validate the package code.</span></span> <span data-ttu-id="04591-292">Un valor de ' 1 ' indica que se debe validar el código de paquete.</span><span class="sxs-lookup"><span data-stu-id="04591-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="04591-293">Un valor de "0" indica que el paquete no se debe validar.</span><span class="sxs-lookup"><span data-stu-id="04591-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="04591-294">7</span><span class="sxs-lookup"><span data-stu-id="04591-294">7</span></span>     | <span data-ttu-id="04591-295">Disco requerido de la tabla de medios.</span><span class="sxs-lookup"><span data-stu-id="04591-295">Required disk from media table.</span></span> <span data-ttu-id="04591-296">Un valor de "0" indica que cualquier disco es aceptable.</span><span class="sxs-lookup"><span data-stu-id="04591-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




