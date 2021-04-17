---
description: La función PdhVbUpdateLog actualiza la consulta actual y escribe nuevos datos en el archivo de registro. Esta función llama a PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667303"
---
# <a name="pdhvbupdatelog-function"></a>PdhVbUpdateLog función)

La función **PdhVbUpdateLog** actualiza la consulta actual y escribe nuevos datos en el archivo de registro. Esta función llama a [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Function PdhVbUpdateLog ( \_ ByVal HLog as PDH \_ hLog, \_ BYVAL szUserString as LPCTSTR \_ )

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hLog* \[ de\]
</dt> <dd>

Identificador del archivo de registro que se va a actualizar. La función [**PdhVbOpenLog**](pdhvbopenlog.md) devuelve este identificador.

</dd> <dt>

*szUserString* \[ de\]
</dt> <dd>

Puntero a una cadena que especifica los datos que se van a agregar al archivo de registro. Normalmente se utiliza para los comentarios dentro del archivo de registro.

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

Debe haber una consulta abierta actualmente y deben agregarse los contadores deseados antes de llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

