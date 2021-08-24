---
description: La función PdhVbGetLogFileSize devuelve el tamaño del archivo de registro especificado. Esta función llama a PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Función PdhVbGetLogFileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: cd3925eee621ac205615f17b26767096151d459628ca7d331a7aaee3336b27ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674795"
---
# <a name="pdhvbgetlogfilesize-function"></a>Función PdhVbGetLogFileSize

La **función PdhVbGetLogFileSize** devuelve el tamaño del archivo de registro especificado. Esta función llama [**a PdhGetLogFileSize.**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetLogFileSize( \_ ByVal hLog As PDH \_ HLOG, \_ ByRef llSize As LONG \_ ) As DWORD

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hLog* \[ En\]
</dt> <dd>

Identificador del archivo de registro. La función [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) devuelve este identificador.

</dd> <dt>

*llSize* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del archivo de registro, en bytes.

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

