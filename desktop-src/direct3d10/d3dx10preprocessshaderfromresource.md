---
description: Nota En lugar de usar esta función heredada, se recomienda usar la API D3DPreprocess. Cree un sombreador a partir de un recurso sin compilarlo.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: Función D3DX10PreprocessShaderFromResource (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 63546fbf7424189c5b9d398b4c6ddce076d7e02db5900031c15b579048da1965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753165"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a>Función D3DX10PreprocessShaderFromResource

> [!Note]  
> En lugar de usar esta función heredada, se recomienda usar la API [**D3DPreprocess.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess)

 

Cree un sombreador a partir de un recurso sin compilarlo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador del módulo de recursos que contiene el sombreador. HMODULE se puede obtener con la [función GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pResourceName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nombre del recurso en el lado hModule que contiene el sombreador. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*pSrcFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Opcional. Nombre de archivo de efecto, que solo se usa para los mensajes de error. Puede ser **NULL.**

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Matriz terminada en NULL de macros de sombreador (vea [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca esta opción en **NULL** para no especificar macros.

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntero a una interfaz include (vea [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); establezca esta opción **en NULL** para especificar que no hay ningún archivo de include.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (vea [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Use **NULL** para especificar que esta función no debe devolverse hasta que se complete.

</dd> <dt>

*ppShaderText* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a la memoria (vea [**INTERFAZ ID3D10Blob)**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene el sombreador nocompilado.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero a la memoria (vea [**INTERFAZ ID3D10Blob)**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene errores de creación de efectos, si se produjo alguno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
