---
description: El método Message del objeto Session realiza cualquier operación de registro habilitada y pospone la ejecución al objeto de controlador de interfaz de usuario asociado al motor. Es posible que el registro esté habilitado de forma selectiva para los distintos tipos de mensajes. Vea el método EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653980"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="9a3f2-105">Session. Message (método)</span><span class="sxs-lookup"><span data-stu-id="9a3f2-105">Session.Message method</span></span>

<span data-ttu-id="9a3f2-106">El método **Message** del objeto [**Session**](session-object.md) realiza cualquier operación de registro habilitada y pospone la ejecución al objeto de controlador de interfaz de usuario asociado al motor.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="9a3f2-107">Es posible que el registro esté habilitado de forma selectiva para los distintos tipos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="9a3f2-108">Vea el método [**EnableLog**](installer-enablelog.md) .</span><span class="sxs-lookup"><span data-stu-id="9a3f2-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="9a3f2-109">Si el campo de registro 0 contiene una cadena de formato, se utiliza para dar formato a los datos de los demás campos.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="9a3f2-110">De lo contrario, si el mensaje es un error, una advertencia o un mensaje de usuario, se realiza un intento de buscar una plantilla de mensaje en la tabla de errores de la base de datos actual con el número de error encontrado en el campo 1 del registro para los tipos de mensaje y los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3f2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a3f2-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="9a3f2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a3f2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a3f2-113">*tipo*</span><span class="sxs-lookup"><span data-stu-id="9a3f2-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="9a3f2-114">El parámetro *Kind* debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="9a3f2-115">Para mostrar un cuadro de mensaje con botones e iconos de inserciones, calcule el valor de *Kind* agregando los estilos de cuadro de mensaje estándar usados por [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) y [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiMessageTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="9a3f2-116">Para obtener más información, vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="9a3f2-117">Constante</span><span class="sxs-lookup"><span data-stu-id="9a3f2-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="9a3f2-118">Significado</span><span class="sxs-lookup"><span data-stu-id="9a3f2-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="9a3f2-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="9a3f2-120">Finalización prematura, posible falta de memoria.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="9a3f2-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="9a3f2-122">Mensaje de error con formato, \[ 1 \] es el número de mensaje en la [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="9a3f2-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="9a3f2-124">Mensaje de advertencia con formato, \[ 1 \] es el número de mensaje en la [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="9a3f2-125"><dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="9a3f2-126">Mensaje de solicitud de usuario, \[ 1 \] es el número de mensaje en la [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="9a3f2-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="9a3f2-128">Mensaje informativo para el registro; no se mostrará.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="9a3f2-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="9a3f2-130">Lista de archivos en uso que se deben reemplazar.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="9a3f2-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="9a3f2-132">Solicitud para determinar una ubicación de origen válida.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="9a3f2-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="9a3f2-134">Mensaje de espacio en disco insuficiente.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="9a3f2-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="9a3f2-136">Inicio de la acción, \[ 1 \] nombre de acción, \[ 2 \] Descripción, \[ 3 \] plantilla para mensajes ACTIONDATA.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="9a3f2-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="9a3f2-138">Datos de la acción.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-138">Action data.</span></span> <span data-ttu-id="9a3f2-139">Los campos de registro corresponden a la plantilla del mensaje ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="9a3f2-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="9a3f2-141">Información de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-141">Progress bar information.</span></span> <span data-ttu-id="9a3f2-142">Vea la descripción de los campos de registro a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="9a3f2-143"><dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="9a3f2-144">Para habilitar el botón Cancelar \[ , establezca 1 \] en 2 y \[ 2 \] en 1.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="9a3f2-145">Para deshabilitar el botón Cancelar \[ establecido \] en 1 a 2 y \[ 2 \] en 0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9a3f2-146">*record*</span><span class="sxs-lookup"><span data-stu-id="9a3f2-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="9a3f2-147">Objeto de [**registro**](record-object.md) necesario que contiene un campo específico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a3f2-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a3f2-148">Return value</span></span>



| <span data-ttu-id="9a3f2-149">Constante</span><span class="sxs-lookup"><span data-stu-id="9a3f2-149">Constant</span></span>                                                                                              | <span data-ttu-id="9a3f2-150">Value</span><span class="sxs-lookup"><span data-stu-id="9a3f2-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="9a3f2-151"><dt>**msiMessageStatusError**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="9a3f2-152">-1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="9a3f2-153"><dt>**msiMessageStatusNone**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="9a3f2-154">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-155"><dt>**msiMessageStatusOk**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="9a3f2-156">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-157"><dt>**msiMessageStatusCancel**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="9a3f2-158">2</span><span class="sxs-lookup"><span data-stu-id="9a3f2-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-159"><dt>**msiMessageStatusAbort**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="9a3f2-160">3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-161"><dt>**msiMessageStatusRetry**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="9a3f2-162">4</span><span class="sxs-lookup"><span data-stu-id="9a3f2-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-163"><dt>**msiMessageStatusIgnore**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="9a3f2-164">5</span><span class="sxs-lookup"><span data-stu-id="9a3f2-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-165"><dt>**msiMessageStatusYes**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="9a3f2-166">6</span><span class="sxs-lookup"><span data-stu-id="9a3f2-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="9a3f2-167"><dt>**msiMessageStatusNo**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="9a3f2-168">7</span><span class="sxs-lookup"><span data-stu-id="9a3f2-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="9a3f2-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a3f2-169">Remarks</span></span>

<span data-ttu-id="9a3f2-170">**Campos de registro de mensajes**</span><span class="sxs-lookup"><span data-stu-id="9a3f2-170">**Message Record Fields**</span></span>

<span data-ttu-id="9a3f2-171">A continuación se describen las definiciones de campos de registro cuando se pasa msiMessageTypeProgress como el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="9a3f2-172">El campo 1 especifica el tipo de mensaje de progreso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="9a3f2-173">El significado de los demás campos depende del valor de este campo.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="9a3f2-174">Los valores posibles que se pueden establecer en el campo 1 son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="9a3f2-175">Nombre del mensaje</span><span class="sxs-lookup"><span data-stu-id="9a3f2-175">Message name</span></span>     | <span data-ttu-id="9a3f2-176">Value</span><span class="sxs-lookup"><span data-stu-id="9a3f2-176">Value</span></span> | <span data-ttu-id="9a3f2-177">Descripción del campo 1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3f2-178">MasterReset</span><span class="sxs-lookup"><span data-stu-id="9a3f2-178">MasterReset</span></span>      | <span data-ttu-id="9a3f2-179">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-179">0</span></span>     | <span data-ttu-id="9a3f2-180">Restablece la barra de progreso y establece el número total esperado de TICs en la barra.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="9a3f2-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="9a3f2-181">ActionInfo</span></span>       | <span data-ttu-id="9a3f2-182">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-182">1</span></span>     | <span data-ttu-id="9a3f2-183">Proporciona información relacionada con los mensajes de progreso que va a enviar la acción actual.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="9a3f2-184">ProgressReport</span><span class="sxs-lookup"><span data-stu-id="9a3f2-184">ProgressReport</span></span>   | <span data-ttu-id="9a3f2-185">2</span><span class="sxs-lookup"><span data-stu-id="9a3f2-185">2</span></span>     | <span data-ttu-id="9a3f2-186">Incrementa la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="9a3f2-187">ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="9a3f2-187">ProgressAddition</span></span> | <span data-ttu-id="9a3f2-188">3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-188">3</span></span>     | <span data-ttu-id="9a3f2-189">Habilita una acción (como CustomAction) para agregar TICs al número total esperado de progreso de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="9a3f2-190">El significado del campo 2 depende del valor del campo 1 como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="9a3f2-191">Valor del campo 1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-191">Field 1 value</span></span> | <span data-ttu-id="9a3f2-192">Descripción del campo 2</span><span class="sxs-lookup"><span data-stu-id="9a3f2-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3f2-193">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-193">0</span></span>             | <span data-ttu-id="9a3f2-194">Se esperaba el número total de TICs en la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="9a3f2-195">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-195">1</span></span>             | <span data-ttu-id="9a3f2-196">Número de pasos que la barra de progreso mueve para cada mensaje de ActionData.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="9a3f2-197">Este campo se omite si el campo 3 es 0.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="9a3f2-198">2</span><span class="sxs-lookup"><span data-stu-id="9a3f2-198">2</span></span>             | <span data-ttu-id="9a3f2-199">Número de pasos que se ha desplace la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="9a3f2-200">3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-200">3</span></span>             | <span data-ttu-id="9a3f2-201">Número de pasos que se van a agregar al progreso total esperado.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="9a3f2-202">El significado del campo 3 depende del valor del campo 1 como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="9a3f2-203">Valor del campo 1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-203">Field 1 value</span></span> | <span data-ttu-id="9a3f2-204">Valor del campo 3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-204">Field 3 value</span></span> | <span data-ttu-id="9a3f2-205">Descripción del campo 3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3f2-206">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-206">0</span></span>             | <span data-ttu-id="9a3f2-207">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-207">0</span></span>             | <span data-ttu-id="9a3f2-208">Barra de progreso de avance (de izquierda a derecha)</span><span class="sxs-lookup"><span data-stu-id="9a3f2-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="9a3f2-209">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-209">1</span></span>             | <span data-ttu-id="9a3f2-210">Barra de progreso hacia atrás (de derecha a izquierda)</span><span class="sxs-lookup"><span data-stu-id="9a3f2-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="9a3f2-211">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-211">1</span></span>             | <span data-ttu-id="9a3f2-212">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-212">0</span></span>             | <span data-ttu-id="9a3f2-213">La acción actual enviará mensajes ProgressReport explícitos.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="9a3f2-214">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-214">1</span></span>             | <span data-ttu-id="9a3f2-215">Incremente la barra de progreso en función del número de pasos especificados en el campo 2 cada vez que se envíe un mensaje de ActionData.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="9a3f2-216">2</span><span class="sxs-lookup"><span data-stu-id="9a3f2-216">2</span></span>             | <span data-ttu-id="9a3f2-217">No utilizado</span><span class="sxs-lookup"><span data-stu-id="9a3f2-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="9a3f2-218">3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-218">3</span></span>             | <span data-ttu-id="9a3f2-219">No utilizado</span><span class="sxs-lookup"><span data-stu-id="9a3f2-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="9a3f2-220">El significado del campo 4 depende del valor del campo 1 como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="9a3f2-221">Valor del campo 1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-221">Field 1 value</span></span> | <span data-ttu-id="9a3f2-222">Valor del campo 4</span><span class="sxs-lookup"><span data-stu-id="9a3f2-222">Field 4 value</span></span> | <span data-ttu-id="9a3f2-223">Descripción del campo 4</span><span class="sxs-lookup"><span data-stu-id="9a3f2-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3f2-224">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-224">0</span></span>             | <span data-ttu-id="9a3f2-225">0</span><span class="sxs-lookup"><span data-stu-id="9a3f2-225">0</span></span>             | <span data-ttu-id="9a3f2-226">La ejecución está en curso.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-226">Execution is in progress.</span></span> <span data-ttu-id="9a3f2-227">En este caso, la interfaz de usuario podría calcular y mostrar el tiempo restante.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="9a3f2-228">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-228">1</span></span>             | <span data-ttu-id="9a3f2-229">Crear el script de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-229">Creating the execution script.</span></span> <span data-ttu-id="9a3f2-230">En este caso, la interfaz de usuario podría mostrar un mensaje para esperar mientras el instalador termina de preparar la instalación.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="9a3f2-231">1</span><span class="sxs-lookup"><span data-stu-id="9a3f2-231">1</span></span>             | <span data-ttu-id="9a3f2-232">No utilizado</span><span class="sxs-lookup"><span data-stu-id="9a3f2-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="9a3f2-233">2</span><span class="sxs-lookup"><span data-stu-id="9a3f2-233">2</span></span>             | <span data-ttu-id="9a3f2-234">No utilizado</span><span class="sxs-lookup"><span data-stu-id="9a3f2-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="9a3f2-235">3</span><span class="sxs-lookup"><span data-stu-id="9a3f2-235">3</span></span>             | <span data-ttu-id="9a3f2-236">No utilizado</span><span class="sxs-lookup"><span data-stu-id="9a3f2-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="9a3f2-237">**Mostrar cuadros de mensaje**</span><span class="sxs-lookup"><span data-stu-id="9a3f2-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="9a3f2-238">Para mostrar un cuadro de mensaje con botones e iconos de inserciones, calcule el valor de *Kind* agregando los estilos de cuadro de mensaje estándar usados por **MessageBox** y **MessageBoxEx** a **msiMessageTypeError**, **msiMessageTypeWarning** o **msiTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="9a3f2-239">Las opciones disponibles del botón de opción para VBScript son vbOKOnly (MB \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (MB \_ ABORTRETRYIGNORE), vbYesNoCancel (MB \_ YESNOCANCEL), vbYesNo (MB \_ SÍNO) y vbRetryCancel (MB \_ RETRYCANCEL).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="9a3f2-240">Las opciones de icono disponibles para VBScript son vbCritical (MB \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (MB \_ ICONWARNING) y vbInformation (MB \_ ICONINFORMATION).</span><span class="sxs-lookup"><span data-stu-id="9a3f2-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="9a3f2-241">Por ejemplo, la siguiente llamada envía un mensaje **msiMessageTypeError** con los botones VbExclamation y vbYesNo.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="9a3f2-242">Si una acción personalizada llama al método de **mensaje** , la acción personalizada debe ser capaz de controlar una cancelación por parte del usuario y debe devolver **msiDoActionStatusUserExit**.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a3f2-243">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a3f2-243">Requirements</span></span>



| <span data-ttu-id="9a3f2-244">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a3f2-244">Requirement</span></span> | <span data-ttu-id="9a3f2-245">Value</span><span class="sxs-lookup"><span data-stu-id="9a3f2-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3f2-246">Versión</span><span class="sxs-lookup"><span data-stu-id="9a3f2-246">Version</span></span><br/> | <span data-ttu-id="9a3f2-247">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9a3f2-248">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a3f2-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9a3f2-249">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a3f2-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9a3f2-250">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a3f2-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a3f2-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a3f2-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9a3f2-252">IID</span><span class="sxs-lookup"><span data-stu-id="9a3f2-252">IID</span></span><br/>     | <span data-ttu-id="9a3f2-253">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9a3f2-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
