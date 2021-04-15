---
description: Lo utiliza un proveedor de servicios criptográficos (CSP) para obtener el identificador de ventana que el CSP debe utilizar como elemento primario o propietario de cualquier interfaz de usuario que se muestre.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND puntero a función (Cspdk. h)
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
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669667"
---
# <a name="crypt_return_hwnd-function-pointer"></a>CRYPT \_ Return ( \_ puntero de función HWND)

Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utiliza la función de devolución de llamada **FuncReturnhWnd** para obtener el identificador de ventana que el CSP debe usar como elemento primario o propietario de cualquier interfaz de usuario que se muestra.

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

Dirección de una variable **hWnd** que recibe el identificador de la ventana primaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este puntero de función no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
