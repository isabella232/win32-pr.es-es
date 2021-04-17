---
description: La función GetEnabledProtocols devuelve una tabla de todos los protocolos que están marcados como habilitados.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Función GetEnabledProtocols (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652367"
---
# <a name="getenabledprotocols-function"></a>GetEnabledProtocols función)

La función **GetEnabledProtocols** devuelve una tabla de todos los protocolos que están marcados como habilitados.

## <a name="syntax"></a>Sintaxis


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ de\]
</dt> <dd>

Identificador de la captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a una estructura [PROTOCOLTABLE](protocoltable.md) que enumera todos los protocolos habilitados en la captura.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetEnabledProtocols** .

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

[PROTOCOLTABLE](protocoltable.md)
</dt> </dl>

 

 




