---
description: La función DestroyPropertyDatabase libera los recursos usados para crear la base de datos de propiedades de protocolo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Función DestroyPropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002853"
---
# <a name="destroypropertydatabase-function"></a>DestroyPropertyDatabase función)

La función **DestroyPropertyDatabase** libera los recursos usados para crear la [*base de datos de propiedades*](p.md)de protocolo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ de\]
</dt> <dd>

Identificador de la base de datos de propiedades que se va a destruir. El identificador se pasa a la DLL del analizador cuando Monitor de red llama a la función de [anulación del registro](deregister.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un código de error.



| Código devuelto                                                                                              | Descripción                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_error interno de NMERR \_**</dt> </dl>    | Se ha producido un error interno. <br/>    |
| <dl> <dt>**NMERR \_ no válido \_ HPROTOCOL**</dt> </dl> | Identificador no válido en *hProtocol*. <br/> |



 

## <a name="remarks"></a>Observaciones

Solo se debe llamar a la función **DestroyPropertyDatabase** cuando se implementa la función de exportación de [anulación del registro](deregister.md) para el protocolo. En el caso de los archivos dll de analizador que admiten varios protocolos, se llama a la función **DestroyPropertyDatabase** para cada implementación de **unregister**.



| Para obtener información acerca de                                        | Vea                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                 |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura de DLL de analizador](parser-dll-architecture.md) |
| Cómo implementar **unregister**  incluye un ejemplo.     | [Implementación de unregister](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eliminar registro](deregister.md)
</dt> </dl>

 

 




