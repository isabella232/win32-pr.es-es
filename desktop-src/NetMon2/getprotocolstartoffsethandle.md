---
description: La función GetProtocolStartOffsetHandle devuelve el desplazamiento de fotogramas de un protocolo determinado.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Función GetProtocolStartOffsetHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666275"
---
# <a name="getprotocolstartoffsethandle-function"></a>GetProtocolStartOffsetHandle función)

La función **GetProtocolStartOffsetHandle** devuelve el desplazamiento de fotogramas de un protocolo determinado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador de un marco.

</dd> <dt>

*hProtocol* \[ de\]
</dt> <dd>

Identificador de un protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es el desplazamiento del marco medido en bytes.

Si la función no es correcta, el valor devuelto es uno (1).

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetProtocolStartOffsetHandle** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




