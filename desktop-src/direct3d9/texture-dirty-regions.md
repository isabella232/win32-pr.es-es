---
description: Las aplicaciones pueden optimizar qué subconjunto de una textura se copia especificando &\# 0034; sucio&\# 0034; regiones en las texturas.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Regiones desfasadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705237"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Regiones desfasadas de textura (Direct3D 9)

Las aplicaciones pueden optimizar qué subconjunto de una textura se copia especificando regiones "desfasadas" en las texturas. Solo las regiones marcadas como desfasadas se copian mediante una llamada a [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture). Sin embargo, las regiones desfasadas se pueden expandir para optimizar la alineación. Cuando se crea una textura, se considera que la textura completa se ha modificado. Solo las siguientes operaciones afectan al estado de modificación de una textura:

-   Agregar una región desfasada a una textura.
-   Bloquear algún búfer de la textura. Esta operación agrega la región bloqueada como una región desfasada. La aplicación puede desactivar esta actualización automática de la región desfasada si tiene un mejor conocimiento de las regiones desfasadas reales.
-   El uso de un nivel de superficie de la textura como un destino en [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) marca toda la textura como desfasada.
-   El uso de la textura como un origen en [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) borra todas las regiones desfasadas en la textura de origen.
-   Usar [**IDirect3DSurface9:: GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) para devolver un contexto de dispositivo.
-   Al llamar a [**IDirect3DBaseTexture9:: GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) , la textura completa se marca como desfasada.
-   Al llamar a [**IDirect3DBaseTexture9:: SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) , la textura completa se marca como desfasada.

Las regiones desfasadas se establecen en el nivel superior de una textura mipmapped y [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) puede expandir la región desfasada hacia abajo en la cadena MIP para minimizar el número de bytes copiados para cada subnivel. Tenga en cuenta que las coordenadas de la región desfasada de subnivel se redondean hacia afuera, es decir, sus partes fraccionarias se redondean hacia el borde más cercano de la textura.

Dado que cada tipo de textura tiene distintos tipos de regiones desfasadas, hay métodos en cada tipo de textura. las texturas 2D usan rectángulos modificados y cuadros de uso de texturas de volumen.

-   [**IDirect3DCubeTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

Si se pasan **valores NULL** para los parámetros PDirtyRect o pDirtyBox de los métodos anteriores, se expande la región desfasada para cubrir toda la textura.

Cada método de bloqueo puede tomar D3DLOCK \_ no hay ninguna \_ actualización no actualizada \_ , lo que impide que se produzcan cambios en el estado modificado de la textura. Para obtener más información, consulte [bloqueo de recursos (Direct3D 9)](locking-resources.md).

Si hay disponible más información sobre el conjunto real de regiones que se cambian durante una operación de bloqueo, las aplicaciones deben usar la \_ actualización D3DLOCK no \_ Dirty \_ . Tenga en cuenta que un bloqueo o una copia en un subnivel de textura únicamente (es decir, sin bloqueo ni copia en el nivel superior) no actualiza las regiones desfasadas para esa textura. Las aplicaciones suponen la misma responsabilidad para actualizar las regiones desfasadas cuando bloquean los niveles inferiores sin bloquear el nivel superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la texturización](basic-texturing-concepts.md)
</dt> </dl>

 

 
