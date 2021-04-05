---
description: La función GetProtocolFromTable devuelve un identificador a un protocolo&\# 8212; basándose en una tabla de entrega y un valor determinados.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Función GetProtocolFromTable (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000923"
---
# <a name="getprotocolfromtable-function"></a>GetProtocolFromTable función)

La función **GetProtocolFromTable** devuelve un identificador a un protocolo basado en una tabla de entrega y un valor determinados.

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

*hTable* \[ de\]
</dt> <dd>

Identificador de una tabla de entrega.

</dd> <dt>

*ItemToFind* \[ de\]
</dt> <dd>

Valor usado para buscar el protocolo en una tabla de entrega. El valor debe estar disponible en los datos del protocolo.

</dd> <dt>

*lpInstData* \[ enuncia\]
</dt> <dd>

Si está disponible en la tabla de entrega, datos de instancia para el protocolo siguiente. Los datos de instancia no pueden tener más de una \_ longitud de DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador de protocolo.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Al implementar la función de exportación [RecognizeFrame](recognizeframe.md) , se usa la función **GetProtocolFromTable** para obtener un identificador del protocolo siguiente. Se llama a la función **GetProtocolFromTable** para recuperar un identificador del protocolo siguiente si el protocolo identifica el protocolo que sigue.

**Datos de instancia**

Los datos de instancia pueden ser cualquier dato que sea menor o igual que \_ la longitud de un valor DWORD PTR, o un puntero a los datos, como los datos de fotogramas sin formato, que no es necesario que el analizador asigne o libere.

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

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




