---
description: La función DocumentProperties recupera o modifica la información de inicialización de la impresora o muestra una hoja de propiedades de configuración de impresora para la impresora especificada.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Función DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156756"
---
# <a name="documentproperties-function"></a><span data-ttu-id="ea63c-103">DocumentProperties (función)</span><span class="sxs-lookup"><span data-stu-id="ea63c-103">DocumentProperties function</span></span>

<span data-ttu-id="ea63c-104">La función **DocumentProperties** recupera o modifica la información de inicialización de la impresora o muestra una hoja de propiedades de configuración de impresora para la impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="ea63c-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea63c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea63c-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="ea63c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea63c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea63c-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea63c-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea63c-108">Identificador de la ventana primaria de la hoja de propiedades de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="ea63c-109">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea63c-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea63c-110">Identificador de un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-110">A handle to a printer object.</span></span> <span data-ttu-id="ea63c-111">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ea63c-112">*pDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea63c-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea63c-113">Un puntero a una cadena terminada en null que especifica el nombre del dispositivo para el que se muestra la hoja de propiedades de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="ea63c-114">*pDevModeOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ea63c-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea63c-115">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que recibe los datos de configuración de la impresora especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ea63c-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="ea63c-116">*pDevModeInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea63c-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea63c-117">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que el sistema operativo utiliza para inicializar los controles de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea63c-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="ea63c-118">Este parámetro solo se usa si la marca **DM \_ in \_ buffer** está establecida en el parámetro *fMode* .</span><span class="sxs-lookup"><span data-stu-id="ea63c-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="ea63c-119">Si no se establece **DM \_ in \_ buffer** , el sistema operativo utiliza el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)predeterminado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="ea63c-120">*fMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea63c-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea63c-121">Las operaciones que realiza la función.</span><span class="sxs-lookup"><span data-stu-id="ea63c-121">The operations the function performs.</span></span> <span data-ttu-id="ea63c-122">Si este parámetro es cero, la función **DocumentProperties** devuelve el número de bytes requeridos por la estructura de datos [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) del controlador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="ea63c-123">De lo contrario, use una o varias de las constantes siguientes para construir un valor para este parámetro; Tenga en cuenta, sin embargo, que para cambiar la configuración de impresión, una aplicación debe especificar al menos un valor de entrada y un valor de salida.</span><span class="sxs-lookup"><span data-stu-id="ea63c-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="ea63c-124">Value</span><span class="sxs-lookup"><span data-stu-id="ea63c-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="ea63c-125">Significado</span><span class="sxs-lookup"><span data-stu-id="ea63c-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="ea63c-126"><dt>**DM \_ en \_ búfer**</dt></span><span class="sxs-lookup"><span data-stu-id="ea63c-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="ea63c-127">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea63c-127">Input value.</span></span> <span data-ttu-id="ea63c-128">Antes de solicitar, copiar o actualizar, la función combina la configuración de impresión actual del controlador de la impresora con la configuración de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada por el parámetro *pDevModeInput* .</span><span class="sxs-lookup"><span data-stu-id="ea63c-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="ea63c-129">La función actualiza la estructura solo para los miembros especificados por el miembro **dmFields** de la estructura **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="ea63c-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="ea63c-130">Este valor también se define como **DM \_ Modify**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="ea63c-131">En casos de conflicto durante la combinación, la configuración de la estructura **DEVMODE** especificada por *pDevModeInput* invalida la configuración de impresión actual del controlador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="ea63c-132"><dt>**DM \_ en el \_ símbolo del sistema**</dt></span><span class="sxs-lookup"><span data-stu-id="ea63c-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="ea63c-133">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea63c-133">Input value.</span></span> <span data-ttu-id="ea63c-134">La función presenta la hoja de propiedades de configuración de impresión del controlador de impresora y, a continuación, cambia la configuración de la estructura de datos [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) de la impresora a los valores especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ea63c-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="ea63c-135">Este valor también se define como **\_ prompt de DM**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="ea63c-136"><dt>**búfer de DM \_ out \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ea63c-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="ea63c-137">Valor de salida.</span><span class="sxs-lookup"><span data-stu-id="ea63c-137">Output value.</span></span> <span data-ttu-id="ea63c-138">La función escribe la configuración de impresión actual del controlador de la impresora, incluidos los datos privados, en la estructura de datos [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada por el parámetro *pDevModeOutput* .</span><span class="sxs-lookup"><span data-stu-id="ea63c-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="ea63c-139">El autor de la llamada debe asignar un búfer lo suficientemente grande como para contener la información.</span><span class="sxs-lookup"><span data-stu-id="ea63c-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="ea63c-140">Si los conjuntos **de \_ \_ búferes de DM out** están claros, el parámetro *pDevModeOutput* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="ea63c-141">Este valor también se define como **\_ copia de DM**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea63c-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea63c-142">Return value</span></span>

<span data-ttu-id="ea63c-143">Si el parámetro *fMode* es cero, el valor devuelto es el tamaño del búfer necesario para contener los datos de inicialización del controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="ea63c-144">Tenga en cuenta que este búfer puede ser mayor que una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) si el controlador de impresora anexa datos privados a la estructura.</span><span class="sxs-lookup"><span data-stu-id="ea63c-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="ea63c-145">Si la función muestra la hoja de propiedades, el valor devuelto es **IDOK** o **IDCANCEL**, según el botón que seleccione el usuario.</span><span class="sxs-lookup"><span data-stu-id="ea63c-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="ea63c-146">Si la función no muestra la hoja de propiedades y es correcta, el valor devuelto es **IDOK**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="ea63c-147">Si se produce un error en la función, el valor devuelto es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="ea63c-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea63c-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea63c-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea63c-149">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ea63c-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ea63c-150">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea63c-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ea63c-151">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="ea63c-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ea63c-152">La cadena a la que apunta el parámetro *pDeviceName* se puede obtener llamando a la función [**GetPrinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="ea63c-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="ea63c-153">La estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) usada realmente por un controlador de impresora contiene la parte independiente del dispositivo (tal y como se definió anteriormente) seguida de una parte específica del controlador que varía en tamaño y contenido con cada controlador y versión del controlador.</span><span class="sxs-lookup"><span data-stu-id="ea63c-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="ea63c-154">Debido a esta dependencia del controlador, es muy importante que las aplicaciones consulten al controlador el tamaño correcto de la estructura **DEVMODE** antes de asignar un búfer.</span><span class="sxs-lookup"><span data-stu-id="ea63c-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="ea63c-155">**Para realizar cambios en la configuración de impresión local para una aplicación, una aplicación debe seguir estos pasos:**</span><span class="sxs-lookup"><span data-stu-id="ea63c-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="ea63c-156">Obtiene el número de bytes necesario para la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa llamando a **DocumentProperties** y especificando cero en el parámetro *fMode* .</span><span class="sxs-lookup"><span data-stu-id="ea63c-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="ea63c-157">Asigne memoria para la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.</span><span class="sxs-lookup"><span data-stu-id="ea63c-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="ea63c-158">Obtener la configuración actual de la impresora llamando a **DocumentProperties**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="ea63c-159">Pase un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) asignada en el paso 2 como parámetro *pDevModeOutput* y especifique el valor del **búfer de DM \_ out \_** .</span><span class="sxs-lookup"><span data-stu-id="ea63c-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="ea63c-160">Modifique los miembros adecuados de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelta e indique qué miembros se cambiaron estableciendo los bits correspondientes en el miembro **dmFields** de **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="ea63c-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="ea63c-161">Llame a **DocumentProperties** y pase la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificada como parámetros *pDevModeInput* y *PDevModeOutput* y especifique los valores **de búfer DM \_ in \_ buffer** y **DM \_ out \_** (que se combinan mediante el operador OR). La estructura **DEVMODE** devuelta por la tercera llamada a **DocumentProperties** se puede usar como argumento en una llamada a la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .</span><span class="sxs-lookup"><span data-stu-id="ea63c-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="ea63c-162">Para crear un identificador para un contexto de dispositivo de impresora mediante la configuración actual de la impresora, solo tiene que llamar a **DocumentProperties** dos veces, tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ea63c-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="ea63c-163">La primera llamada obtiene el tamaño del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completo y la segunda llamada inicializa el **DEVMODE** con la configuración de la impresora actual.</span><span class="sxs-lookup"><span data-stu-id="ea63c-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="ea63c-164">Pase el **DEVMODE** inicializado a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) para obtener el identificador del contexto del dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="ea63c-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea63c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea63c-165">Requirements</span></span>



| <span data-ttu-id="ea63c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea63c-166">Requirement</span></span> | <span data-ttu-id="ea63c-167">Value</span><span class="sxs-lookup"><span data-stu-id="ea63c-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea63c-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea63c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ea63c-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea63c-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea63c-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea63c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ea63c-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea63c-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea63c-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea63c-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea63c-173"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea63c-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ea63c-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea63c-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea63c-175"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea63c-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ea63c-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea63c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea63c-177"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ea63c-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ea63c-178">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ea63c-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea63c-179">**DocumentPropertiesW** (Unicode) y **DocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ea63c-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ea63c-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea63c-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea63c-181">Impresión</span><span class="sxs-lookup"><span data-stu-id="ea63c-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ea63c-182">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ea63c-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ea63c-183">**AdvancedDocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="ea63c-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="ea63c-184">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="ea63c-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="ea63c-185">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="ea63c-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="ea63c-186">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ea63c-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ea63c-187">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ea63c-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

