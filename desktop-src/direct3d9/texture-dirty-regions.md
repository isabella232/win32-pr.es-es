---
description: Las aplicaciones pueden optimizar qué subconjunto de una textura se copia especificando &\# 0034;dirty&\# 0034; regiones en texturas.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Regiones de texturas desaseadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465654"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Regiones de texturas desaseadas (Direct3D 9)

Las aplicaciones pueden optimizar qué subconjunto de una textura se copia especificando regiones "desaseadas" en las texturas. Una llamada a [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)copia solo las regiones marcadas como desaseadas. Sin embargo, las regiones desalineadas se pueden expandir para optimizar la alineación. Cuando se crea una textura, se considera que toda la textura está desaseada. Solo las operaciones siguientes afectan al estado de des dirty de una textura:

-   Agregar una región desaseinada a una textura.
-   Bloqueo de algún búfer en la textura. Esta operación agrega la región bloqueada como región desaseinada. La aplicación puede desactivar esta actualización automática de regiones desa pruebas si tiene un mejor conocimiento de las regiones desaseñadas reales.
-   El uso de un nivel de superficie de la textura como destino en [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) marca toda la textura como desnuciada.
-   El uso de la textura como origen en [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) borra todas las regiones desaseadas de la textura de origen.
-   Uso [**de IDirect3DSurface9::GetDC para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) devolver un contexto de dispositivo.
-   Al [**llamar a IDirect3DBaseTexture9::GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) se marca toda la textura como desusada.
-   Al [**llamar a IDirect3DBaseTexture9::SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) se marca toda la textura como desaseada.

Las regiones desaprobadas se establecen en el nivel superior de una textura mipmapped e [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) puede expandir la región desaprobada en la cadena mip para minimizar el número de bytes copiados para cada subnivel. Tenga en cuenta que las coordenadas de la región desardenada de subnivel se redondean hacia el exterior, es decir, sus fracciones se redondean hacia el borde más cercano de la textura.

Dado que cada tipo de textura tiene diferentes tipos de regiones desa pruebas, hay métodos en cada tipo de textura. Las texturas 2D usan rectángulos sucios y las texturas de volumen usan cuadros.

-   [**IDirect3DCubeTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

Si **se pasa NULL** para los parámetros pDirtyRect o pDirtyBox de los métodos anteriores, se expande la región desaprobación para cubrir toda la textura.

Cada método de bloqueo puede tomar D3DLOCK NO DIRTY UPDATE, lo que evita cualquier cambio en el estado desarroba \_ \_ de la \_ textura. Para obtener más información, vea [Bloqueo de recursos (Direct3D 9).](locking-resources.md)

Cuando haya disponible más información sobre el verdadero conjunto de regiones que se cambian durante una operación de bloqueo, las aplicaciones deben usar D3DLOCK \_ NO \_ DIRTY \_ UPDATE. Tenga en cuenta que un bloqueo o una copia solo en un subnivel de textura (es decir, sin bloquear ni copiar en el nivel superior) no actualiza las regiones desaprobadas para esa textura. Las aplicaciones asumen la misma responsabilidad de actualizar las regiones desapercibadas cuando bloquean los niveles inferiores sin bloquear el nivel superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
