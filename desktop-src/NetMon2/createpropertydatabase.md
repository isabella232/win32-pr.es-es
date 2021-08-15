---
description: La función CreatePropertyDatabase crea una base de datos de propiedades que almacena las propiedades de un protocolo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Función CreatePropertyDatabase (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7c07f6f3e4569c06f0b3890e3ef3a26bca10b3272849fc005dfb3be6cbc2836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367222"
---
# <a name="createpropertydatabase-function"></a>Función CreatePropertyDatabase

La **función CreatePropertyDatabase** crea una base de datos de propiedades que almacena las propiedades de un protocolo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ En\]
</dt> <dd>

Identificador del protocolo asociado a la base de datos. Cuando Monitor de red llama a la [función Register,](register-parser.md) Monitor de red pasa el identificador de protocolo al archivo DLL del analizador.

</dd> <dt>

*nPropiedades* \[ En\]
</dt> <dd>

Número de propiedades almacenadas en la base de datos. Establezca este parámetro en el número de propiedades que admite el protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                             | Descripción                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**ERROR INTERNO DE NMERR \_ \_**</dt> </dl>   | Se ha producido un error interno.<br/>                                     |
| <dl> <dt>**NMERR \_ INVALID \_ HPOTOCOL**</dt> </dl> | El identificador del protocolo especificado en *hProtocol* no es válido.<br/>     |
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl>   | Monitor de red no tiene suficiente memoria para crear la base de datos.<br/> |



 

## <a name="remarks"></a>Comentarios

Solo se debe llamar a la función **CreatePropertyDatabase** al implementar la [función Register.](register-parser.md) El analizador usa **CreatePropertyDatabase para** crear una base de datos de propiedades que describe las propiedades de un protocolo. Monitor de red utiliza la base de datos para interpretar la información dentro del protocolo.

La **función CreatePropertyDatabase** asigna las estructuras que Monitor de red para mantener una base de datos de propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Registro](register-parser.md)
</dt> </dl>

 

 




