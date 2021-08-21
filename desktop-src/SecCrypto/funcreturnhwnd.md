---
description: Lo usa un proveedor de servicios criptográficos (CSP) para obtener el identificador de ventana que el CSP debe usar como primario o propietario de cualquier interfaz de usuario que se muestre.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND puntero de función (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 387e1e9140dac8081acf851eb7125a612506783adbeefe1174137ff7f74fae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006753"
---
# <a name="crypt_return_hwnd-function-pointer"></a>Puntero de \_ función CRYPT RETURN \_ HWND

Un proveedor de servicios criptográficos (CSP) [](../secgloss/c-gly.md) usa la función de devolución de llamada **FuncReturnhWnd** para obtener el identificador de ventana que debe usar el CSP como el primario o el propietario de cualquier interfaz de usuario que se muestre.

## <a name="syntax"></a>Sintaxis


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phWnd* \[ in, out\]
</dt> <dd>

Dirección de una variable **HWND** que recibe el identificador de ventana principal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este puntero de función no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
