---
description: Recupera una gran variedad de información de la batería.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: Código de control de IOCTL_BATTERY_QUERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001957"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="cc91e-103">\_Código de \_ control de información de consulta de batería ioctl \_</span><span class="sxs-lookup"><span data-stu-id="cc91e-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="cc91e-104">Recupera una gran variedad de información de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="cc91e-105">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc91e-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="cc91e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc91e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc91e-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="cc91e-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-108">Identificador de la batería en la que se va a devolver información.</span><span class="sxs-lookup"><span data-stu-id="cc91e-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="cc91e-109">Para recuperar un identificador de dispositivo, llame a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="cc91e-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="cc91e-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="cc91e-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="cc91e-111">The control code for the operation.</span></span> <span data-ttu-id="cc91e-112">Este valor identifica la operación específica que se va a realizar y el tipo de dispositivo en el que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="cc91e-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="cc91e-113">Utilice **la \_ \_ \_ información de consulta** de la batería de ioctl para esta operación.</span><span class="sxs-lookup"><span data-stu-id="cc91e-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="cc91e-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="cc91e-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-115">Puntero a una estructura [**de \_ \_ información de consulta**](battery-query-information-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc91e-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="cc91e-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-117">Tamaño del búfer de entrada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cc91e-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cc91e-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="cc91e-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-119">Puntero al búfer de retorno.</span><span class="sxs-lookup"><span data-stu-id="cc91e-119">A pointer to the return buffer.</span></span> <span data-ttu-id="cc91e-120">El tipo de datos (y, por lo tanto, el tamaño) del búfer de retorno depende de la información solicitada en el miembro del **\_ nivel de \_ información \_ de consulta** de la batería de la estructura de información de consulta de la batería de entrada. [**\_ \_**](battery-query-information-str.md)</span><span class="sxs-lookup"><span data-stu-id="cc91e-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="cc91e-121">En la tabla siguiente se muestran los datos devueltos por un nivel de información determinado.</span><span class="sxs-lookup"><span data-stu-id="cc91e-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="cc91e-122">Nivel de información</span><span class="sxs-lookup"><span data-stu-id="cc91e-122">Information level</span></span>                 | <span data-ttu-id="cc91e-123">Datos devueltos</span><span class="sxs-lookup"><span data-stu-id="cc91e-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc91e-124">**BatteryDeviceName**</span><span class="sxs-lookup"><span data-stu-id="cc91e-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="cc91e-125">Cadena Unicode terminada en **null** que especifica el nombre de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cc91e-126">**BatteryEstimatedTime**</span><span class="sxs-lookup"><span data-stu-id="cc91e-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="cc91e-127">**ULong** que especifica el tiempo de ejecución estimado de la batería, en segundos.</span><span class="sxs-lookup"><span data-stu-id="cc91e-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="cc91e-128">Si la tasa de purga proporcionada en el miembro **AtRate** de la estructura de [**\_ \_ información de consulta**](battery-query-information-str.md) de la batería es cero, este cálculo se basa en la tasa de consumo actual.</span><span class="sxs-lookup"><span data-stu-id="cc91e-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="cc91e-129">Si **AtRate** es distinto de cero, la hora devuelta es el tiempo de ejecución esperado para la tasa especificada.</span><span class="sxs-lookup"><span data-stu-id="cc91e-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="cc91e-130">Si el tiempo estimado es desconocido (por ejemplo, la batería no se está descargando y **AtRate** es cero), se devuelve la **\_ \_ hora desconocida** de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="cc91e-131">Tenga en cuenta que este valor no es muy preciso en algunos sistemas de batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="cc91e-132">El valor puede variar considerablemente en función del uso de energía presente, que podría verse afectado por la actividad del disco y otros factores.</span><span class="sxs-lookup"><span data-stu-id="cc91e-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="cc91e-133">No hay ningún mecanismo de notificación para los cambios en este valor.</span><span class="sxs-lookup"><span data-stu-id="cc91e-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="cc91e-134">**BatteryGranularityInformation**</span><span class="sxs-lookup"><span data-stu-id="cc91e-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="cc91e-135">Una matriz de longitud variable de estructuras de [**\_ \_ escalado de informes de batería**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) que contiene la granularidad de los informes para la capacidad de la batería que se devuelve del estado de las consultas de la [**batería de ioctl \_ \_ \_**](ioctl-battery-query-status.md).</span><span class="sxs-lookup"><span data-stu-id="cc91e-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="cc91e-136">Se devuelven varias entradas cuando la granularidad depende de la capacidad actual de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="cc91e-137">Vea **\_ \_ escalado de informes de batería** para la interpretación de la matriz de entradas.</span><span class="sxs-lookup"><span data-stu-id="cc91e-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="cc91e-138">El número de entradas se indica por el tamaño del búfer devuelto y se puede calcular como (*lpBytesReturned* /sizeof (escala de **generación \_ de \_ informes de batería**)).</span><span class="sxs-lookup"><span data-stu-id="cc91e-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="cc91e-139">El número máximo de entradas que se devolverá es cuatro.</span><span class="sxs-lookup"><span data-stu-id="cc91e-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="cc91e-140">**BatteryInformation**</span><span class="sxs-lookup"><span data-stu-id="cc91e-140">**BatteryInformation**</span></span>            | <span data-ttu-id="cc91e-141">Estructura [**de \_ información**](battery-information-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cc91e-142">**BatteryManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="cc91e-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="cc91e-143">Una estructura de [**\_ \_ fecha de fabricación**](battery-manufacture-date-str.md) de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cc91e-144">**BatteryManufactureName**</span><span class="sxs-lookup"><span data-stu-id="cc91e-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="cc91e-145">Cadena Unicode terminada en **null** que contiene el nombre del fabricante de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cc91e-146">**BatterySerialNumber**</span><span class="sxs-lookup"><span data-stu-id="cc91e-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="cc91e-147">Cadena Unicode terminada en **null** que contiene el número de serie de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cc91e-148">**BatteryTemperature**</span><span class="sxs-lookup"><span data-stu-id="cc91e-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="cc91e-149">**ULong** que contiene la temperatura actual de la batería, en décimas de grado Kelvin.</span><span class="sxs-lookup"><span data-stu-id="cc91e-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cc91e-150">**BatteryUniqueID**</span><span class="sxs-lookup"><span data-stu-id="cc91e-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="cc91e-151">Cadena Unicode terminada en **null** que identifica de forma única la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="cc91e-152">Este valor se puede usar para realizar el seguimiento de una batería específica.</span><span class="sxs-lookup"><span data-stu-id="cc91e-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="cc91e-153">En el caso de las baterías inteligentes, este identificador será la concatenación del nombre del fabricante, el nombre del dispositivo, la fecha de fabricación y una representación imprimible del número de serie.</span><span class="sxs-lookup"><span data-stu-id="cc91e-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="cc91e-154">Este valor no está diseñado para mostrarse al usuario.</span><span class="sxs-lookup"><span data-stu-id="cc91e-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="cc91e-155">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="cc91e-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-156">Tamaño del búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cc91e-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="cc91e-157">Dependiendo del nivel de información de los datos solicitados, puede tratarse de un búfer de tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="cc91e-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cc91e-158">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="cc91e-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-159">Puntero a una variable que recibe el tamaño de los datos devueltos en el búfer de *lpOutBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="cc91e-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="cc91e-160">Si el búfer de salida es demasiado pequeño para devolver datos, se produce un error en la llamada, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de código **\_ insuficiente \_ búfer** y el recuento de bytes devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="cc91e-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="cc91e-161">Si *lpOverlapped* es **null** (Nonoverlapped de e/s), *lpBytesReturned* no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cc91e-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="cc91e-162">Si *lpOverlapped* no es **null** (e/s superpuesta), *lpBytesReturned* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cc91e-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="cc91e-163">Si se trata de una operación superpuesta, puede recuperar el número de bytes devueltos mediante una llamada a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="cc91e-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="cc91e-164">Si *hDevice* está asociado a un puerto de finalización de e/s, puede obtener el número de bytes devueltos mediante una llamada a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="cc91e-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="cc91e-165">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="cc91e-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="cc91e-166">Puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="cc91e-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="cc91e-167">Si *hDevice* se abrió con la marca de **indicador de archivo \_ \_ superpuesto** , *lpOverlapped* debe apuntar a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="cc91e-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="cc91e-168">En este caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="cc91e-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="cc91e-169">Si el dispositivo se ha abierto con la marca de **indicador de archivo \_ \_ superpuesto** y *lpOverlapped* es **null**, la función genera un error de manera imprevisible.</span><span class="sxs-lookup"><span data-stu-id="cc91e-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="cc91e-170">Si *hDevice* se ha abierto sin especificar la marca de la **marca de archivo \_ \_ superpuesta** , *lpOverlapped* se omite y la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) no vuelve hasta que se ha completado la operación o hasta que se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cc91e-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc91e-171">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc91e-171">Return value</span></span>

<span data-ttu-id="cc91e-172">Si la operación se completa correctamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cc91e-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="cc91e-173">Si se produce un error en la operación o está pendiente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cc91e-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="cc91e-174">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cc91e-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="cc91e-175">Parte de la información sobre las baterías es opcional o puede no tener sentido para algunas baterías.</span><span class="sxs-lookup"><span data-stu-id="cc91e-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="cc91e-176">Si el tipo de datos solicitado no está disponible para la batería actual, se devuelve un **error de \_ \_ función no válida** .</span><span class="sxs-lookup"><span data-stu-id="cc91e-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="cc91e-177">Todas las solicitudes de información de batería se completarán con el estado **\_ \_ no \_ se encontró el archivo de error** cuando el elemento **BatteryTag** de la solicitud no coincide con el de la etiqueta de la batería actual.</span><span class="sxs-lookup"><span data-stu-id="cc91e-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="cc91e-178">Esto garantiza que la información de la batería devuelta coincida con la de la batería solicitada.</span><span class="sxs-lookup"><span data-stu-id="cc91e-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="cc91e-179">(Consulte [etiquetas de batería](battery-information.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="cc91e-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="cc91e-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc91e-180">Remarks</span></span>

<span data-ttu-id="cc91e-181">Este IOCTL de la batería recupera una gran variedad de información de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="cc91e-182">La estructura de parámetros de entrada, [**\_ \_ información de consulta**](battery-query-information-str.md)de la batería, indica el tipo de información que se va a devolver y cuándo se debe devolver la información de la batería.</span><span class="sxs-lookup"><span data-stu-id="cc91e-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="cc91e-183">El tipo de datos y el contenido del búfer de salida varían en función de los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="cc91e-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="cc91e-184">Para conocer las implicaciones de la e/s superpuesta en esta operación, consulte la sección Comentarios del tema [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="cc91e-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="cc91e-185">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc91e-185">Examples</span></span>

<span data-ttu-id="cc91e-186">Para obtener un ejemplo, consulte [enumeración de dispositivos de batería](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="cc91e-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc91e-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc91e-187">Requirements</span></span>



| <span data-ttu-id="cc91e-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc91e-188">Requirement</span></span> | <span data-ttu-id="cc91e-189">Value</span><span class="sxs-lookup"><span data-stu-id="cc91e-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc91e-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc91e-190">Minimum supported client</span></span><br/> | <span data-ttu-id="cc91e-191">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cc91e-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="cc91e-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc91e-192">Minimum supported server</span></span><br/> | <span data-ttu-id="cc91e-193">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc91e-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="cc91e-194">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc91e-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc91e-195"><dt>Poclass. h; </dt> <dt>BatClass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="cc91e-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc91e-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc91e-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc91e-197">Información de la batería</span><span class="sxs-lookup"><span data-stu-id="cc91e-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="cc91e-198">Códigos de control de administración de energía</span><span class="sxs-lookup"><span data-stu-id="cc91e-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="cc91e-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="cc91e-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="cc91e-200">**\_información de consulta de la batería \_**</span><span class="sxs-lookup"><span data-stu-id="cc91e-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="cc91e-201">**\_escala de informes de batería \_**</span><span class="sxs-lookup"><span data-stu-id="cc91e-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="cc91e-202">**Estado de la \_ consulta de batería ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc91e-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="cc91e-203">**\_etiqueta de \_ consulta ioctl Battery \_**</span><span class="sxs-lookup"><span data-stu-id="cc91e-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="cc91e-204">**\_información del \_ conjunto de baterías de ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="cc91e-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

