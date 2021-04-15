---
description: La función PdhVbOpenLog abre el archivo de registro especificado para lectura y escritura. Esta función llama a PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545510"
---
# <a name="pdhvbopenlog-function"></a><span data-ttu-id="09aa6-104">PdhVbOpenLog función)</span><span class="sxs-lookup"><span data-stu-id="09aa6-104">PdhVbOpenLog function</span></span>

<span data-ttu-id="09aa6-105">La función **PdhVbOpenLog** abre el archivo de registro especificado para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="09aa6-105">The **PdhVbOpenLog** function opens the specified log file for reading and writing.</span></span> <span data-ttu-id="09aa6-106">Esta función llama a [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span><span class="sxs-lookup"><span data-stu-id="09aa6-106">This function calls [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09aa6-107">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="09aa6-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="09aa6-108">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="09aa6-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="09aa6-109">La función PdhVbOpenLog ( \_ ByVal SzLogFileName as LPCTSTR, \_ ByVal DWACCESSFLAGS as DWORD, \_ BYVAL lpdwLogType as LPDWORD, \_ ByVal hQuery como PDH \_ HQUERY, \_ ByVal DwMaxSize como DWORD, \_ ByVal SZUSERCAPTION como LPCSTR, \_ ByRef phLog como PDH \_ HLOG \_ ) como DWORD</span><span class="sxs-lookup"><span data-stu-id="09aa6-109">Function PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH\_HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH\_HLOG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="09aa6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09aa6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09aa6-111">*szLogFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-111">*szLogFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-112">Puntero a una cadena que especifica el nombre del archivo de registro que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="09aa6-112">Pointer to a string that specifies the name of the log file to be opened.</span></span>

<span data-ttu-id="09aa6-113">Si el archivo de registro contiene datos de SQL, el formato del nombre del archivo de registro es **SQL:**_DataSourceName_*_!_* _NombreDeArchivoDeRegistro_.</span><span class="sxs-lookup"><span data-stu-id="09aa6-113">If the log file contains SQL data, the format of the name of the log file is **SQL:**_DataSourceName_*_!_*_LogFileName_.</span></span> <span data-ttu-id="09aa6-114">En este caso, el valor del parámetro *lpdwLogType* es el tipo de registro de PDH \_ \_ \_ SQL.</span><span class="sxs-lookup"><span data-stu-id="09aa6-114">In this case, the value of the *lpdwLogType* parameter is PDH\_LOG\_TYPE\_SQL.</span></span>

</dd> <dt>

<span data-ttu-id="09aa6-115">*dwAccessFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-115">*dwAccessFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-116">Tipo de acceso que se especificará cuando se abra el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="09aa6-116">Type of access to be specified when the log file is opened.</span></span> <span data-ttu-id="09aa6-117">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="09aa6-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="09aa6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="09aa6-118">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="09aa6-119">Significado</span><span class="sxs-lookup"><span data-stu-id="09aa6-119">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <span data-ttu-id="09aa6-120"><dt>**\_acceso de \_ lectura del registro de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-120"><dt>**PDH\_LOG\_READ\_ACCESS**</dt></span></span> </dl>       | <span data-ttu-id="09aa6-121">Se abre un archivo de registro para una operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="09aa6-121">A log file is opened for a read operation.</span></span><br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <span data-ttu-id="09aa6-122"><dt>**\_acceso de \_ escritura de registro de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-122"><dt>**PDH\_LOG\_WRITE\_ACCESS**</dt></span></span> </dl>    | <span data-ttu-id="09aa6-123">Se abre un nuevo archivo de registro para una operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="09aa6-123">A new log file is opened for a write operation.</span></span><br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <span data-ttu-id="09aa6-124"><dt>**\_acceso de \_ actualización de registros de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-124"><dt>**PDH\_LOG\_UPDATE\_ACCESS**</dt></span></span> </dl> | <span data-ttu-id="09aa6-125">Se abre un archivo de registro existente para una operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="09aa6-125">An existing log file is opened for a write operation.</span></span><br/> |



 

<span data-ttu-id="09aa6-126">El valor seleccionado en la tabla anterior se puede combinar mediante el operador OR con una de las siguientes marcas de acceso Create.</span><span class="sxs-lookup"><span data-stu-id="09aa6-126">The value selected from the previous table can be combined using the OR operator with one of the following create access flags.</span></span>



| <span data-ttu-id="09aa6-127">Value</span><span class="sxs-lookup"><span data-stu-id="09aa6-127">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="09aa6-128">Significado</span><span class="sxs-lookup"><span data-stu-id="09aa6-128">Meaning</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <span data-ttu-id="09aa6-129"><dt>**\_ \_ crear nuevo registro \_ de PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-129"><dt>**PDH\_LOG\_CREATE\_NEW**</dt></span></span> </dl>          | <span data-ttu-id="09aa6-130">Se crea un nuevo archivo de registro con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-130">A new log file with the specified name is created.</span></span><br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <span data-ttu-id="09aa6-131"><dt>**\_ \_ crear siempre Registro \_ de PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-131"><dt>**PDH\_LOG\_CREATE\_ALWAYS**</dt></span></span> </dl> | <span data-ttu-id="09aa6-132">Se crea un nuevo archivo de registro con el nombre especificado y se borra cualquier archivo de registro existente con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="09aa6-132">A new log file with the specified name is created and any existing log file with the same name is erased.</span></span><br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <span data-ttu-id="09aa6-133"><dt>**registro de PDH \_ \_ abierto \_ existente**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-133"><dt>**PDH\_LOG\_OPEN\_EXISTING**</dt></span></span> </dl> | <span data-ttu-id="09aa6-134">Se abre un archivo de registro existente con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-134">An existing log file with the specified name is opened.</span></span> <span data-ttu-id="09aa6-135">Si no existe un archivo de registro con el nombre especificado, es igual al registro de \_ PDH \_ crear \_ nuevo.</span><span class="sxs-lookup"><span data-stu-id="09aa6-135">If a log file with the specified name does not exist, this is equal to PDH\_LOG\_CREATE\_NEW.</span></span><br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <span data-ttu-id="09aa6-136"><dt>**\_ \_ abrir siempre Registro \_ de PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-136"><dt>**PDH\_LOG\_OPEN\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="09aa6-137">Se abre un archivo de registro existente con el nombre especificado o se crea un nuevo archivo de registro con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-137">An existing log file with the specified name is opened or a new log file with the specified name is created.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="09aa6-138">*lpdwLogType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-138">*lpdwLogType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-139">Puntero a una variable que indica el tipo de archivo de registro que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="09aa6-139">Pointer to a variable that indicates the type of log file to be opened.</span></span> <span data-ttu-id="09aa6-140">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="09aa6-140">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="09aa6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="09aa6-141">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="09aa6-142">Significado</span><span class="sxs-lookup"><span data-stu-id="09aa6-142">Meaning</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <span data-ttu-id="09aa6-143"><dt>**tipo de registro de PDH sin \_ \_ \_ definir**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-143"><dt>**PDH\_LOG\_TYPE\_UNDEFINED**</dt></span></span> </dl> | <span data-ttu-id="09aa6-144">Formato de archivo de registro sin definir.</span><span class="sxs-lookup"><span data-stu-id="09aa6-144">Undefined log file format.</span></span><br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <span data-ttu-id="09aa6-145"><dt>**tipo de registro de PDH \_ \_ \_ CSV**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-145"><dt>**PDH\_LOG\_TYPE\_CSV**</dt></span></span> </dl>                   | <span data-ttu-id="09aa6-146">Archivos de texto que contienen encabezados de columna en la primera línea y muestras de datos individuales en cada línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="09aa6-146">Text files containing column headers in the first line, and individual data samples in each subsequent line.</span></span><br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <span data-ttu-id="09aa6-147"><dt>**tipo de registro de PDH \_ \_ \_ SQL**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-147"><dt>**PDH\_LOG\_TYPE\_SQL**</dt></span></span> </dl>                   | <span data-ttu-id="09aa6-148">Los datos del archivo de registro se encuentra en SQL.</span><span class="sxs-lookup"><span data-stu-id="09aa6-148">The data in the log file is in SQL.</span></span><br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <span data-ttu-id="09aa6-149"><dt>**tipo de registro de PDH \_ \_ \_ TSV**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-149"><dt>**PDH\_LOG\_TYPE\_TSV**</dt></span></span> </dl>                   | <span data-ttu-id="09aa6-150">Igual que el registro de PDH, \_ \_ Escriba \_ CSV.</span><span class="sxs-lookup"><span data-stu-id="09aa6-150">Same as PDH\_LOG\_TYPE\_CSV.</span></span><br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <span data-ttu-id="09aa6-151"><dt>**tipo de registro de PDH \_ \_ \_ binario**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-151"><dt>**PDH\_LOG\_TYPE\_BINARY**</dt></span></span> </dl>          | <span data-ttu-id="09aa6-152">Formato de archivo de registro binario.</span><span class="sxs-lookup"><span data-stu-id="09aa6-152">Binary log file format.</span></span> <span data-ttu-id="09aa6-153">Incluye archivos de registro circulares.</span><span class="sxs-lookup"><span data-stu-id="09aa6-153">Includes circular log files.</span></span><br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <span data-ttu-id="09aa6-154"><dt>**tipo de registro de PDH \_ \_ \_ Perfmon**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-154"><dt>**PDH\_LOG\_TYPE\_PERFMON**</dt></span></span> </dl>       | <span data-ttu-id="09aa6-155">Formato de archivo de registro de Perfmon.</span><span class="sxs-lookup"><span data-stu-id="09aa6-155">Perfmon log file format.</span></span><br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="09aa6-156">*hQuery* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-156">*hQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-157">Identificador de consulta.</span><span class="sxs-lookup"><span data-stu-id="09aa6-157">Query handle.</span></span> <span data-ttu-id="09aa6-158">La función [**PdhVbOpenQuery**](pdhvbopenquery.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="09aa6-158">This handle is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

<span data-ttu-id="09aa6-159">Este parámetro puede ser **null** si el archivo de registro se va a abrir para lectura.</span><span class="sxs-lookup"><span data-stu-id="09aa6-159">This parameter can be **NULL** if the log file is to be opened for reading.</span></span>

</dd> <dt>

<span data-ttu-id="09aa6-160">*dwMaxSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-160">*dwMaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-161">Tamaño máximo del archivo de registro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="09aa6-161">Maximum size of the log file, in bytes.</span></span> <span data-ttu-id="09aa6-162">Este valor solo se utiliza si el archivo de registro es un archivo de registro circular o de tamaño limitado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-162">This value is used only if the log file is a limited-size or circular log file.</span></span>

</dd> <dt>

<span data-ttu-id="09aa6-163">*szUserCaption* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-163">*szUserCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-164">Puntero a una cadena que especifica el título definido por el usuario del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="09aa6-164">Pointer to a string that specifies the user-defined caption of the log file.</span></span> <span data-ttu-id="09aa6-165">Un título de archivo de registro suele describir el contenido del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="09aa6-165">A log file caption generally describes the contents of the log file.</span></span> <span data-ttu-id="09aa6-166">Cuando se abre un archivo de registro existente, se omite el valor de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="09aa6-166">When an existing log file is opened, the value of this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="09aa6-167">*phLog* \[ en, Ref\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-167">*phLog* \[in, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="09aa6-168">Puntero a un búfer que recibe un identificador para el archivo de registro abierto.</span><span class="sxs-lookup"><span data-stu-id="09aa6-168">Pointer to a buffer that receives a handle to the opened log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09aa6-169">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09aa6-169">Return value</span></span>

<span data-ttu-id="09aa6-170">Si la función se ejecuta correctamente, devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="09aa6-170">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="09aa6-171">Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="09aa6-171">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="09aa6-172">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="09aa6-172">The following are possible values.</span></span>



| <span data-ttu-id="09aa6-173">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="09aa6-173">Return code</span></span>                                                                                                | <span data-ttu-id="09aa6-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="09aa6-174">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09aa6-175"><dt>**\_búfer insuficiente de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-175"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="09aa6-176">Los datos solicitados son mayores que el búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-176">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="09aa6-177">No se pueden devolver los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="09aa6-177">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="09aa6-178"><dt>**PDH \_ argumento no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-178"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="09aa6-179">Uno o varios de los búferes de cadena no tienen el tamaño correcto.</span><span class="sxs-lookup"><span data-stu-id="09aa6-179">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="09aa6-180"><dt>**\_identificador no válido de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-180"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="09aa6-181">El identificador no es un objeto PDH válido.</span><span class="sxs-lookup"><span data-stu-id="09aa6-181">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="09aa6-182"><dt>**\_ \_ \_ error al abrir el archivo de registro de PDH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-182"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="09aa6-183">No se puede abrir el archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-183">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="09aa6-184"><dt>**\_ \_ no \_ se encontró el archivo PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-184"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="09aa6-185">No se puede encontrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="09aa6-185">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="09aa6-186">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09aa6-186">Remarks</span></span>

<span data-ttu-id="09aa6-187">Al usar esta función para escribir datos de rendimiento en un archivo de registro, primero se debe abrir una consulta mediante [**PdhVbOpenQuery**](pdhvbopenquery.md).</span><span class="sxs-lookup"><span data-stu-id="09aa6-187">When using this function to write performance data to a log file, a query must first be opened using [**PdhVbOpenQuery**](pdhvbopenquery.md).</span></span>

<span data-ttu-id="09aa6-188">Debe haber una consulta abierta actualmente y deben agregarse los contadores deseados, antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="09aa6-188">There must be a currently opened query, and the desired counters must be added to it, before this function is called.</span></span>

<span data-ttu-id="09aa6-189">Tenga en cuenta que los archivos de registro con el formato Perfmon solo se pueden abrir para lectura.</span><span class="sxs-lookup"><span data-stu-id="09aa6-189">Note that log files in the Perfmon format can only be opened for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="09aa6-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09aa6-190">Requirements</span></span>



| <span data-ttu-id="09aa6-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="09aa6-191">Requirement</span></span> | <span data-ttu-id="09aa6-192">Value</span><span class="sxs-lookup"><span data-stu-id="09aa6-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09aa6-193">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09aa6-193">Minimum supported client</span></span><br/> | <span data-ttu-id="09aa6-194">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-194">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09aa6-195">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09aa6-195">Minimum supported server</span></span><br/> | <span data-ttu-id="09aa6-196">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="09aa6-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09aa6-197">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09aa6-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="09aa6-198"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-198"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="09aa6-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09aa6-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09aa6-200"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09aa6-200"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09aa6-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="09aa6-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09aa6-202">**PdhOpenLog**</span><span class="sxs-lookup"><span data-stu-id="09aa6-202">**PdhOpenLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[<span data-ttu-id="09aa6-203">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="09aa6-203">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="09aa6-204">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="09aa6-204">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

