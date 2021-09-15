---
description: Usar texturas comprimidas (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Usar texturas comprimidas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473238"
---
# <a name="using-compressed-textures-direct3d-9"></a>Usar texturas comprimidas (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Determinar la compatibilidad con texturas comprimidas

Para probar el adaptador, especifique cualquier formato de píxel que use DXT1, DXT2, DXT3, DXT4 o DXT5. Si [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) devuelve D3D OK, el dispositivo puede crear textura directamente a partir de una superficie de textura comprimida \_ que use ese formato. Si es así, puede usar superficies de textura comprimidas directamente con Direct3D llamando al método [**IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) En el ejemplo de código siguiente se muestra cómo determinar si el adaptador admite un formato de textura comprimido.


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



Si el dispositivo no admite el texturing desde superficies de textura comprimidas, puede almacenar los datos de textura en una superficie de formato comprimido, pero debe convertir las texturas comprimidas a un formato compatible antes de que se puedan usar para el texturing.

## <a name="creating-compressed-textures"></a>Crear texturas comprimidas

Después de crear un dispositivo que admita un formato de textura comprimido en el adaptador, puede crear un recurso de textura comprimido. Llame [**a IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) y especifique un formato de textura comprimido para el parámetro Format.

Antes de cargar una imagen en un objeto de textura, recupere un puntero a la superficie de textura mediante una llamada al método [**IDirect3DTexture9::GetSurfaceLevel.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

Ahora puede usar cualquier función D3DXLoadSurfacexxx para cargar una imagen en la superficie recuperada mediante [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel). Estas funciones controlan la conversión a y desde formatos de textura comprimidos.

Puede crear y convertir archivos de textura comprimida (DDS) mediante el Editor de texturas de DirectX (Dxtex.exe) proporcionado con el SDK de DirectX. Puede obtener información Dxtex.exe y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

La ventaja de este comportamiento es que una aplicación puede copiar el contenido de una superficie comprimida en un archivo sin calcular cuánto almacenamiento se necesita para una superficie de un ancho y alto determinados en el formato específico.

En la tabla siguiente se muestran los cinco tipos de texturas comprimidas. Para obtener más información sobre cómo se almacenan los datos, vea Formatos de textura [comprimidos (Direct3D 9).](compressed-texture-formats.md) Solo necesita esta información si está escribiendo sus propias rutinas de compresión.



| FOURCC | Descripción        | ¿Alfa premultiplicado? |
|--------|--------------------|----------------------|
| DXT1   | Alfa opaco/de 1 bit | N/D                  |
| DXT2   | Alfa explícito     | Sí                  |
| DXT3   | Alfa explícito     | No                   |
| DXT4   | Alfa interpolado | Sí                  |
| DXT5   | Alfa interpolado | No                   |



 

Al transferir datos de un formato no multiplicado a un formato premultiplicado, Direct3D escala los colores en función de los valores alfa. No se admite la transferencia de datos de un formato premultiplicado a un formato no multiplicado. Si intenta transferir datos desde un origen alfa premultiplicado a un destino alfa no multiplicado, el método devuelve D3DERR \_ INVALIDCALL. Si transfiere datos de un origen alfa premultiplicado a un destino que no tiene alfa, los componentes de color de origen, que se han escalado mediante alfa, se copian tal cual.

## <a name="decompressing-compressed-texture-surfaces"></a>Descompresión de superficies de textura comprimida

Al igual que con la compresión de una superficie de textura, la descompresión de una textura comprimida se realiza a través de los servicios de copia de Direct3D.

Para copiar una superficie de textura comprimida en una superficie de textura sin comprimir, use la función [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md). Esta función controla la compresión hacia y desde superficies comprimidas y sin comprimir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de textura comprimidos](compressed-texture-resources.md)
</dt> </dl>

 

 
