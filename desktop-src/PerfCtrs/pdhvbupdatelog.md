---
description: La función PdhVbUpdateLog actualiza la consulta actual y escribe nuevos datos en el archivo de registro. Esta función llama a PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Función PdhVbUpdateLog
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
ms.openlocfilehash: c7bf8af71d3a0f5cd20a84ef0f1532806e3d3e8d268bd2d322d617534b533cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033615"
---
# <a name="pdhvbupdatelog-function"></a>Función PdhVbUpdateLog

La **función PdhVbUpdateLog** actualiza la consulta actual y escribe nuevos datos en el archivo de registro. Esta función llama [**a PdhUpdateLog.**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Function PdhVbUpdateLog( \_ ByVal hLog As PDH \_ HLOG, \_ ByVal szUserString As LPCTSTR \_ )

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hLog* \[ En\]
</dt> <dd>

Identificador del archivo de registro que se va a actualizar. La función [**PdhVbOpenLog**](pdhvbopenlog.md) devuelve este identificador.

</dd> <dt>

*szUserString* \[ En\]
</dt> <dd>

Puntero a una cadena que especifica los datos que se van a agregar al archivo de registro. Por lo general, se usa para los comentarios dentro del archivo de registro.

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

Debe haber una consulta abierta actualmente y los contadores deseados deben agregarse a ella antes de llamar a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

