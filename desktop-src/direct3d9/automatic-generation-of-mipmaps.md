---
description: Ahora puede crear automáticamente un mipmap que es una serie de texturas, cada una filtrada por una resolución diferente.
ms.assetid: ae5955f9-e52a-41d7-a199-800e37a3e936
title: Generación automática de mapas MIP (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fda5b765d42ffa10f8cc5998daa66ae36c2bc75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705329"
---
# <a name="automatic-generation-of-mipmaps-direct3d-9"></a>Generación automática de mapas MIP (Direct3D 9)

Ahora puede crear automáticamente un mipmap que es una serie de texturas, cada una filtrada por una resolución diferente. Los mapas MIP se utilizan normalmente para proporcionar diferentes niveles de detalle al realizar la representación. La generación automática de mapas MIP en el momento de la creación de textura aprovecha el filtrado de hardware porque el mipmap reside en la memoria de vídeo.

Para generar automáticamente un mipmap, establezca un nuevo D3DUSAGE de uso [ \_ AUTOGENMIPMAP](d3dusage.md) antes de llamar a [**CreateTexture**](/windows/desktop/api). La generación de subnivel a partir de este punto en es completamente transparente para la aplicación. Solo el nivel superior de textura es accesible para la aplicación; no se puede obtener acceso a los subniveles de textura, ya que se crearán solo cuando los necesite el controlador. En los casos en los que la generación de subnivels puede tardar mucho tiempo, use [**GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) para sugerir al controlador que debe generar subniveles en el momento adecuado para la aplicación.

## <a name="mipmap-filtering"></a>Filtrado de mipmap

[**SetAutoGenFilterType**](/windows/desktop/api) controla la calidad del filtrado durante la generación automática. Al cambiar el tipo de filtro, se eliminan los subnivels del mipmap y se vuelven a generar. Use [**GetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getautogenfiltertype) para obtener el tipo de filtro actual. El tipo de filtro predeterminado es D3DTEXF \_ linear. Si el controlador no admite un filtro lineal, el tipo de filtro se establecerá en D3DTEXF \_ Point.

Estos métodos no tienen ningún efecto si la textura no se crea con [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) y no se devuelve ningún error. Todos los tipos de filtro admitidos por el controlador para el filtrado de textura normal se admiten para el autogenerado, excepto D3DTEXF \_ None. Para cada tipo de recurso, los controladores deben admitir todos los tipos de filtro que se indican en los límites de filtro de textura, CubeTexture y volumetexture correspondientes.

Para comprobar qué tipos de filtro se admiten, compruebe qué extremos son compatibles con los miembros TextureFilterCaps y/o CubeTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="mipmap-support"></a>Compatibilidad con mipmap

[D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md) es solo una sugerencia y si se especifica durante la creación de texturas o cuando se llama a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , no se produciría un error en ninguno de los tipos de la interfaz de controlador de dispositivo (DDI).

La llamada a [**UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) no es válida cuando el origen es un mipmap generado automáticamente, pero el destino no lo es. El origen puede ser un mipmap no generado automáticamente y el destino puede ser un mipmap generado automáticamente. En este caso, solo se actualiza el nivel de coincidencia superior. El resto de subnivels de origen se omiten. Del mismo modo, cuando el origen y el destino se generan automáticamente, solo se actualiza el nivel de coincidencia superior. Los subniveles del origen se omiten y se vuelven a generar los subnivels de destino.

Para comprobar la compatibilidad con la generación automática de mapas MIP, compruebe que [D3DCAPS2 \_ CANAUTOGENMIPMAP](d3dcaps2.md) está establecido. Si es así, llame a [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con [D3DUSAGE \_ AUTOGENMIPMAP](d3dusage.md). Si el valor devuelto es D3D \_ OK, se garantiza que los mapas MIP se generarán automáticamente. Si el valor devuelto es D3DOK \_ NOAUTOGEN, significa que la llamada a Create se realizará correctamente, pero no habrá ningún MIP generado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
