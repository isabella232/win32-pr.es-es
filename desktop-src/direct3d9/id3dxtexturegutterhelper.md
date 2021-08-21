---
description: La interfaz ID3DXTextureGutterHelper se usa para compilar y administrar regiones de canalón en una textura. Las regiones de canalizaciones separan texturas y permiten la interpolación bilineal para evitar la representación de artefactos en los límites de textura.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interfaz ID3DXTextureGutterHelper (D3DX9Mesh.h)
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
ms.openlocfilehash: e8e72814c036e297111a4a2f3825574a2a088310cb17d484902c59875958e7e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118093959"
---
# <a name="id3dxtexturegutterhelper-interface"></a>Interfaz ID3DXTextureGutterHelper

La interfaz ID3DXTextureGutterHelper se usa para compilar y administrar regiones de canalón en una textura. Las regiones de canalizaciones separan texturas y permiten la interpolación bilineal para evitar la representación de artefactos en los límites de textura.

El botón Obtener... Los métodos proporcionan acceso a las estructuras de datos utilizadas por el método Apply... Métodos.

## <a name="members"></a>Miembros

La **interfaz ID3DXTextureGutterHelper** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXTextureGutterHelper** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXTextureGutterHelper tiene** estos métodos.



| Método                                                                   | Descripción                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Aplica los canales a un búfer de textura FLOAT.<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | Aplica los canales a un objeto de búfer [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | Aplica los canales a un objeto de textura [**IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | Recupera coordenadas baricéntricas de texel.<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | Recupera el índice de la cara de malla a la que pertenece cada elemento de textura.<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | Recibe un valor de clase de texel que indica la clase de texel según la ubicación de cada texel.<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | Recupera el alto de la textura, en píxeles.<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | Recupera las coordenadas de textura (u, v) de cada texel.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Recupera el ancho de la textura, en píxeles.<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | Vuelve a muestrear una textura en la parametrización de este gutterhelper.<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | Establece coordenadas baricéntricas de texel.<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | Establece el índice de la cara de malla a la que pertenece cada elemento de textura.<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | Establece un valor de clase de texel que indica la clase de texel según la ubicación de cada texel.<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | Establece las coordenadas de textura (u, v) de cada texel.<br/>                                          |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> Cuando se usa con la transferencia de radiancia precalutada (PRT), esta interfaz requiere una parametrización única del modelo. Cada texel debe corresponder a un único punto en la superficie del modelo y viceversa. Si el modelo incluye varias texturas, debe dividirse en partes independientes que contengan un objeto auxiliar de medias por textura.

 

Esta interfaz se puede usar para generar un mapa en el espacio de textura en el que cada elemento de textura se encuentra en una de las cuatro clases.



| Texel (clase) | Ubicación de Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto no válido; No se usará texel.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Dentro del triángulo.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Dentro del medianía.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Dentro del medianía; Texel se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper::ApplyGuttersPRT.**](id3dxtexturegutterhelper--applyguttersprt.md) |



 

Para las clases 1 y 2, se almacena un texel con la cara a la que pertenece, junto con coordenadas barítticas de los dos primeros vértices de esa cara. Los vértices de los canales se asignan al borde más cercano en el espacio de textura.

No hay ninguna clase de texel 3.

La **interfaz ID3DXTextureGutterHelper** se obtiene llamando a la función [**D3DXCreateTextureGutterHelper.**](d3dxcreatetexturegutterhelper.md)

El tipo LPD3DXTEXTUREGUTTERHELPER se define como un puntero a la **interfaz ID3DXTextureGutterHelper.**


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
