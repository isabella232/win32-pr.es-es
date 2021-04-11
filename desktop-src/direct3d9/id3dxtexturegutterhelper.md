---
description: La interfaz ID3DXTextureGutterHelper se usa para crear y administrar regiones de medianil en una textura. Las regiones de medianil separan las texturas y permiten la interpolación bilineal para evitar la representación de artefactos en los límites de textura.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interfaz ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362722"
---
# <a name="id3dxtexturegutterhelper-interface"></a>Interfaz ID3DXTextureGutterHelper

La interfaz ID3DXTextureGutterHelper se usa para crear y administrar regiones de medianil en una textura. Las regiones de medianil separan las texturas y permiten la interpolación bilineal para evitar la representación de artefactos en los límites de textura.

La... los métodos proporcionan acceso a las estructuras de datos que usa el método Apply... modalidades.

## <a name="members"></a>Miembros

La interfaz **ID3DXTextureGutterHelper** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureGutterHelper** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXTextureGutterHelper** tiene estos métodos.



| Método                                                                   | Descripción                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Aplica medianils a un búfer de textura flotante.<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | Aplica medianils a un objeto de búfer de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | Aplica medianils a un objeto de textura [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | Recupera las coordenadas de Barycentric de textura.<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | Recupera el índice de la superficie de la malla a la que pertenece cada textura.<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | Recibe un valor de la clase textura que indica la clase textura según la ubicación de cada textura.<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | Recupera el alto de la textura, en píxeles.<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | Recupera las coordenadas de textura (u, v) de cada textura.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Recupera el ancho de la textura, en píxeles.<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | Remuestrea una textura en la parametrización de esta gutterhelper.<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | Establece las coordenadas de Barycentric de textura.<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | Establece el índice de la superficie de la malla a la que pertenece cada textura.<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | Establece un valor de la clase textura que indica la clase textura según la ubicación de cada textura.<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | Establece las coordenadas de textura (u, v) de cada textura.<br/>                                          |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Cuando se usa con radiance Transfer (PRT) precalculado, esta interfaz requiere una parametrización única del modelo. Cada textura debe corresponder a un solo punto en la superficie del modelo y viceversa. Si el modelo incluye varias texturas, debe dividirse en partes independientes, cada una de las cuales contenga un objeto auxiliar de medianil por textura.

 

Esta interfaz se puede usar para generar un mapa en el espacio de textura en el que cada textura se encuentra en una de las cuatro clases.



| Clase textura | Ubicación de textura                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto no válido; no se usará textura.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triángulo interior.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Encuadernación interior.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Encuadernación interior; textura se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

En el caso de las clases 1 y 2, un textura se almacena con la superficie a la que pertenece, junto con las coordenadas Barycentric de los dos primeros vértices de esa superficie. Los vértices de medianil se asignan al borde más cercano en el espacio de textura.

No hay ninguna clase textura 3.

La interfaz **ID3DXTextureGutterHelper** se obtiene mediante una llamada a la función [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .

El tipo LPD3DXTEXTUREGUTTERHELPER se define como un puntero a la interfaz **ID3DXTextureGutterHelper** .


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
