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
# <a name="pdhvbopenlog-function"></a>PdhVbOpenLog función)

La función **PdhVbOpenLog** abre el archivo de registro especificado para lectura y escritura. Esta función llama a [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga).

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

La función PdhVbOpenLog ( \_ ByVal SzLogFileName as LPCTSTR, \_ ByVal DWACCESSFLAGS as DWORD, \_ BYVAL lpdwLogType as LPDWORD, \_ ByVal hQuery como PDH \_ HQUERY, \_ ByVal DwMaxSize como DWORD, \_ ByVal SZUSERCAPTION como LPCSTR, \_ ByRef phLog como PDH \_ HLOG \_ ) como DWORD

## <a name="parameters"></a>Parámetros

<dl> <dt>

*szLogFileName* \[ de\]
</dt> <dd>

Puntero a una cadena que especifica el nombre del archivo de registro que se va a abrir.

Si el archivo de registro contiene datos de SQL, el formato del nombre del archivo de registro es **SQL:**_DataSourceName_*_!_* _NombreDeArchivoDeRegistro_. En este caso, el valor del parámetro *lpdwLogType* es el tipo de registro de PDH \_ \_ \_ SQL.

</dd> <dt>

*dwAccessFlags* \[ de\]
</dt> <dd>

Tipo de acceso que se especificará cuando se abra el archivo de registro. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                   | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**\_acceso de \_ lectura del registro de PDH \_**</dt> </dl>       | Se abre un archivo de registro para una operación de lectura.<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**\_acceso de \_ escritura de registro de PDH \_**</dt> </dl>    | Se abre un nuevo archivo de registro para una operación de escritura.<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**\_acceso de \_ actualización de registros de PDH \_**</dt> </dl> | Se abre un archivo de registro existente para una operación de escritura.<br/> |



 

El valor seleccionado en la tabla anterior se puede combinar mediante el operador OR con una de las siguientes marcas de acceso Create.



| Value                                                                                                                                                                                   | Significado                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**\_ \_ crear nuevo registro \_ de PDH**</dt> </dl>          | Se crea un nuevo archivo de registro con el nombre especificado.<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**\_ \_ crear siempre Registro \_ de PDH**</dt> </dl> | Se crea un nuevo archivo de registro con el nombre especificado y se borra cualquier archivo de registro existente con el mismo nombre.<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**registro de PDH \_ \_ abierto \_ existente**</dt> </dl> | Se abre un archivo de registro existente con el nombre especificado. Si no existe un archivo de registro con el nombre especificado, es igual al registro de \_ PDH \_ crear \_ nuevo.<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**\_ \_ abrir siempre Registro \_ de PDH**</dt> </dl>       | Se abre un archivo de registro existente con el nombre especificado o se crea un nuevo archivo de registro con el nombre especificado.<br/>                                          |



 

</dd> <dt>

*lpdwLogType* \[ de\]
</dt> <dd>

Puntero a una variable que indica el tipo de archivo de registro que se va a abrir. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                      | Significado                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**tipo de registro de PDH sin \_ \_ \_ definir**</dt> </dl> | Formato de archivo de registro sin definir.<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**tipo de registro de PDH \_ \_ \_ CSV**</dt> </dl>                   | Archivos de texto que contienen encabezados de columna en la primera línea y muestras de datos individuales en cada línea siguiente.<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**tipo de registro de PDH \_ \_ \_ SQL**</dt> </dl>                   | Los datos del archivo de registro se encuentra en SQL.<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**tipo de registro de PDH \_ \_ \_ TSV**</dt> </dl>                   | Igual que el registro de PDH, \_ \_ Escriba \_ CSV.<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**tipo de registro de PDH \_ \_ \_ binario**</dt> </dl>          | Formato de archivo de registro binario. Incluye archivos de registro circulares.<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**tipo de registro de PDH \_ \_ \_ Perfmon**</dt> </dl>       | Formato de archivo de registro de Perfmon.<br/>                                                                                     |



 

</dd> <dt>

*hQuery* \[ de\]
</dt> <dd>

Identificador de consulta. La función [**PdhVbOpenQuery**](pdhvbopenquery.md) devuelve este identificador.

Este parámetro puede ser **null** si el archivo de registro se va a abrir para lectura.

</dd> <dt>

*dwMaxSize* \[ de\]
</dt> <dd>

Tamaño máximo del archivo de registro, en bytes. Este valor solo se utiliza si el archivo de registro es un archivo de registro circular o de tamaño limitado.

</dd> <dt>

*szUserCaption* \[ de\]
</dt> <dd>

Puntero a una cadena que especifica el título definido por el usuario del archivo de registro. Un título de archivo de registro suele describir el contenido del archivo de registro. Cuando se abre un archivo de registro existente, se omite el valor de este parámetro.

</dd> <dt>

*phLog* \[ en, Ref\]
</dt> <dd>

Puntero a un búfer que recibe un identificador para el archivo de registro abierto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve 0.

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md). Los valores posibles son los siguientes.



| Código devuelto                                                                                                | Descripción                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_búfer insuficiente de PDH \_**</dt> </dl>   | Los datos solicitados son mayores que el búfer proporcionado. No se pueden devolver los datos solicitados.<br/> |
| <dl> <dt>**PDH \_ argumento no válido \_**</dt> </dl>      | Uno o varios de los búferes de cadena no tienen el tamaño correcto.<br/>                                  |
| <dl> <dt>**\_identificador no válido de PDH \_**</dt> </dl>        | El identificador no es un objeto PDH válido.<br/>                                                       |
| <dl> <dt>**\_ \_ \_ error al abrir el archivo de registro de PDH \_**</dt> </dl> | No se puede abrir el archivo de registro especificado.<br/>                                                      |
| <dl> <dt>**\_ \_ no \_ se encontró el archivo PDH**</dt> </dl>       | No se puede encontrar el archivo especificado.<br/>                                                          |



 

## <a name="remarks"></a>Observaciones

Al usar esta función para escribir datos de rendimiento en un archivo de registro, primero se debe abrir una consulta mediante [**PdhVbOpenQuery**](pdhvbopenquery.md).

Debe haber una consulta abierta actualmente y deben agregarse los contadores deseados, antes de llamar a esta función.

Tenga en cuenta que los archivos de registro con el formato Perfmon solo se pueden abrir para lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

