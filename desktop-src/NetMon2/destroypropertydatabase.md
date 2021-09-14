---
description: La función DestroyPropertyDatabase libera los recursos usados para crear la base de datos de propiedades de protocolo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Función DestroyPropertyDatabase (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260468"
---
# <a name="destroypropertydatabase-function"></a>Función DestroyPropertyDatabase

La **función DestroyPropertyDatabase** libera los recursos usados para crear la base de datos de [*propiedades de protocolo*](p.md).

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ En\]
</dt> <dd>

Identificador de la base de datos de propiedades que se va a destruir. El identificador se pasa al archivo DLL del analizador cuando Monitor de red llama a la [función Deregister.](deregister.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                              | Descripción                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**ERROR INTERNO \_ DE NMERR \_**</dt> </dl>    | Se ha producido un error interno. <br/>    |
| <dl> <dt>**NMERR \_ INVALID \_ HPROTOCOL**</dt> </dl> | Identificador no válido *en hProtocol.* <br/> |



 

## <a name="remarks"></a>Observaciones

Solo se debe llamar a la función **DestroyPropertyDatabase** al implementar la función de exportación [Deregister](deregister.md) para el protocolo. En el caso de los archivos DLL del analizador que admiten varios protocolos, se llama a la función **DestroyPropertyDatabase** para cada implementación **de Deregister**.



| Para obtener información acerca de                                        | Vea                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                 |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura dll del analizador](parser-dll-architecture.md) |
| Cómo implementar **Deregister incluye**  un ejemplo.     | [Implementación de Anulación del registro](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eliminar registro](deregister.md)
</dt> </dl>

 

 




