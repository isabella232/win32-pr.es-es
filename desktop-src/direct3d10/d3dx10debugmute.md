---
description: Habilite o deshabilite los mensajes de depuración.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Función D3DX10DebugMute (D3DX10Core.h)
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
ms.openlocfilehash: f4cd6a7ade60bc59cb1e6cbd9d3a447fac5cb7364db1ca85dcf704acedaa645c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128387"
---
# <a name="d3dx10debugmute-function"></a>Función D3DX10DebugMute

Habilite o deshabilite los mensajes de depuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Exclusión mutua* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Establezca en **TRUE para** habilitar los mensajes de depuración; establezca en **FALSE para** deshabilitar los mensajes de depuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Use esta función para deshabilitar los mensajes de error de las API D3DX10 durante la depuración. El uso de esta función debe protegerse mediante el modificador del compilador DEBUG D3D10. \_


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



El estado predeterminado es **TRUE para** una compilación de depuración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
