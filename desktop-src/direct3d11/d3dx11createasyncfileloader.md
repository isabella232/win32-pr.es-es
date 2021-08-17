---
title: Función D3DX11CreateAsyncFileLoader (D3DX11async.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Vea la sección Comentarios. Cree un cargador de archivos asincrónicos.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- Función D3DX11CreateAsyncFileLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5997d31765df1de78ed6323a0176be024a5e26bb2eb81a0556f2abedbf2e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124870"
---
# <a name="d3dx11createasyncfileloader-function"></a>Función D3DX11CreateAsyncFileLoader

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Vea la sección Comentarios.

 

Cree un cargador de archivos asincrónicos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFileName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre del archivo que se va a cargar. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos se resuelve en LPCSTR.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***

Dirección de un puntero al cargador de datos asincrónicos (vea [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.

Para Windows Store, los ejemplos de DirectX (por ejemplo, el ejemplo de tutorial de [Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica de Windows Runtime [**(AsyncBase).**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))

En el caso de las aplicaciones de escritorio win32, puede usar el Runtime de simultaneidad [para](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) implementar algo similar al modelo de programación asincrónica de Windows Runtime.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

