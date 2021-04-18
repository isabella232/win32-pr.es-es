---
description: La función SetPrinter establece los datos de una impresora especificada o establece el estado de la impresora especificada mediante la pausa de la impresión, la reanudación de la impresión o la eliminación de todos los trabajos de impresión.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Función SetPrinter (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716481"
---
# <a name="setprinter-function"></a><span data-ttu-id="292f4-103">SetPrinter función)</span><span class="sxs-lookup"><span data-stu-id="292f4-103">SetPrinter function</span></span>

<span data-ttu-id="292f4-104">La función **SetPrinter** establece los datos de una impresora especificada o establece el estado de la impresora especificada mediante la pausa de la impresión, la reanudación de la impresión o la eliminación de todos los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="292f4-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="292f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="292f4-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="292f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="292f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="292f4-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="292f4-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292f4-108">Identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-108">A handle to the printer.</span></span> <span data-ttu-id="292f4-109">Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="292f4-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="292f4-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292f4-111">El tipo de datos que la función almacena en el búfer al que apunta *pPrinter*.</span><span class="sxs-lookup"><span data-stu-id="292f4-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="292f4-112">Si el parámetro de *comando* no es igual a cero, el parámetro *LEVEL* debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="292f4-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="292f4-113">Este valor puede ser 0, 2, 3, 4, 5, 6, 7, 8 o 9.</span><span class="sxs-lookup"><span data-stu-id="292f4-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="292f4-114">*pPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="292f4-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292f4-115">Puntero a un búfer que contiene los datos que se van a establecer para la impresora o que contienen información para el comando especificado por el parámetro de *comando* .</span><span class="sxs-lookup"><span data-stu-id="292f4-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="292f4-116">El tipo de datos del búfer viene determinado por el valor de *LEVEL*.</span><span class="sxs-lookup"><span data-stu-id="292f4-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="292f4-117">Nivel</span><span class="sxs-lookup"><span data-stu-id="292f4-117">Level</span></span>                                                                                                | <span data-ttu-id="292f4-118">Estructura</span><span class="sxs-lookup"><span data-stu-id="292f4-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="292f4-119"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="292f4-120">Si el parámetro de *comando* es el estado del conjunto de control de la impresora, *pPrinter* debe contener un valor **DWORD** que especifique el nuevo estado de la impresora que se va a establecer. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="292f4-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="292f4-121">Para obtener una lista de los valores de estado posibles, vea el miembro **status** de la estructura de la [**impresora \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="292f4-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="292f4-122">Tenga en cuenta que el estado de la **impresora en \_ \_ pausa** y el estado de la **impresora \_ pendiente de \_ \_ eliminación** no son valores de estado válidos para establecer.</span><span class="sxs-lookup"><span data-stu-id="292f4-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="292f4-123">Si el *nivel* es 0, pero el parámetro del *comando* no es el estado del  conjunto de control de la impresora, pPrinter debe ser **null**. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="292f4-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="292f4-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="292f4-125">Estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que contiene información detallada acerca de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="292f4-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="292f4-127">Una estructura de [**información de impresora \_ \_ 3**](printer-info-3.md) que contiene la información de seguridad de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="292f4-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="292f4-129">Una estructura de [**información de impresora \_ \_ 4**](printer-info-4.md) que contiene la información de impresora mínima, incluido el nombre de la impresora, el nombre del servidor y si la impresora es remota o local.</span><span class="sxs-lookup"><span data-stu-id="292f4-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="292f4-130"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="292f4-131">Una estructura de información de impresora [**\_ \_ 5**](printer-info-5.md) que contiene información de la impresora, como los atributos de impresora y la configuración de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="292f4-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="292f4-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="292f4-133">Estructura de la información de la [**impresora \_ \_ 6**](printer-info-6.md) que especifica el valor de estado de una impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="292f4-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="292f4-135">Estructura de la información de la [**impresora \_ \_ 7**](printer-info-7.md) .</span><span class="sxs-lookup"><span data-stu-id="292f4-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="292f4-136">El miembro *dwAction* de esta estructura indica si **SetPrinter** debe publicar, anular la publicación, volver a publicar o actualizar los datos de la impresora en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="292f4-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="292f4-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="292f4-138">Una estructura de la información de la [**impresora \_ \_ 8**](printer-info-8.md) que especifica la configuración de impresora predeterminada global.</span><span class="sxs-lookup"><span data-stu-id="292f4-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="292f4-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="292f4-140">Una estructura de [**información de impresora \_ \_ 9**](printer-info-9.md) que especifica la configuración de impresora predeterminada por usuario.</span><span class="sxs-lookup"><span data-stu-id="292f4-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="292f4-141">*Comando* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="292f4-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292f4-142">la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="292f4-142">The action to perform.</span></span>

<span data-ttu-id="292f4-143">Si el parámetro *LEVEL* es distinto de cero, establezca el valor de este parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="292f4-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="292f4-144">En este caso, la impresora conserva su estado actual y la función vuelve a configurar los datos de la impresora según lo especificado por los parámetros *LEVEL* y *pPrinter* .</span><span class="sxs-lookup"><span data-stu-id="292f4-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="292f4-145">Si el parámetro *LEVEL* es cero, establezca el valor de este parámetro en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="292f4-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="292f4-146">Value</span><span class="sxs-lookup"><span data-stu-id="292f4-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="292f4-147">Significado</span><span class="sxs-lookup"><span data-stu-id="292f4-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="292f4-148"><dt>**pausar control de impresora \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="292f4-149">Pausar la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="292f4-150"><dt>**\_purga de control de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="292f4-151">Elimine todos los trabajos de impresión de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="292f4-152"><dt>**\_reanudación del control de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="292f4-153">Reanudar una impresora en pausa.</span><span class="sxs-lookup"><span data-stu-id="292f4-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="292f4-154"><dt>**\_Estado del \_ conjunto de control de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="292f4-155">Establezca el estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-155">Set the printer status.</span></span><br/> <span data-ttu-id="292f4-156">Establezca el parámetro *pPrinter* en un puntero a un valor **DWORD** que especifique el nuevo estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="292f4-157">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="292f4-157">Return value</span></span>

<span data-ttu-id="292f4-158">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="292f4-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="292f4-159">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="292f4-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="292f4-160">Si el *nivel* es 7 y se produce un error en la acción de publicación, **SetPrinter** devuelve un **error de \_ e/s \_ pendiente** e intenta completar la acción en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="292f4-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="292f4-161">Si el *nivel* es 7 y se produjo un error en la acción de actualización, **SetPrinter** devuelve el **archivo de error \_ \_ no \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="292f4-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="292f4-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="292f4-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="292f4-163">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="292f4-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="292f4-164">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="292f4-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="292f4-165">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="292f4-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="292f4-166">No se puede usar **SetPrinter** para cambiar la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="292f4-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="292f4-167">Para modificar la configuración actual de la impresora, llame a la función [**GetPrinter**](getprinter.md) para recuperar la configuración actual en una estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) , modifique los miembros de dicha estructura según sea necesario y, a continuación, llame a **SetPrinter**.</span><span class="sxs-lookup"><span data-stu-id="292f4-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="292f4-168">La función **SetPrinter** omite los miembros **pServerName**, **AveragePPM**, **status** y **CJobs** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="292f4-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="292f4-169">Al pausar una impresora, se suspende la programación de todos los trabajos de impresión de la impresora, excepto en el caso de los trabajos de impresión que se estén imprimiendo en ese momento.</span><span class="sxs-lookup"><span data-stu-id="292f4-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="292f4-170">Los trabajos de impresión se pueden enviar a una impresora en pausa, pero no se programará ningún trabajo para imprimirlo en la impresora hasta que se reanude la impresión.</span><span class="sxs-lookup"><span data-stu-id="292f4-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="292f4-171">Si una impresora está desactivada, se eliminarán todos los trabajos de impresión de la impresora, excepto el trabajo de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="292f4-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="292f4-172">Si usa **SetPrinter** para modificar la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predeterminada de una impresora (estableciendo globalmente los valores predeterminados de la impresora), primero debe llamar a la función [**DocumentProperties**](documentproperties.md) para validar la estructura **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="292f4-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="292f4-173">En el caso de las estructuras [**Printer \_ info \_ 2**](printer-info-2.md) y [**Printer \_ info \_ 3**](printer-info-3.md) que contienen un puntero a un descriptor de seguridad, la función solo puede establecer los componentes del descriptor de seguridad para los que el autor de la llamada tiene permiso de modificación.</span><span class="sxs-lookup"><span data-stu-id="292f4-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="292f4-174">Para establecer determinados componentes de descriptor de seguridad, debe especificar los derechos de acceso necesarios cuando llame a la función [**OpenPrinter**](openprinter.md) o [**OpenPrinter2**](openprinter2.md) para recuperar un identificador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="292f4-175">En la tabla siguiente se muestran los derechos de acceso necesarios para modificar los distintos componentes del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="292f4-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="292f4-176">Permiso de acceso</span><span class="sxs-lookup"><span data-stu-id="292f4-176">Access permission</span></span>            | <span data-ttu-id="292f4-177">Componente de descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="292f4-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="292f4-178">**propietario de escritura \_**</span><span class="sxs-lookup"><span data-stu-id="292f4-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="292f4-179">Propietario</span><span class="sxs-lookup"><span data-stu-id="292f4-179">Owner</span></span><br/> <span data-ttu-id="292f4-180">Grupo primario</span><span class="sxs-lookup"><span data-stu-id="292f4-180">Primary group</span></span><br/> |
| <span data-ttu-id="292f4-181">**ESCRIBIR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="292f4-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="292f4-182">Lista de control de acceso discrecional (DACL)</span><span class="sxs-lookup"><span data-stu-id="292f4-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="292f4-183">**ACCESO a la \_ seguridad del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="292f4-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="292f4-184">Lista de control de acceso del sistema (SACL)</span><span class="sxs-lookup"><span data-stu-id="292f4-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="292f4-185">Si el descriptor de seguridad contiene un componente que el autor de la llamada no tiene el derecho de acceso para modificarlo, **SetPrinter** produce un error.</span><span class="sxs-lookup"><span data-stu-id="292f4-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="292f4-186">Los componentes de un descriptor de seguridad que no desea modificar deberían ser **nulos** o no estar presentes, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="292f4-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="292f4-187">Si no desea modificar el descriptor de seguridad y está llamando a **SetPrinter** con una estructura de [**\_ información \_ 2**](printer-info-2.md) de la impresora, establezca el miembro **pSecurityDescriptor** de esa estructura en **null**.</span><span class="sxs-lookup"><span data-stu-id="292f4-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="292f4-188">El Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para compartir archivos e impresoras.</span><span class="sxs-lookup"><span data-stu-id="292f4-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="292f4-189">Si un administrador del equipo llama a **SetPrinter** , habilita la excepción.</span><span class="sxs-lookup"><span data-stu-id="292f4-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="292f4-190">Si lo llama un usuario que no es administrador y la excepción aún no se ha habilitado, se produce un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="292f4-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="292f4-191">Puede usar el nivel 7 con la estructura de la [**información de impresora \_ \_ 7**](printer-info-7.md) para publicar, anular la publicación o actualizar los datos del servicio de directorio para la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="292f4-192">Los datos del servicio de directorio para una impresora incluyen todos los datos almacenados en las claves de SPLDS \_ \* mediante llamadas a la función [**SetPrinterDataEx**](setprinterdataex.md) para la impresora.</span><span class="sxs-lookup"><span data-stu-id="292f4-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="292f4-193">Antes de llamar a **SetPrinter**, establezca el miembro **pszObjectGUID** de la información de la **impresora \_ \_ 7** en **null** y establezca el miembro *dwAction* en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="292f4-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="292f4-194">Value</span><span class="sxs-lookup"><span data-stu-id="292f4-194">Value</span></span>                             | <span data-ttu-id="292f4-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="292f4-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292f4-196">**publicación de DSPRINT \_**</span><span class="sxs-lookup"><span data-stu-id="292f4-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="292f4-197">Publica los datos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="292f4-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="292f4-198">**DSPRINT \_ volver a publicar**</span><span class="sxs-lookup"><span data-stu-id="292f4-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="292f4-199">Los datos del servicio de directorio de la impresora no se publican y se vuelven a publicar, actualizando todas las propiedades de la impresora publicada.</span><span class="sxs-lookup"><span data-stu-id="292f4-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="292f4-200">Al volver a publicar también se cambia el GUID de la impresora publicada.</span><span class="sxs-lookup"><span data-stu-id="292f4-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="292f4-201">Use este valor si sospecha que los datos publicados de la impresora están dañados.</span><span class="sxs-lookup"><span data-stu-id="292f4-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="292f4-202">**DSPRINT \_ Anular publicación**</span><span class="sxs-lookup"><span data-stu-id="292f4-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="292f4-203">Anula la publicación de los datos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="292f4-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="292f4-204">**actualización de DSPRINT \_**</span><span class="sxs-lookup"><span data-stu-id="292f4-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="292f4-205">Actualiza los datos del servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="292f4-205">Updates the directory service data.</span></span> <span data-ttu-id="292f4-206">Esto es lo mismo que **DSPRINT \_ PUBLISH**, salvo que se produce un error en **SetPrinter** con el **archivo de error \_ \_ no \_ encontrado** si la impresora no está publicada todavía.</span><span class="sxs-lookup"><span data-stu-id="292f4-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="292f4-207">Use **la \_ actualización de DSPRINT** para actualizar las propiedades publicadas pero no forzar la publicación.</span><span class="sxs-lookup"><span data-stu-id="292f4-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="292f4-208">Los controladores de impresora siempre deben usar **DSPRINT \_ Update** en lugar de **DSPRINT \_ PUBLISH**.</span><span class="sxs-lookup"><span data-stu-id="292f4-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="292f4-209">**DSPRINT \_ PENDING** no es un valor *dwAction* válido para **SetPrinter**.</span><span class="sxs-lookup"><span data-stu-id="292f4-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="292f4-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292f4-210">Requirements</span></span>



| <span data-ttu-id="292f4-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="292f4-211">Requirement</span></span> | <span data-ttu-id="292f4-212">Value</span><span class="sxs-lookup"><span data-stu-id="292f4-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292f4-213">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="292f4-213">Minimum supported client</span></span><br/> | <span data-ttu-id="292f4-214">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="292f4-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="292f4-215">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="292f4-215">Minimum supported server</span></span><br/> | <span data-ttu-id="292f4-216">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="292f4-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="292f4-217">Encabezado</span><span class="sxs-lookup"><span data-stu-id="292f4-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="292f4-218"><dt>WinSpool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="292f4-219">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="292f4-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="292f4-220"><dt>WinSpool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="292f4-221">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="292f4-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="292f4-222"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="292f4-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="292f4-223">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="292f4-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="292f4-224">**SetPrinterW** (Unicode) y **SetPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="292f4-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="292f4-225">Vea también</span><span class="sxs-lookup"><span data-stu-id="292f4-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292f4-226">Impresión</span><span class="sxs-lookup"><span data-stu-id="292f4-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="292f4-227">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="292f4-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="292f4-228">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="292f4-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="292f4-229">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="292f4-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="292f4-230">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="292f4-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="292f4-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="292f4-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="292f4-232">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="292f4-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="292f4-233">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="292f4-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="292f4-234">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="292f4-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="292f4-235">**Información de la impresora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="292f4-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="292f4-236">**Información de la impresora \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="292f4-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="292f4-237">**Información de la impresora \_ \_ 7**</span><span class="sxs-lookup"><span data-stu-id="292f4-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="292f4-238">**Información de la impresora \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="292f4-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="292f4-239">**Información de la impresora \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="292f4-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="292f4-240">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="292f4-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




