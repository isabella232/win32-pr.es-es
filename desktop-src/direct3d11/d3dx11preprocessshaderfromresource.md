---
title: Función D3DX11PreprocessShaderFromResource (D3DX11async.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la API D3DPreprocess. Cree un sombreador a partir de un recurso sin compilarlo.
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- Función D3DX11PreprocessShaderFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34aef8bad8220e9f579560c8e47477a96313bbddd9ed6970710ffffc263da35e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124660"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a>Función D3DX11PreprocessShaderFromResource

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la API [**D3DPreprocess.**](/windows/desktop/direct3dhlsl/d3dpreprocess)

 

Cree un sombreador a partir de un recurso sin compilarlo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Identificador del módulo de recursos que contiene el sombreador. HMODULE se puede obtener con la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pResourceName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del recurso en el lado hModule que contiene el sombreador. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve en LPCSTR.

</dd> <dt>

*pSrcFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Opcional. Nombre de archivo de efecto, que solo se usa para los mensajes de error. Puede ser **NULL.**

</dd> <dt>

*pDefines* \[ En\]
</dt> <dd>

Tipo: **const D3D11 \_ SHADER \_ MACRO \***

Matriz terminada en NULL de macros de sombreador; establezca esta opción **en NULL** para no especificar macros.

</dd> <dt>

*pInclude* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntero a una interfaz include; establezca esta opción **en NULL** para especificar que no hay ningún archivo de include.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (vea [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Use **NULL** para especificar que esta función no debe devolver hasta que se complete.

</dd> <dt>

*ppShaderText* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Puntero a la memoria que contiene el sombreador nocompilado.

</dd> <dt>

*ppErrorMsgs* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Dirección de un puntero a la memoria que contiene errores de creación de efectos, si se produjo alguno.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

