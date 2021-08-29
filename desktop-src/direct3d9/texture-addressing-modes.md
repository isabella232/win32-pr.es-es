---
description: La aplicación Direct3D puede asignar coordenadas de textura a cualquier vértice de cualquier primitiva.
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: Modos de direccionamiento de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb1ccc45d6f3663f3e9f7e0bb1a721f594f7834db7de4541aa1dfece2954a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984785"
---
# <a name="texture-addressing-modes-direct3d-9"></a>Modos de direccionamiento de textura (Direct3D 9)

La aplicación Direct3D puede asignar coordenadas de textura a cualquier vértice de cualquier primitiva. Para obtener más información, vea [Coordenadas de textura (Direct3D 9).](texture-coordinates.md) Normalmente, las coordenadas de textura u y v que se asignan a un vértice se encuentran en el intervalo de 0,0 a 1,0, ambos inclusive. Sin embargo, al asignar coordenadas de textura fuera de ese intervalo, puede crear ciertos efectos de texturizado especiales.

Puede controlar lo que hace Direct3D con coordenadas de textura que están fuera del intervalo \[ 0.0, 1.0 estableciendo el modo \] de direccionamiento de textura. Por ejemplo, puede hacer que la aplicación establezca el modo de direccionamiento de textura para que una textura se en mosaico en una primitiva.

Direct3D permite a las aplicaciones realizar el ajuste de textura. Es importante tener en cuenta que establecer el modo de direccionamiento de textura en D3DTADDRESS WRAP no es lo mismo que realizar el \_ ajuste de textura. Al establecer el modo de direccionamiento de textura en D3DTADDRESS WRAP, se aplican varias copias de la textura de origen a la primitiva actual y la habilitación del ajuste de textura cambia la forma en que el sistema rasteriza los polígonos con \_ textura. Para obtener más información, vea [Ajuste de textura (Direct3D 9).](texture-wrapping.md)

Al habilitar el ajuste de textura de forma eficaz, las coordenadas de textura fuera del intervalo \[ 0.0, 1.0 no son válidas y el comportamiento para rasterizar estas coordenadas de textura delinquentes no está definido en este \] caso. Cuando el ajuste de textura está habilitado, no se usan los modos de direccionamiento de textura. Debe tener cuidado de que la aplicación no especifique coordenadas de textura inferiores a 0,0 o superiores a 1,0 cuando el ajuste de textura esté habilitado.

## <a name="setting-the-addressing-mode"></a>Establecer el modo de direccionamiento

Puede establecer modos de direccionamiento de textura para fases de textura individuales llamando al método [**IDirect3DDevice9::SetSamplerState.**](/windows/desktop/api) Especifique el identificador de fase de textura deseado en el *parámetro Sampler.* Establezca el parámetro *Type* en los valores D3DSAMP \_ ADDRESSU, D3DSAMP ADDRESSV o D3DSAMP ADDRESSW para actualizar los modos de direccionamiento \_ \_ u, v o w individualmente. El *parámetro Value* determina qué modo se establece. Puede ser cualquier miembro del [**tipo enumerado D3DTEXTUREADDRESS.**](./d3dtextureaddress.md) Para recuperar el modo de dirección de textura actual para una fase de textura, llame a los miembros [**IDirect3DDevice9::GetSamplerState**](/windows/desktop/api), mediante los miembros \_ D3DSAMP ADDRESSU, D3DSAMP ADDRESSV o D3DSAMP ADDRESSW de la enumeración \_ \_ [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para identificar el modo de dirección sobre el que desea obtener información.

## <a name="device-limitations"></a>Limitaciones del dispositivo

Aunque el sistema generalmente permite coordenadas de textura fuera del intervalo de 0,0 y 1,0, ambos inclusive, las limitaciones de hardware suelen afectar a lo lejos que pueden estar las coordenadas de textura de ese intervalo. Un dispositivo de representación comunica este límite en el **miembro MaxTextureRepeat** de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) al recuperar las funcionalidades del dispositivo. El valor de este miembro describe el intervalo completo de coordenadas de textura permitido por el dispositivo. Por ejemplo, si este valor es 128, las coordenadas de textura de entrada deben mantenerse en el intervalo de -128.0 a +128.0. Pasar vértices con coordenadas de textura fuera de este intervalo no es válido. La misma restricción se aplica a las coordenadas de textura generadas como resultado de la generación automática de coordenadas de textura y las transformaciones de coordenadas de textura.

La interpretación **de MaxTextureRepeat** también se ve afectada por el bit de funcionalidad D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE. Cuando se establece este bit, el valor del **miembro MaxTextureRepeat** se usa exactamente como se describe. Sin embargo, cuando D3DPTEXTURECAPS TEXREPEATNOTSCALEDBYSIZE no está establecido, las limitaciones de repetición de textura dependen del tamaño de la textura indizada por las coordenadas de \_ textura. En este caso, **MaxTextureRepeat** se debe escalar por el tamaño de textura actual en el nivel de detalle más grande para calcular el intervalo de coordenadas de textura válido. Por ejemplo, dada una dimensión de textura de 32 y **MaxTextureRepeat** de 512, el intervalo de coordenadas de textura válido real es 512/32 = 16, por lo que las coordenadas de textura de este dispositivo deben estar dentro del intervalo de -16.0 a +16.0.

En los temas siguientes se incluye información adicional sobre los modos de direccionamiento de textura.

-   [Modo de dirección de textura encapsulada (Direct3D 9)](wrap-texture-address-mode.md)
-   [Modo de dirección de textura de reflejo (Direct3D 9)](mirror-texture-address-mode.md)
-   [Modo de dirección de textura de fijación (Direct3D 9)](clamp-texture-address-mode.md)
-   [Modo de dirección de textura de color de borde (Direct3D 9)](border-color-texture-address-mode.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
