---
title: Función D3DX11CreateTextureFromResource (D3DX11.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar funciones de recursos y, a continuación, estas bibliotecas DirectXTK (runtime), CreateXXXTextureFromMemory (donde XXX es DDS o WIC)Biblioteca DirectXTex (herramientas), LoadFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos) y, a continuación, CreateTexture Cree una textura a partir de otro recurso.
ms.assetid: 2b62239a-c19b-4d4f-9fd2-afcd87ba0fac
keywords:
- Función D3DX11CreateTextureFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 886e289905ba10be088cc1fdc21802a07051ae8f9ea65f6e8781644db2c42183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124680"
---
# <a name="d3dx11createtexturefromresource-function"></a>Función D3DX11CreateTextureFromResource

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar las funciones [de recursos](/windows/desktop/menurc/resources-functions)y, a continuación, estas:
>
> -   [Biblioteca DirectXTK](https://github.com/Microsoft/DirectXTK) (runtime), **CreateXXXTextureFromMemory** (donde XXX es DDS o WIC)
> -   [Biblioteca DirectXTex](https://github.com/Microsoft/DirectXTex) (herramientas), **LoadFromXXXMemory** (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 compatible con TGA como un formato de origen de arte común para juegos) y, a **continuación, CreateTexture**

 

Cree una textura a partir de otro recurso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateTextureFromResource(
  _In_  ID3D11Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntero al dispositivo (consulte [**ID3D11Device)**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)que usará el recurso.

</dd> <dt>

*hSrcModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Identificador del recurso de origen. HMODULE se puede obtener con la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*pSrcResource* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Cadena que contiene el nombre del recurso de origen. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*pLoadInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)\***

Opcional. Identifica las características de una textura (vea [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Puntero a una interfaz de bombeo de subprocesos (vea [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)). Si se especifica **NULL,** esta función se comportará sincrónicamente y no volverá hasta que finalice.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***

Dirección de un puntero al recurso de textura (vea [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).

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
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

