---
description: Cree un grupo de efectos a partir de un recurso.
ms.assetid: 594ab788-fd96-4ea9-ad93-ef02fefa5d61
title: Función D3DX10CreateEffectPoolFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: a4e0130a5712e8c60c7f6d3b101a91db9e62f1cc66bed959c49a923923d2ec5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989205"
---
# <a name="d3dx10createeffectpoolfromresource-function"></a>Función D3DX10CreateEffectPoolFromResource

Cree un grupo de efectos a partir de un recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateEffectPoolFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _In_        ID3D10EffectPool   **ppEffectPool,
  _In_        ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador del módulo de recursos que contiene el efecto. HMODULE se puede obtener con [la función GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pResourceName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nombre del recurso en hModule. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos se resuelve en LPCSTR.

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

Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Puntero a una interfaz include (vea [**ID3D10Include Interface).**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) Este parámetro puede ser **NULL**.

</dd> <dt>

*pProfile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadena que especifica el perfil de [sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)o el modelo de sombreador.

</dd> <dt>

*HLSLFlags* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opciones de compilación HLSL (vea [D3D10 \_ SHADER Constants](d3d10-shader.md)).

</dd> <dt>

*FXFlags* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opciones de compilación de efecto [(vea Compilar y marcas de efecto).](d3d10-graphics-reference-effect-constants.md)

</dd> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Puntero al dispositivo (vea [**ID3D10Device Interface)**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)que usará los recursos.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos [**(vea ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Use **NULL** para especificar que esta función no debe devolverse hasta que se complete.

</dd> <dt>

*ppEffectPool* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***

Dirección de un puntero al grupo de efectos (vea [**Id3D10EffectPool (interfaz).**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)

</dd> <dt>

*ppErrors* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero a la memoria (vea [**Interfaz ID3D10Blob)**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)que contiene errores de compilación de efecto, si los hubiera.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
