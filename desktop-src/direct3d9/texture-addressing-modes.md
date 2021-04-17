---
description: La aplicación Direct3D puede asignar coordenadas de textura a cualquier vértice de cualquier primitiva.
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: Modos de direccionamiento de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ebad5fdb141c41c43c651a2188640d7a6b764e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705255"
---
# <a name="texture-addressing-modes-direct3d-9"></a>Modos de direccionamiento de textura (Direct3D 9)

La aplicación Direct3D puede asignar coordenadas de textura a cualquier vértice de cualquier primitiva. Para obtener más información, consulte [coordenadas de textura (Direct3D 9)](texture-coordinates.md). Normalmente, las coordenadas de textura de u y v que se asignan a un vértice están en el intervalo de 0,0 a 1,0, ambos incluidos. Sin embargo, si se asignan coordenadas de textura fuera de ese intervalo, se pueden crear determinados efectos de textura especiales.

Puede controlar lo que hace Direct3D con las coordenadas de textura que se encuentran fuera del \[ intervalo 0,0 y 1,0 \] estableciendo el modo de direccionamiento de textura. Por ejemplo, puede hacer que la aplicación establezca el modo de direccionamiento de textura para que una textura se ponga en mosaico en un primitivo.

Direct3D permite que las aplicaciones realicen el ajuste de textura. Es importante tener en cuenta que establecer el modo de direccionamiento de textura en D3DTADDRESS \_ Wrap no es lo mismo que realizar el ajuste de textura. Al establecer el modo de direccionamiento de textura en D3DTADDRESS \_ Wrap, se aplican varias copias de la textura de origen al primitivo actual y, al habilitar el ajuste de textura, se cambia el modo en que el sistema rasteriza los polígonos con textura. Para obtener más información, vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).

La habilitación del ajuste de textura eficazmente hace que las coordenadas de textura fuera del \[ intervalo 0,0, 1,0 \] no sean válidas y el comportamiento de la rasterización de dichas coordenadas de textura aquel no está definido en este caso. Cuando está habilitado el ajuste de textura, no se usan los modos de direccionamiento de textura. Tenga cuidado de que la aplicación no especifique coordenadas de textura inferiores a 0,0 o superior a 1,0 cuando se habilita el ajuste de textura.

## <a name="setting-the-addressing-mode"></a>Establecer el modo de direccionamiento

Puede establecer modos de direccionamiento de texturas para fases de textura individuales llamando al método [**IDirect3DDevice9:: SetSamplerState**](/windows/desktop/api) . Especifique el identificador de la fase de textura deseado en el parámetro de *muestra* . Establezca el parámetro de *tipo* en D3DSAMP \_ ADDRESSU, D3DSAMP \_ ADDRESSV o D3DSAMP \_ ADDRESSW para actualizar los modos u-, v-o w-Addressing de forma individual. El parámetro *Value* determina el modo que se va a establecer. Puede ser cualquier miembro del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) . Para recuperar el modo de dirección de textura actual para una fase de textura, llame a [**IDirect3DDevice9:: GetSamplerState**](/windows/desktop/api), usando los \_ miembros D3DSAMP ADDRESSU, D3DSAMP \_ ADDRESSV o D3DSAMP \_ ADDRESSW de la enumeración [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para identificar el modo de dirección sobre el que desea obtener información.

## <a name="device-limitations"></a>Limitaciones del dispositivo

Aunque el sistema suele permitir las coordenadas de textura fuera del intervalo de 0,0 y 1,0, ambas inclusive, las limitaciones de hardware suelen afectar a la diferencia entre las coordenadas de textura del intervalo. Un dispositivo de representación comunica este límite en el miembro **MaxTextureRepeat** de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) cuando se recuperan las funcionalidades del dispositivo. El valor de este miembro describe el intervalo completo de coordenadas de textura permitido por el dispositivo. Por ejemplo, si este valor es 128, las coordenadas de textura de entrada deben mantenerse en el intervalo de-128,0 a + 128,0. Pasar los vértices con coordenadas de textura fuera de este intervalo no es válido. La misma restricción se aplica a las coordenadas de textura generadas como resultado de la generación automática de coordenadas de textura y las transformaciones de coordenadas de textura.

La interpretación de **MaxTextureRepeat** también se ve afectada por el \_ bit de capacidad TEXREPEATNOTSCALEDBYSIZE de D3DPTEXTURECAPS. Cuando se establece este bit, el valor del miembro **MaxTextureRepeat** se usa exactamente como se describe. Sin embargo, si \_ no se establece D3DPTEXTURECAPS TEXREPEATNOTSCALEDBYSIZE, las limitaciones de repetición de texturas dependen del tamaño de la textura indexada por las coordenadas de textura. En este caso, **MaxTextureRepeat** se debe escalar según el tamaño de la textura actual en el nivel de detalle más grande para calcular el intervalo de coordenadas de textura válido. Por ejemplo, dada una dimensión de textura de 32 y **MaxTextureRepeat** de 512, el intervalo de coordenadas de textura válido real es 512/32 = 16, por lo que las coordenadas de textura para este dispositivo deben estar dentro del intervalo de-16,0 a + 16,0.

En los temas siguientes se incluye información adicional acerca de los modos de direccionamiento de textura.

-   [Ajustar el modo de dirección de textura (Direct3D 9)](wrap-texture-address-mode.md)
-   [Modo de dirección de textura de reflejo (Direct3D 9)](mirror-texture-address-mode.md)
-   [Modo de dirección de textura de abrazadera (Direct3D 9)](clamp-texture-address-mode.md)
-   [Modo de dirección de textura de color de borde (Direct3D 9)](border-color-texture-address-mode.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la texturización](basic-texturing-concepts.md)
</dt> </dl>

 

 
