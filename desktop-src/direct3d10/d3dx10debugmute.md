---
description: Habilitar o deshabilitar los mensajes de depuración.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Función D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718381"
---
# <a name="d3dx10debugmute-function"></a>D3DX10DebugMute función)

Habilitar o deshabilitar los mensajes de depuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Silenciar* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Establézcalo en **true** para habilitar los mensajes de depuración; establézcalo en **false** para deshabilitar los mensajes de depuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Use esta función para deshabilitar los mensajes de error de las API de D3DX10 durante la depuración. el uso de esta función debe protegerse mediante el \_ modificador del compilador de depuración D3D10.


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



El estado predeterminado es **true** para una compilación de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
