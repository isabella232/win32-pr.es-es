---
title: Función D3DX11CreateAsyncResourceLoader (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un cargador de recursos asíncronos.
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- Función D3DX11CreateAsyncResourceLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083770"
---
# <a name="d3dx11createasyncresourceloader-function"></a>D3DX11CreateAsyncResourceLoader función)

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.

 

Cree un cargador de recursos asíncronos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcModule* \[ de\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Identificador del módulo de recursos. Use la [función GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obtener el identificador.

</dd> <dt>

*pSrcResource* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del recurso en hSrcModule. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos se resuelve como LPCSTR.

</dd> <dt>

*ppDataLoader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

La dirección de un puntero al cargador de datos asincrónicos (vea [**ID3DX11DataLoader (interfaz**](id3dx11dataloader.md))).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.

En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

