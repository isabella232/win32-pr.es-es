---
title: Función D3DX11CreateAsyncShaderResourceViewProcessor (D3DX11async.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Función D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566273"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a>Función D3DX11CreateAsyncShaderResourceViewProcessor

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Vea la sección Comentarios.

 

Cree un procesador de datos que cargará un recurso y, a continuación, cree una vista de sombreador y recurso para él. Los procesadores de datos son un componente de la característica de carga de datos asincrónica de D3DX11 que usa las [**bomba de subprocesos**](id3dx11threadpump.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntero al dispositivo Direct3D (consulte [**ID3D11Device)**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)que se usará para crear un recurso y una vista de recursos de sombreador para ese recurso.

</dd> <dt>

*pLoadInfo* \[ En\]
</dt> <dd>

Tipo: **[ **INFORMACIÓN DE CARGA DE \_ IMÁGENES \_ \_ D3DX11**](d3dx11-image-load-info.md)\***

Opcional. Identifica las características de una textura (vea [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) cuando se crea el procesador de datos; esta opción se establece en **NULL** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

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

 

