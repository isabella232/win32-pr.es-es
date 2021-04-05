---
description: La función GetProtocolInfo devuelve un puntero a un valor de información de protocolo.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Función GetProtocolInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000922"
---
# <a name="getprotocolinfo-function"></a>GetProtocolInfo función)

La función **GetProtocolInfo** devuelve un puntero a un valor de información de protocolo.

## <a name="syntax"></a>Sintaxis


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ de\]
</dt> <dd>

Identificador de un protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al valor de información del protocolo.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetProtocolInfo** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




