---
description: La función CreatePropertyDatabase crea una base de datos de propiedades que almacena las propiedades de un protocolo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Función CreatePropertyDatabase (Netmon. h)
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
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677736"
---
# <a name="createpropertydatabase-function"></a>CreatePropertyDatabase función)

La función **CreatePropertyDatabase** crea una base de datos de propiedades que almacena las propiedades de un protocolo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ de\]
</dt> <dd>

Identificador del protocolo asociado a la base de datos. Cuando Monitor de red llama a la función [Register](register-parser.md) , monitor de red pasa el identificador de protocolo a la dll del analizador.

</dd> <dt>

*nProperties* \[ de\]
</dt> <dd>

Número de propiedades almacenadas en la base de datos. Establezca este parámetro en el número de propiedades que admite el protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un código de error.



| Código devuelto                                                                                             | Descripción                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_error interno de NMERR \_**</dt> </dl>   | Se ha producido un error interno.<br/>                                     |
| <dl> <dt>**NMERR \_ no válido \_ HPOTOCOL**</dt> </dl> | El identificador del protocolo especificado en *hProtocol* no es válido.<br/>     |
| <dl> <dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt> </dl>   | Monitor de red no tiene suficiente memoria para crear la base de datos.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo se debe llamar a la función **CreatePropertyDatabase** cuando se implementa la función [Register](register-parser.md) . El analizador usa **CreatePropertyDatabase** para crear una base de datos de propiedades que describe las propiedades de un protocolo. Monitor de red usa la base de datos para interpretar la información incluida en el protocolo.

La función **CreatePropertyDatabase** asigna las estructuras que monitor de red necesita para mantener una base de datos de propiedades.

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

[Registro](register-parser.md)
</dt> </dl>

 

 




