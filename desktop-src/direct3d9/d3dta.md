---
description: 'Las constantes de argumento de textura se usan como valores para los siguientes miembros del tipo enumerado D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db520bee7e4352b3242824819cc579acd82b1d013d290b2155d54170bc478c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527319"
---
# <a name="d3dta"></a>D3DTA

Las constantes de argumento de textura se usan como valores para los siguientes miembros del tipo enumerado [**D3DTEXTURESTAGESTATETYPE:**](./d3dtexturestagestatetype.md)

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

Establezca y recupere argumentos de textura mediante una llamada a los [**métodos SetTextureStageState**](/windows/desktop/api) [**y GetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)

Marcas de argumentos

Puede combinar una marca de argumento con un modificador , pero no se pueden combinar dos marcas de argumento.



| \#Definir          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTA \_ (CONSTANTE)   | Seleccione una constante de una fase de textura. El valor predeterminado es 0xffffffff.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ ACTUAL    | El argumento de textura es el resultado de la fase de mezcla anterior. En la primera fase de textura (fase 0), este argumento es equivalente a D3DTA \_ DIFUSO. Si la fase de mezcla anterior usa una textura de mapa de protuberancias (la operación D3DTOP BUMPENVMAP), el sistema elige la textura de la fase antes de la textura del mapa \_ de protuberancias. Si s representa la fase de textura actual y s - 1 contiene una textura de mapa de protuberancias, este argumento se convierte en la salida del resultado por fases de textura s - 2. Los permisos son de lectura y escritura. |
| D3DTA \_ DIFUSO    | El argumento de textura es el color difuso interpolado a partir de componentes de vértice durante el sombreado de Gouraud. Si el vértice no contiene un color difuso, el color predeterminado es 0xffffffff. Los permisos son de solo lectura.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | Valor de máscara para todos los argumentos; no se usa al establecer argumentos de textura.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ SPECULAR   | El argumento de textura es el color especular interpolado a partir de los componentes de vértice durante el sombreado de Gouraud. Si el vértice no contiene un color especular, el color predeterminado es 0xffffffff. Los permisos son de solo lectura.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ TEMP       | El argumento de textura es un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) está presente. El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0). Los permisos son de lectura y escritura.                                                                                                                                                                                                                                   |
| TEXTURA \_ D3DTA    | El argumento de textura es el color de textura de esta fase de textura. Los permisos son de solo lectura.                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ TFACTOR    | El argumento texture es el factor de textura establecido en una llamada anterior a [**SetRenderState**](/windows/desktop/api) con el valor de render-state [**de \_ TEXTUREFACTOR de D3DRS.**](./d3drenderstatetype.md) Los permisos son de solo lectura.                                                                                                                                                                                                                                                       |



 

Marcas modificadoras

Una marca de argumento se puede combinar con una de las siguientes marcas modificadoras.



| \#Definir              | Descripción                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| D3DTA \_ ALPHAREPLICATE | Replique la información alfa en todos los canales de color antes de que finalice la operación. Se trata de un modificador de lectura. |
| COMPLEMENTO D3DTA \_     | Tome el complemento del argumento x, (1.0 - x). Se trata de un modificador de lectura.                                     |



 

## <a name="constant-information"></a>Información constante



|   Requisito                       |  Value           |
|--------------------------|-------------|
| Encabezado                   | d3d9types.h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
