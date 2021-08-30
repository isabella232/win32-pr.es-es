---
description: La función PdhVbOpenLog abre el archivo de registro especificado para lectura y escritura. Esta función llama a PdhOpenLog.
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: Función PdhVbOpenLog
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
ms.openlocfilehash: 82c0c9e225e1efac86eac4f0e10df0ebab2f580dbb1fe484c81a4a6f97b37cdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033645"
---
# <a name="pdhvbopenlog-function"></a>Función PdhVbOpenLog

La **función PdhVbOpenLog** abre el archivo de registro especificado para lectura y escritura. Esta función llama a [**PdhOpenLog.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbOpenLog( \_ ByVal szLogFileName As LPCTSTR, \_ ByVal dwAccessFlags As DWORD, \_ ByVal lpdwLogType As LPDWORD, \_ ByVal hQuery As PDH \_ HQUERY, \_ ByVal dwMaxSize As DWORD, \_ ByVal szUserCaption As LPCSTR, \_ ByRef phLog As PDH \_ HLOG \_ ) As DWORD

## <a name="parameters"></a>Parámetros

<dl> <dt>

*szLogFileName* \[ En\]
</dt> <dd>

Puntero a una cadena que especifica el nombre del archivo de registro que se va a abrir.

Si el archivo de registro contiene SQL datos, el formato del nombre del archivo de registro **es SQL:**_DataSourceName_*_!_* _LogFileName_. En este caso, el valor del parámetro *lpdwLogType* es PDH \_ LOG TYPE \_ \_ SQL.

</dd> <dt>

*dwAccessFlags* \[ En\]
</dt> <dd>

Tipo de acceso que se va a especificar cuando se abra el archivo de registro. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                   | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**PDH \_ LOG \_ READ \_ ACCESS**</dt> </dl>       | Se abre un archivo de registro para una operación de lectura.<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**ACCESO DE ESCRITURA \_ DE REGISTROS \_ DE PDH \_**</dt> </dl>    | Se abre un nuevo archivo de registro para una operación de escritura.<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**PDH \_ LOG \_ UPDATE \_ ACCESS**</dt> </dl> | Se abre un archivo de registro existente para una operación de escritura.<br/> |



 

El valor seleccionado de la tabla anterior se puede combinar mediante el operador OR con una de las siguientes marcas de acceso de creación.



| Value                                                                                                                                                                                   | Significado                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**PDH \_ LOG \_ CREATE \_ NEW**</dt> </dl>          | Se crea un nuevo archivo de registro con el nombre especificado.<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**PDH \_ LOG \_ CREATE \_ ALWAYS**</dt> </dl> | Se crea un nuevo archivo de registro con el nombre especificado y se borra cualquier archivo de registro existente con el mismo nombre.<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**PDH \_ LOG \_ OPEN \_ EXISTING**</dt> </dl> | Se abre un archivo de registro existente con el nombre especificado. Si no existe un archivo de registro con el nombre especificado, es igual a PDH \_ LOG \_ CREATE \_ NEW.<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**PDH \_ LOG \_ OPEN \_ ALWAYS**</dt> </dl>       | Se abre un archivo de registro existente con el nombre especificado o se crea un nuevo archivo de registro con el nombre especificado.<br/>                                          |



 

</dd> <dt>

*lpdwLogType* \[ En\]
</dt> <dd>

Puntero a una variable que indica el tipo de archivo de registro que se va a abrir. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                      | Significado                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**PDH \_ LOG \_ TYPE \_ UNDEFINED**</dt> </dl> | Formato de archivo de registro indefinido.<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**PDH \_ LOG \_ TYPE \_ CSV**</dt> </dl>                   | Archivos de texto que contienen encabezados de columna en la primera línea y ejemplos de datos individuales en cada línea posterior.<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**Tipo de \_ registro \_ PDH \_ SQL**</dt> </dl>                   | Los datos del archivo de registro están en SQL.<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**PDH \_ LOG \_ TYPE \_ TSV**</dt> </dl>                   | Igual que PDH \_ LOG \_ TYPE \_ CSV.<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**PDH \_ LOG \_ TYPE \_ BINARY**</dt> </dl>          | Formato de archivo de registro binario. Incluye archivos de registro circulares.<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**\_PERFMON DE TIPO DE REGISTRO \_ \_ PDH**</dt> </dl>       | Formato de archivo de registro perfmon.<br/>                                                                                     |



 

</dd> <dt>

*hQuery* \[ En\]
</dt> <dd>

Identificador de consulta. La función [**PdhVbOpenQuery**](pdhvbopenquery.md) devuelve este identificador.

Este parámetro puede ser **NULL si** el archivo de registro se va a abrir para lectura.

</dd> <dt>

*dwMaxSize* \[ En\]
</dt> <dd>

Tamaño máximo del archivo de registro, en bytes. Este valor solo se usa si el archivo de registro es un archivo de registro circular o de tamaño limitado.

</dd> <dt>

*szUserCaption* \[ En\]
</dt> <dd>

Puntero a una cadena que especifica el título definido por el usuario del archivo de registro. Por lo general, un título de archivo de registro describe el contenido del archivo de registro. Cuando se abre un archivo de registro existente, se omite el valor de este parámetro.

</dd> <dt>

*phLog* \[ in, ref\]
</dt> <dd>

Puntero a un búfer que recibe un identificador al archivo de registro abierto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve 0.

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error [PDH](pdh-error-codes.md). A continuación se den los valores posibles.



| Código devuelto                                                                                                | Descripción                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BÚFER INSUFICIENTE DE PDH \_ \_**</dt> </dl>   | Los datos solicitados son mayores que el búfer proporcionado. No se pueden devolver los datos solicitados.<br/> |
| <dl> <dt>**PDH \_ INVALID \_ ARGUMENT**</dt> </dl>      | Uno o varios de los búferes de cadena no tienen el tamaño correcto.<br/>                                  |
| <dl> <dt>**IDENTIFICADOR NO VÁLIDO de PDH \_ \_**</dt> </dl>        | El identificador no es un objeto PDH válido.<br/>                                                       |
| <dl> <dt>**ERROR DE \_ APERTURA DEL ARCHIVO DE REGISTRO \_ \_ PDH \_**</dt> </dl> | No se puede abrir el archivo de registro especificado.<br/>                                                      |
| <dl> <dt>**ARCHIVO PDH \_ \_ NO \_ ENCONTRADO**</dt> </dl>       | No se encuentra el archivo especificado.<br/>                                                          |



 

## <a name="remarks"></a>Comentarios

Cuando se usa esta función para escribir datos de rendimiento en un archivo de registro, primero se debe abrir una consulta [**mediante PdhVbOpenQuery**](pdhvbopenquery.md).

Debe haber una consulta abierta actualmente y los contadores deseados deben agregarse a ella, antes de llamar a esta función.

Tenga en cuenta que los archivos de registro en formato Perfmon solo se pueden abrir para lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

