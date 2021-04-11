---
description: La función FindNextPrinterChangeNotification recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o un servidor de impresión.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Función FindNextPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910798"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="ed1b0-103">FindNextPrinterChangeNotification función)</span><span class="sxs-lookup"><span data-stu-id="ed1b0-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="ed1b0-104">La función **FindNextPrinterChangeNotification** recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="ed1b0-105">Llame a esta función cuando se satisfaga una operación de espera en el objeto de notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="ed1b0-106">La función también restablece el objeto de notificación de cambios al estado no señalado.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="ed1b0-107">Después, puede usar el objeto en otra operación de espera para seguir supervisando la impresora o el servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="ed1b0-108">El sistema operativo establecerá el objeto en el estado señalado la próxima vez que se produzca uno de un conjunto de cambios especificado en la impresora o el servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="ed1b0-109">La función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crea el objeto de notificación de cambios y especifica el conjunto de cambios que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1b0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed1b0-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ed1b0-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed1b0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1b0-112">*hChange* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed1b0-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1b0-113">Identificador de un objeto de notificación de cambios asociado a una impresora o servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="ed1b0-114">Este identificador se obtiene mediante una llamada a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="ed1b0-115">El sistema operativo establece este objeto de notificación de cambio en el estado señalado cuando detecta uno de los cambios especificados en el filtro de notificación de cambio del objeto.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="ed1b0-116">*pdwChange* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ed1b0-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1b0-117">Puntero a una variable cuyos bits se establecen para indicar los cambios que se produjeron para producir la notificación más reciente.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="ed1b0-118">Los marcadores de bits que se pueden establecer se corresponden con los especificados en el parámetro *fdwFilter* de la llamada a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="ed1b0-119">El sistema establece una o varias de las siguientes marcas de bits.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="ed1b0-120">Value</span><span class="sxs-lookup"><span data-stu-id="ed1b0-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="ed1b0-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ed1b0-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="ed1b0-122"><dt>**\_formulario para \_ Agregar y cambiar la impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="ed1b0-123">Se ha agregado un formulario al servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="ed1b0-124"><dt>**\_ \_ Agregar trabajo de cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="ed1b0-125">Se envió un trabajo de impresión a la impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="ed1b0-126"><dt>**cambio de impresora- \_ \_ agregar \_ Puerto**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="ed1b0-127">Se ha agregado un puerto o un monitor al servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="ed1b0-128"><dt>**cambio de impresora- \_ \_ agregar \_ procesador de impresión \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="ed1b0-129">Se ha agregado un procesador de impresión al servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="ed1b0-130"><dt>**cambio de impresora \_ \_ agregar \_ impresora**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="ed1b0-131">Se ha agregado una impresora al servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="ed1b0-132"><dt>**cambio de impresora- \_ \_ agregar \_ controlador de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="ed1b0-133">Se ha agregado un controlador de impresora al servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="ed1b0-134"><dt>**\_Puerto de \_ configuración de cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="ed1b0-135">Se configuró un puerto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="ed1b0-136"><dt>**\_formulario de \_ eliminación de cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="ed1b0-137">Se eliminó un formulario del servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="ed1b0-138"><dt>**\_trabajo de \_ eliminación de cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="ed1b0-139">Se eliminó un trabajo.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="ed1b0-140"><dt>**\_Puerto de \_ eliminación de cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="ed1b0-141">Se eliminó un puerto o un monitor del servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="ed1b0-142"><dt>**cambio de impresora- \_ \_ eliminar \_ procesador de impresión \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="ed1b0-143">Se eliminó un procesador de impresión del servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="ed1b0-144"><dt>**cambio de impresora- \_ \_ eliminar \_ impresora**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="ed1b0-145">Se eliminó una impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="ed1b0-146"><dt>**\_controlador de \_ impresora para eliminar el cambio de impresora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="ed1b0-147">Se eliminó un controlador de impresora del servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="ed1b0-148"><dt>**\_ \_ no se pudo cambiar la impresora \_ impresora de conexión \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="ed1b0-149">Error en una conexión de impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="ed1b0-150"><dt>**\_formulario de \_ conjunto de cambios de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="ed1b0-151">Se estableció un formulario en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="ed1b0-152"><dt>**\_trabajo de \_ conjunto de cambios de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="ed1b0-153">Se estableció un trabajo.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="ed1b0-154"><dt>**\_impresora de \_ conjunto de cambios de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="ed1b0-155">Se estableció una impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="ed1b0-156"><dt>**\_controlador de \_ impresora de conjunto de cambios de impresora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="ed1b0-157">Se estableció un controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="ed1b0-158"><dt>**\_trabajo de \_ escritura de cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="ed1b0-159">Se escribieron los datos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="ed1b0-160"><dt>**tiempo de espera de \_ cambio de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="ed1b0-161">Se agotó el tiempo de espera del trabajo.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="ed1b0-162"><dt>**\_servidor de cambios de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="ed1b0-163">Windows 7: se ha producido un cambio en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="ed1b0-164">*pPrinterNotifyOptions* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ed1b0-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1b0-165">Puntero a una estructura [**de \_ \_ Opciones de notificación de impresora**](printer-notify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="ed1b0-166">Establezca el miembro **Flags** de esta estructura **en \_ Opciones de notificación de impresora \_ \_ Actualizar** para que la función devuelva los datos actuales de todos los campos supervisados de información de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="ed1b0-167">La función omite todos los demás miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="ed1b0-168">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ed1b0-169">*ppPrinterNotifyInfo* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ed1b0-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed1b0-170">Puntero a una variable de puntero que recibe un puntero a un búfer asignado por el sistema y de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="ed1b0-171">Llame a la función [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) para liberar el búfer cuando termine de usarlo.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="ed1b0-172">Este parámetro puede ser **null** si no se requiere información.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="ed1b0-173">El búfer contiene una estructura de [**\_ \_ información de notificación de impresora**](printer-notify-info.md) , que contiene una matriz de estructuras de [**\_ \_ \_ datos de información de notificación de impresora**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="ed1b0-174">Cada elemento de la matriz contiene información sobre uno de los campos especificados en el parámetro *pPrinterNotifyOptions* de la llamada a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="ed1b0-175">Normalmente, la función solo proporciona datos para los campos que han cambiado para generar la notificación más reciente.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="ed1b0-176">Sin embargo, si la estructura a la que apunta el parámetro *pPrinterNotifyOptions* especifica la **\_ \_ \_ actualización de las opciones de notificación** de la impresora, la función proporciona datos para todos los campos supervisados.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="ed1b0-177">Si el **bit \_ \_ \_ descartado** de la información de notificación de impresora se establece en el miembro de **marcas** de la estructura de [**\_ \_ información de notificación**](printer-notify-info.md) de la impresora, se ha producido un desbordamiento o un error, y es posible que se hayan perdido las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="ed1b0-178">En este caso, no se enviarán notificaciones adicionales hasta que realice una segunda llamada a **FindNextPrinterChangeNotification** que especifique la **\_ \_ \_ actualización de las opciones de notificación** de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1b0-179">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed1b0-179">Return value</span></span>

<span data-ttu-id="ed1b0-180">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ed1b0-181">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1b0-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed1b0-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ed1b0-183">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ed1b0-184">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ed1b0-185">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ed1b0-186">Llame a la función **FindNextPrinterChangeNotification** después de que se haya satisfecho una operación de espera en un objeto de notificación creado por [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="ed1b0-187">La llamada a **FindNextPrinterChangeNotification** permite obtener información sobre el cambio que cumplía la operación de espera y restablece el objeto de notificación para que se pueda señalizar cuando se produzca el siguiente cambio.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="ed1b0-188">Con una excepción, no llame a la función **FindNextPrinterChangeNotification** si el objeto de notificación de cambios no está en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="ed1b0-189">Si una función wait devuelve el valor **de \_ tiempo de espera** de la espera, el objeto de cambio no está en el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="ed1b0-190">Llame a la función **FindNextPrinterChangeNotification** solo si la función wait se realiza correctamente sin que se agote el tiempo de espera. La excepción es cuando se llama a **FindNextPrinterChangeNotification** con el bit de **\_ \_ \_ actualización opciones de notificación de impresora** establecido en el parámetro *pPrinterNotifyOptions* .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="ed1b0-191">Tenga en cuenta que incluso cuando se establece esta marca, sigue siendo posible establecer la marca de notificación de la **\_ \_ información \_ de notificaciones** de la impresora en el parámetro *ppPrinterNotifyInfo* .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="ed1b0-192">Para seguir supervisando los cambios en la impresora o el servidor de impresión, repita el ciclo de llamada a una de las [funciones de espera](/windows/desktop/Sync/wait-functions) y, a continuación, llame a la función **FindNextPrinterChangeNotification** para examinar el cambio y restablecer el objeto de notificación.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="ed1b0-193">**FindNextPrinterChangeNotification** puede combinar varios cambios en el mismo campo de información de la impresora en una sola notificación.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="ed1b0-194">Cuando esto ocurre, la función suele contraer todos los cambios del campo en una única entrada en la matriz de estructuras de [**\_ \_ \_ datos de notificación**](printer-notify-info-data.md) de la impresora en *ppPrinterNotifyInfo*; la única entrada solo informa de la información más reciente.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="ed1b0-195">Sin embargo, para algunos campos de información de trabajos e impresoras, la función puede devolver varias entradas de matriz para el mismo campo.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="ed1b0-196">En este caso, la última entrada de la matriz para el campo informa de los datos actuales y las entradas anteriores contienen los datos de las fases intermedias.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="ed1b0-197">Cuando ya no necesite el objeto de notificación de cambios, ciérrelo llamando a la función [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="ed1b0-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="ed1b0-198">En Windows XP con Service Pack 2 (SP2) y versiones posteriores, el Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para compartir archivos e impresoras.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="ed1b0-199">Si un usuario realiza una conexión de impresora a otro equipo y la excepción no está habilitada, el usuario no recibirá las notificaciones de cambio de la impresora del servidor.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="ed1b0-200">Un administrador del equipo tendrá que habilitar la excepción.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ed1b0-201">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed1b0-201">Examples</span></span>

<span data-ttu-id="ed1b0-202">En el ejemplo de código siguiente se muestra cómo se puede supervisar el estado de la impresora mediante estas funciones.</span><span class="sxs-lookup"><span data-stu-id="ed1b0-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="ed1b0-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed1b0-203">Requirements</span></span>



| <span data-ttu-id="ed1b0-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1b0-204">Requirement</span></span> | <span data-ttu-id="ed1b0-205">Value</span><span class="sxs-lookup"><span data-stu-id="ed1b0-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1b0-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed1b0-206">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1b0-207">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ed1b0-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ed1b0-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed1b0-208">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1b0-209">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed1b0-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ed1b0-210">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed1b0-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1b0-211"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ed1b0-212">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed1b0-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed1b0-213"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ed1b0-214">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed1b0-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed1b0-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed1b0-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ed1b0-216">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed1b0-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1b0-217">Impresión</span><span class="sxs-lookup"><span data-stu-id="ed1b0-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ed1b0-218">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ed1b0-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ed1b0-219">**FindClosePrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ed1b0-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="ed1b0-220">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ed1b0-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="ed1b0-221">**\_información de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="ed1b0-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="ed1b0-222">**\_datos de \_ información de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="ed1b0-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="ed1b0-223">**\_Opciones de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="ed1b0-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

