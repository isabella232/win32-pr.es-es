---
description: Nota En lugar de usar esta función heredada, se recomienda usar la API D3DDisassemble. Esta función , que desensambla un efecto compilado en una cadena de texto que contiene instrucciones de ensamblado y registra asignaciones, ha quedado en desuso.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Función D3DX10DisassembleEffect (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 282dcbb91013e5e8bf6def540809fa3afdb3bca40e2a2fd5250c5b3c92877af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753285"
---
# <a name="d3dx10disassembleeffect-function"></a>Función D3DX10DisassembleEffect

> [!Note]  
> En lugar de usar esta función heredada, se recomienda usar la API [**D3DDisassemble.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble)

 

Esta función , que desensambla un efecto compilado en una cadena de texto que contiene instrucciones de ensamblado y registra asignaciones, ha quedado en desuso. En su lugar, [**use D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEffect* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

Puntero a la interfaz de efecto (vea [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).

</dd> <dt>

*EnableColorCode* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Incluya etiquetas HTML en la salida para colorear el resultado.

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un búfer (vea [**Interfaz ID3D10Blob)**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene el efecto desensamblado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
