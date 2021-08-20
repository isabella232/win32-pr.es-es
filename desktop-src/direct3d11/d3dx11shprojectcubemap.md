---
title: Función D3DX11SHProjectCubeMap (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la biblioteca matemática Spherical Estadípticas, SHProjectCubeMap.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Función D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2002505a39703601607eb6cec89afed1c54dfec2e361c0afa517e11ed6e6035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099257"
---
# <a name="d3dx11shprojectcubemap-function"></a>Función D3DX11SHProjectCubeMap

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca matemática [Spherical Estadípticas,](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) **SHProjectCubeMap**.

 

Proyecta una función representada en un mapa de cubo en armónicos esféricos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntero a un [**objeto ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> <dt>

*Pedido* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

El orden de la evaluación sh genera coeficientes Order^2 cuyo grado es Order-1. El intervalo válido está entre 2 y 6.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntero a un [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa un mapa de cubo que se va a proyectar en armónicos esféricos.

</dd> <dt>

*Prout* 
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***

Vector SH de salida para rojo.

</dd> <dt>

*pGOut* 
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***

Vector SH de salida para verde.

</dd> <dt>

*pBOut* 
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)\***

Vector SH de salida para azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

