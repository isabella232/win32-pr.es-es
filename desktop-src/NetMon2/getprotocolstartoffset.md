---
description: Devuelve el desplazamiento de un protocolo especificado en el marco.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Función GetProtocolStartOffset (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171429"
---
# <a name="getprotocolstartoffset-function"></a>Función GetProtocolStartOffset

La **función GetProtocolStartOffset** devuelve el desplazamiento de un protocolo especificado en el marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* 
</dt> <dd>

Identificador del marco.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nombre del protocolo, como TCP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un desplazamiento **DWORD** al principio del protocolo en el que se busca un valor devuelto de cero indica que el protocolo es el primer protocolo del marco.

Si la función no se realiza correctamente, el protocolo no está en el marco, el valor devuelto es -1.

## <a name="remarks"></a>Observaciones

Cuando se le da el identificador a un marco, esta función devuelve el desplazamiento a un protocolo especificado en el marco. Por ejemplo, para determinar si el marco es un marco DNS, el analizador DNS requiere la dirección de puerto del protocolo TCP. El analizador DNS llamaría a esta función con TCP como el *valor ProtocolName.* Si el protocolo TCP reconoce el marco, se devuelve el desplazamiento **DE WORD** desde el principio del marco hasta el principio del marco TCP. Si no hay ningún protocolo TCP, el valor devuelto es cero.

Esta función busca el principio de un protocolo en un marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




