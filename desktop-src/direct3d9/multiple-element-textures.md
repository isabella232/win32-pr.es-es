---
description: Las texturas tradicionales se consideran texturas de un solo elemento.
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: Texturas de varios elementos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a69c04c54f4be73b71a1ac5f2ead123bb51d649ad5e75369411b6bf0906517c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563545"
---
# <a name="multiple-element-textures-direct3d-9"></a>Texturas de varios elementos (Direct3D 9)

Las texturas tradicionales se consideran texturas de un solo elemento. Las texturas de varios elementos permiten a las aplicaciones escribir simultáneamente en varios elementos de una textura desde el sombreador de píxeles. El resultado en el siguiente paso de representación es que una aplicación puede usar uno o varios de los elementos como una textura de un solo elemento, es decir, como entradas para el sombreador de píxeles. Estos elementos adicionales se pueden pensar como un almacén temporal para los resultados intermedios que la aplicación usará en un paso posterior.

La primera generación de hardware que expone esta característica tiene las restricciones siguientes:

-   Todas las superficies de textura de varios elementos se asignarán automáticamente. Esta limitación se aborda tratando esto como un nuevo tipo de formato de superficie con varios canales RGBA intercalados.
-   Todos los elementos de la textura de varios elementos pueden tener la misma profundidad de bits. Esta limitación se expresa mediante el nombre de los nuevos formatos de superficie.
-   Una textura de varios elementos no puede ser la principal o que se puede mostrar. En otras palabras, solo debe estar fuera de pantalla. Esta limitación se expresa mediante la enumeración de formato de superficie.
-   No se permite el dithering, la prueba alfa, la fusión, la fusión, la operación de trama ni el enmascaramiento. No se realiza ningún procesamiento posterior al sombreador de píxeles, excepto la prueba z y la prueba de galería de símbolos.
-   La textura no puede ser un mapa mip. Se producirá un error en la creación de la cadena de mip.
-   El mismo elemento no se puede establecer como una textura al mismo tiempo que un destino de representación. Sin embargo, los distintos elementos de la misma superficie de textura de varios elementos pueden ser simultáneamente texturas y representar destinos.
-   No se admite suavizado de contorno.
-   Las superficies de textura de varios elementos, cuando se usan como textura, no se pueden filtrar. Esta limitación se puede comprobar mediante [**CheckDeviceFormat.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
-   Las superficies de textura de varios elementos no se pueden bloquear.
-   Se puede usar más de una superficie de textura de varios elementos simultáneamente mediante la asignación de cada una a varias fases, al igual que con las texturas normales.
-   Las superficies de textura de varios elementos admiten la conversión de gamma de la conversión 2.2 a 1.0 en una operación de lectura, al igual que con otros formatos de textura.
-   Algunas de las implementaciones no aplican la máscara de escritura de salida (D3DRS \_ COLORWRITEENABLE). Aquellos que pueden tener máscaras de escritura de color independientes. Esto se expresa mediante un nuevo bit de funcionalidad. El número de máscaras de escritura de color independientes disponibles será igual al número máximo de elementos de los que el dispositivo es capaz.
-   [**Borrar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) borra todos los elementos de la textura de varios elementos que se establece como destino de representación.

El uso de texturas de varios elementos sigue estos pasos:

1.  Las aplicaciones detectan la compatibilidad con esta característica comprobando la disponibilidad de los formatos de textura de varios elementos.
2.  La aplicación crea estas superficies mediante una [**llamada a CreateTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
3.  La aplicación establece la superficie como un destino de representación mediante la [**llamada SetRenderTarget.**](/windows/desktop/api) El sombreador de píxeles proporciona salida a las superficies mediante la [instrucción mov - ps.](../direct3dhlsl/mov---ps.md)
4.  [**Se llama a SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para establecer una superficie de textura de varios elementos en una fase determinada. Al igual que con otras texturas, se permite establecer la misma superficie en varias fases a la vez.
5.  [**Se llama a SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para establecer D3DSAMP ELEMENTINDEX en el número de elemento adecuado en la textura de varios elementos de la que se \_ muestrea el muestreador. El valor predeterminado para este estado es 0, lo que significa que funcionarán texturas que no son de varios elementos. Si se establece este estado en un número inadecuado, se produce un comportamiento indefinido, por ejemplo, si la textura de varios elementos tiene solo dos elementos de ancho, pero se pide al muestreador que muestree desde el cuarto elemento.

## <a name="api-support"></a>Compatibilidad de la API

A continuación se muestra un resumen de los elementos de API que admiten texturas de varios elementos:

-   El [formato de superficie D3DFMT \_ MULTI2 \_ ARGB8](d3dformat.md) expresa la naturaleza intercalada del formato.
-   El estado del \_ sampler D3DSAMP ELEMENTINDEX indica qué índice de elemento se va a usar.
-   Los siguientes estados de representación admiten texturas de varios elementos:

    -   D3DRS \_ COLORWRITEENABLE1
    -   D3DRS \_ COLORWRITEENABLE2
    -   D3DRS \_ COLORWRITEENABLE3

    D3DRS \_ COLORWRITEENABLE se aplica al destino de representación (o elemento) cero.

-   La [marca D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS](d3dpmisccaps.md) indica que el dispositivo admite máscaras de escritura independientes para varias texturas de elementos o varios destinos de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
