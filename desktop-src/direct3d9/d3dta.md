---
description: 'Las constantes de argumento de textura se utilizan como valores para los siguientes miembros del tipo enumerado D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58d4d5665b1a098b84eaa95294e69220d6ea4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714875"
---
# <a name="d3dta"></a>D3DTA

Las constantes de argumento de textura se utilizan como valores para los siguientes miembros del tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

Establecer y recuperar argumentos de textura mediante una llamada a los métodos [**SetTextureStageState**](/windows/desktop/api) y [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .

Marcas de argumento

Puede combinar una marca de argumento con un modificador, pero no se pueden combinar dos marcas de argumento.



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| D3DTA \_ constante)   | Seleccione una constante en una fase de textura. El valor predeterminado es 0xFFFFFFFF.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ actual    | El argumento Texture es el resultado de la fase de fusión anterior. En la primera fase de textura (fase 0), este argumento es equivalente a \_ difuso D3DTA. Si la fase de fusión anterior usa una textura de mapa de rugosidad (la \_ operación D3DTOP BUMPENVMAP), el sistema elige la textura de la fase anterior a la textura del mapa de rugosidad. Si s representa la fase de textura actual y s-1 contiene una textura de mapa de rugosidad, este argumento se convierte en el resultado de la fase de textura s-2. Los permisos son de lectura/escritura. |
| \_Difusión D3DTA    | El argumento Texture es el color difuso interpolado desde los componentes de vértice durante el sombreado Gouraud. Si el vértice no contiene un color difuso, el color predeterminado es 0xFFFFFFFF. Los permisos son de solo lectura.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | Valor de máscara para todos los argumentos; no se utiliza al establecer argumentos de textura.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_Reflejo D3DTA   | El argumento Texture es el color especular interpolado desde los componentes de vértice durante el sombreado Gouraud. Si el vértice no contiene un color especular, el color predeterminado es 0xFFFFFFFF. Los permisos son de solo lectura.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ Temp       | El argumento Texture es un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la funcionalidad del dispositivo [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) está presente. El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0). Los permisos son de lectura/escritura.                                                                                                                                                                                                                                   |
| \_Textura D3DTA    | El argumento Texture es el color de la textura de esta fase de textura. Los permisos son de solo lectura.                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ TFACTOR    | El argumento Texture es el factor de textura establecido en una llamada anterior a [**SetRenderState**](/windows/desktop/api) con el valor de representación de [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) . Los permisos son de solo lectura.                                                                                                                                                                                                                                                       |



 

Marcas modificadoras

Una marca de argumento se puede combinar con uno de los siguientes marcadores de modificador.



|                       |                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| \#define              | Descripción                                                                                                    |
| D3DTA \_ ALPHAREPLICATE | Replique la información alfa en todos los canales de color antes de que se complete la operación. Este es un modificador de lectura. |
| Complemento de D3DTA \_     | Tome el complemento del argumento x, (1,0-x). Este es un modificador de lectura.                                     |



 

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3d9types. h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
