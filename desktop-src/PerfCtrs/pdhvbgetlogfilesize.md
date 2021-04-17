---
description: La función PdhVbGetLogFileSize devuelve el tamaño del archivo de registro especificado. Esta función llama a PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize función)
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
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667309"
---
# <a name="pdhvbgetlogfilesize-function"></a>PdhVbGetLogFileSize función)

La función **PdhVbGetLogFileSize** devuelve el tamaño del archivo de registro especificado. Esta función llama a [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Function PdhVbGetLogFileSize ( \_ ByVal HLog as PDH \_ hLog, \_ BYREF llSize as Long \_ ) as DWORD

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hLog* \[ de\]
</dt> <dd>

Identificador del archivo de registro. La función [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) devuelve este identificador.

</dd> <dt>

*llSize* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del archivo de registro, en bytes.

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

