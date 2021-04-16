---
description: Las texturas tradicionales se consideran texturas de un solo elemento.
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: Texturas de varios elementos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a434d1e6c6a892c794551aa0caf34890f3def9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696068"
---
# <a name="multiple-element-textures-direct3d-9"></a>Texturas de varios elementos (Direct3D 9)

Las texturas tradicionales se consideran texturas de un solo elemento. Las texturas de varios elementos permiten a las aplicaciones escribir simultáneamente en varios elementos de una textura desde el sombreador de píxeles. El resultado en el siguiente paso de representación es que una aplicación puede usar uno o varios de los elementos como textura de un solo elemento, es decir, como entradas para el sombreador de píxeles. Estos elementos adicionales se pueden considerar como un almacén temporal de resultados intermedios que se usarán en un paso posterior de la aplicación.

La primera generación de hardware que expone esta característica tiene las siguientes restricciones:

-   Todas las superficies de textura de varios elementos se asignarán automáticamente. Para solucionar esta limitación, se trata como un nuevo tipo de formato de superficie con varios canales RGBA intercalados.
-   Todos los elementos de la textura de varios elementos pueden tener la misma profundidad de bits. Esta limitación se expresa mediante el nombre de los nuevos formatos de superficie.
-   Una textura de varios elementos no puede ser Primary/displayable. En otras palabras, debe ser solo de pantalla. Esta limitación se expresa mediante la enumeración de formato de superficie.
-   No se permiten tramas, pruebas alfa, luneta térmica, fusión, operación de trama o enmascaramiento. No se realiza ningún procesamiento del sombreador posterior a los píxeles, salvo la prueba z y la prueba de estarcido.
-   La textura no puede ser un mipmap. Se producirá un error en la creación de la cadena MIP.
-   No se puede establecer el mismo elemento como textura al mismo tiempo que es un destino de representación. Sin embargo, los distintos elementos de la misma superficie de textura de varios elementos pueden ser simultáneamente texturas y destinos de representación.
-   No se admite el suavizado de contorno.
-   Las superficies de textura de varios elementos, cuando se usan como textura, no se pueden filtrar. Esta limitación se puede comprobar mediante [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   No se pueden bloquear superficies de textura de varios elementos.
-   Se puede usar más de una superficie de textura de varios elementos al mismo tiempo asignando cada una a varias fases, al igual que con las texturas normales.
-   Las superficies de textura de varios elementos admiten la conversión de gamma de la conversión de 2,2 a 1,0 en una operación de lectura, al igual que con otros formatos de textura.
-   Algunas de las implementaciones no aplican la máscara de escritura de salida (D3DRS \_ COLORWRITEENABLE). Aquellos que pueden tener máscaras de escritura de color independientes. Esto se expresa mediante un nuevo bit de capacidad. El número de máscaras de escritura de color independientes disponibles será igual al número máximo de elementos de los que el dispositivo es compatible.
-   [**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) borra todos los elementos de la textura de varios elementos que se establece como destino de representación.

El uso de texturas de varios elementos sigue estos pasos:

1.  Las aplicaciones detectan la compatibilidad con esta característica comprobando la disponibilidad de los formatos de textura de varios elementos.
2.  La aplicación crea estas superficies mediante una llamada a [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture).
3.  La aplicación establece la superficie como destino de representación mediante la llamada a [**SetRenderTarget**](/windows/desktop/api) . El sombreador de píxeles proporciona la salida a las superficies mediante la instrucción [MOV-PS](../direct3dhlsl/mov---ps.md) .
4.  Se llama a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para establecer una superficie de textura de varios elementos en una fase determinada. Como con otras texturas, se permite que la misma superficie se establezca en varias fases a la vez.
5.  Se llama a [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para establecer D3DSAMP ELEMENTINDEX en el \_ número de elemento adecuado en la textura de varios elementos de la que muestrea el muestreador. El valor predeterminado de este estado es 0, lo que significa que las texturas que no son de varios elementos funcionarán. Si se establece este estado en un número inadecuado, se produce un comportamiento indefinido: Si la textura de varios elementos solo tiene dos elementos, pero la muestra se solicita para muestrear el cuarto elemento, por ejemplo.

## <a name="api-support"></a>Compatibilidad de la API

A continuación se ofrece un resumen de los elementos de la API que admiten texturas de varios elementos:

-   El formato de superficie de [ \_ \_ ARGB8 de MULTI2 de D3DFMT](d3dformat.md) expresa la naturaleza intercalada del formato.
-   El estado de la muestra de D3DSAMP \_ ELEMENTINDEX indica el índice de elemento que se va a usar.
-   Los siguientes Estados de representación admiten texturas de varios elementos:

    -   D3DRS \_ COLORWRITEENABLE1
    -   D3DRS \_ COLORWRITEENABLE2
    -   D3DRS \_ COLORWRITEENABLE3

    D3DRS \_ COLORWRITEENABLE se aplica al destino de representación (o elemento) cero.

-   La marca [D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS](d3dpmisccaps.md) indica que el dispositivo admite máscaras de escritura independientes para varias texturas de elemento o varios destinos de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
