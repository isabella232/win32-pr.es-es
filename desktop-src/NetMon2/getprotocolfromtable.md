---
description: La función GetProtocolFromTable devuelve un identificador a un protocolo&8212; basado en una tabla y un valor de entrega \# determinados.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Función GetProtocolFromTable (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171442"
---
# <a name="getprotocolfromtable-function"></a>Función GetProtocolFromTable

La **función GetProtocolFromTable** devuelve un identificador a un protocolo basado en una tabla y un valor de entrega determinados.

## <a name="syntax"></a>Sintaxis


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hTable* \[ En\]
</dt> <dd>

Identificador de una tabla de entrega.

</dd> <dt>

*ItemToFind* \[ En\]
</dt> <dd>

Valor utilizado para buscar el protocolo en una tabla de entrega. El valor debe estar disponible en los datos del protocolo.

</dd> <dt>

*lpInstData* \[ out\]
</dt> <dd>

Si está disponible en la tabla de entrega, los datos de instancia para el protocolo siguiente. Los datos de instancia no pueden tener una longitud superior a \_ DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un identificador de protocolo.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

Al implementar la [función de exportación RecognizeFrame,](recognizeframe.md) la función **GetProtocolFromTable** se usa para obtener un identificador para el protocolo siguiente. Se **llama a la función GetProtocolFromTable** para recuperar un identificador del protocolo siguiente si el protocolo identifica qué protocolo sigue.

**Datos de instancia**

Los datos de instancia pueden ser datos menores o iguales que un PTR DWORD de longitud, o un puntero a datos, como datos de fotogramas sin procesar, que el analizador no necesita asignar o \_ liberar.

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

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




