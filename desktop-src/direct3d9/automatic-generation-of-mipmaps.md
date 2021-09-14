---
description: Ahora puede crear automáticamente un mapa mip, que es una serie de texturas, cada una filtrada por una resolución diferente.
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: Generación automática de mapas Mip (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060756"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>Generación automática de mapas Mip (Direct3D 9)

Ahora puede crear automáticamente un mapa mip, que es una serie de texturas, cada una filtrada por una resolución diferente. Los mapas Mip se usan normalmente para proporcionar diferentes niveles de detalle al representarse. La generación automática de mapas MIP en tiempo de creación de textura aprovecha el filtrado de hardware porque el mapa mipmap reside en la memoria de vídeo.

Para generar un mapa mip automáticamente, establezca un nuevo [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) de uso antes de llamar a [**CreateTexture**](/windows/desktop/api). La generación de subniveles a partir de este momento es completamente transparente para la aplicación. Solo la aplicación puede acceder al nivel de textura superior; Los subniveles de textura no son accesibles, ya que solo se crearán cuando el controlador los necesite. En los casos en los que la generación de subniveles puede tardar mucho tiempo, use [**GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) para dar indicaciones al controlador de que debe generar subniveles a la vez adecuados para la aplicación.

## <a name="mipmap-filtering"></a>Filtrado de mapa mip

[**SetAutoGenFilterType controla**](/windows/desktop/api) la calidad del filtrado durante la generación automática. Al cambiar el tipo de filtro, los subniveles mipmap se regeneran. Use [**GetAutoGenFilterType para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) obtener el tipo de filtro actual. El tipo de filtro predeterminado es D3DTEXF \_ LINEAR. Si el controlador no admite un filtro lineal, el tipo de filtro se establecerá en D3DTEXF \_ POINT.

Estos métodos no tienen ningún efecto si la textura no se crea con [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) y no se devuelve ningún error. Todos los tipos de filtro admitidos por el controlador para el filtrado de textura normal se admiten para la generación automática, excepto D3DTEXF \_ NONE. Para cada tipo de recurso, los controladores deben admitir todos los tipos de filtro notificados en los límites de filtro de textura, CubeTexture y volumetexture correspondientes.

Para comprobar qué tipos de filtro se admiten, compruebe qué límites son compatibles con los miembros TextureFilterCaps o CubeTextureFilterCaps de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="mipmap-support"></a>Compatibilidad con Mipmap

[D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) es solo una sugerencia y especificarlo durante la creación de texturas o al llamar a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) no provocaría un error en ninguno de los tipos de interfaz de controlador de dispositivo (DDI).

Llamar [**a UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) no es posible cuando el origen es un mapa mipmap generado automáticamente, pero el destino no lo es. El origen puede ser un mapa mipmap no generado automáticamente y el destino puede ser un mapa MIP generado automáticamente. En este caso, solo se actualiza el nivel de coincidencia superior. Se omiten todos los demás subniveles de origen. Del mismo modo, cuando el origen y el destino se generan automáticamente, solo se actualiza el nivel de coincidencia superior. Los subniveles del origen se omiten y se regeneran los subniveles de destino.

Para comprobar la compatibilidad con la generación automática de mapas mip, compruebe que [D3DCAPS2 \_ CANAUTOGENMIPMAP](d3dcaps2.md) está establecido. Si es así, llame a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md). Si el valor devuelto es D3D OK, se garantiza que \_ los mapas mip se generan automáticamente. Si el valor devuelto es D3DOK NOAUTOGEN, significa que la llamada de creación se realizará correctamente, pero no se generará \_ ningún mipmap.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
