---
title: Estructura de RECORD_HEADER
description: Encabezado de registro usado por la entrada del registro de cambios \_ y las estructuras de encabezado del registro de \_ cambios \_ \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Restaurar sistema de estructura RECORD_HEADER
- PRECORD_HEADER de puntero de estructura para restaurar sistema
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492184"
---
# <a name="record_header-structure"></a>Estructura del encabezado de registro \_

\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]

Encabezado de registro usado por la [**\_ \_ entrada del registro de cambios**](change-log-entry.md) y las estructuras de [**\_ \_ encabezado del registro de cambios**](change-log-header.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwRecordSize**
</dt> <dd>

Tamaño total del registro, incluido el encabezado, en bytes.

</dd> <dt>

**dwRecordType**
</dt> <dd>

Tipo de registro. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**RecordTypeLogHeader**</dt> <dt>0</dt> </dl>     | El registro es el encabezado del registro de cambios.<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**RecordTypeLogEntry**</dt> <dt>1</dt> </dl>         | El registro es el encabezado de una entrada del registro de cambios.<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**RecordTypeVolumePath**</dt> <dt>2</dt> </dl> | Los datos son la ruta de acceso del volumen para la entrada del registro de cambios.<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**RecordTypeFirstPath**</dt> <dt>3</dt> </dl>     | Los datos son la ruta de acceso de archivo para la entrada del registro de cambios.<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**RecordTypeSecondPath**</dt> <dt>4</dt> </dl> | Los datos se utilizan al cambiar el nombre de las entradas del registro de cambios; Esta ruta de acceso es donde se almacena el archivo cuyo nombre ha cambiado.<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**RecordTypeTempPath**</dt> <dt>5</dt> </dl>         | Los datos son el nombre del archivo de copia de seguridad que se usa para restaurar la entrada del registro de cambios. Los archivos de copia de seguridad se encuentran en la carpeta RP *n* . El nombre de archivo tiene el formato siguiente: un *xxxxxxx*. *ext*, donde *xxxxxxx* es un número de siete dígitos y *ext* es la extensión de nombre de archivo.<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**RecordTypeAclInline**</dt> <dt>6</dt> </dl>     | Los datos son una ACL. El formato de los datos es una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . <br/> Este valor no puede ser mayor que 8.192 bytes. Para especificar un valor mayor que 8.192 bytes, utilice el miembro **RecordTypeAclFile** .<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**RecordTypeAclFile**</dt> <dt>7</dt> </dl>             | Los datos son el nombre del archivo ACL utilizado para almacenar la ACL. Los archivos ACL se encuentran en la carpeta RP *n* . El nombre de archivo tiene el formato siguiente: S *xxxxxxx*. ACL, donde *xxxxxxx* es un número de siete dígitos.<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**RecordTypeDebugInfo**</dt> <dt>8</dt> </dl>     | Los datos son información de depuración para la entrada del registro de cambios. El formato de datos es una estructura de **\_ \_ \_ información de depuración de registro de Sr** . Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**RecordTypeShortName**</dt> <dt>9</dt> </dl>     | Los datos son el nombre corto del archivo de copia de seguridad.<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ \_ \_ información de depuración del registro de Sr** se define de la siguiente manera.

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                       |



 

