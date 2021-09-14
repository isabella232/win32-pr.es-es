---
description: La función DestroyProtocol destruye el protocolo que crea la función CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Función DestroyProtocol (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260460"
---
# <a name="destroyprotocol-function"></a>Función DestroyProtocol

La **función DestroyProtocol** destruye el protocolo que crea la función **CreateProtocol.**

## <a name="syntax"></a>Sintaxis


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ En\]
</dt> <dd>

Controle el protocolo que se va a destruir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

El archivo DLL del analizador llama a **la función DestroyProtocol** durante su implementación de [DllMain](dllmain-parser.md). **Se llama a DestroyProtocol** cuando el sistema operativo va a descargar el archivo DLL.



| Para obtener información acerca de                                        | Vea                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                  |
| Cómo implementar **DllMain incluye** un ejemplo.         | [Implementación de DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




