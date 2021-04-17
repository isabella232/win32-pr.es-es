---
description: Define los efectos de intercambio.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: Enumeración D3DSWAPEFFECT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41327dc66f676c6f498ad0cefb23202bedc13112
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717694"
---
# <a name="d3dswapeffect-enumeration"></a>Enumeración D3DSWAPEFFECT

Define los efectos de intercambio.

## <a name="syntax"></a>Sintaxis

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**\_Descartar D3DSWAPEFFECT**
</dt> <dd>

Cuando se crea una cadena de intercambio con un efecto de intercambio de D3DSWAPEFFECT \_ Flip o D3DSWAPEFFECT \_ Copy, el tiempo de ejecución garantiza que una operación [**IDirect3DDevice9::P reenviar**](/windows/desktop/api) no afectará al contenido de ninguno de los búferes de reserva. Desafortunadamente, el cumplimiento de esta garantía puede implicar una gran cantidad de memoria de vídeo o sobrecargas de procesamiento, especialmente cuando se implementa semántica de volteo para una cadena de intercambio en ventanas o una semántica de copia para una cadena de intercambio de pantalla completa. Una aplicación puede usar el \_ efecto de intercambio descartar D3DSWAPEFFECT para evitar estas sobrecargas y habilitar el controlador de pantalla para seleccionar la técnica de presentación más eficaz para la cadena de intercambio. Este es también el único efecto de intercambio que se puede usar al especificar un valor distinto de D3DMULTISAMPLE \_ None para el miembro MultiSampleType de [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md).

Al igual que una cadena de intercambio que usa D3DSWAPEFFECT \_ Flip, una cadena de intercambio que usa D3DSWAPEFFECT \_ discard puede incluir más de un búfer de reserva, cualquiera de los cuales se puede acceder mediante [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer). La cadena de intercambio se considera mejor como una cola en la que 0 siempre indexa el búfer de reserva que se mostrará en la siguiente operación Present y desde donde se descartan los búferes cuando se han mostrado.

Una aplicación que usa este efecto de intercambio no puede realizar suposiciones sobre el contenido de un búfer de reserva descartado y, por tanto, debe actualizar un búfer de reserva completo antes de invocar una operación present que lo mostraría. Aunque esto no se aplica, la versión de depuración del tiempo de ejecución sobrescribirá el contenido de los búferes de reserva descartados con datos aleatorios para que los desarrolladores puedan comprobar que sus aplicaciones están actualizando correctamente todas las superficies del búfer de reserva.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ Flip**
</dt> <dd>

La cadena de intercambio podría incluir varios búferes de reserva y se prevé mejor como una cola circular que incluye el búfer frontal. Dentro de esta cola, los búferes de reserva siempre se numeran secuencialmente de 0 a (n-1), donde n es el número de búferes de reserva, de modo que 0 denota el búfer presentado menos recientemente. Cuando se invoca Present, la cola se "gira" para que el búfer frontal se convierta en búfer (n-1), mientras que el búfer de reserva 0 se convierte en el nuevo búfer frontal.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**Copia de D3DSWAPEFFECT \_**
</dt> <dd>

Este efecto de intercambio solo se puede especificar para una cadena de intercambio que comprenda un solo búfer de reserva. Si la cadena de intercambio está en la ventana o en pantalla completa, el tiempo de ejecución garantizará la semántica implícita de una operación de presentación basada en copia, es decir, que la operación deja el contenido del búfer de reserva sin modificar, en lugar de reemplazarlo por el contenido del búfer de front-end como una operación present basada en volteo.

En el caso de una cadena de intercambio de pantalla completa, el motor en tiempo de ejecución utiliza una combinación de operaciones de volteo y operaciones de copia, que se admite si es necesario en los búferes de reserva ocultos, para llevar a cabo la operación actual. En consecuencia, la presentación se sincroniza con el retrazado vertical del adaptador de pantalla y su velocidad está restringida por el intervalo de presentación elegido. Una cadena de intercambio especificada con la \_ marca inmediata del intervalo D3DPRESENT \_ es la única excepción. (Consulte la descripción del miembro **PresentationIntervals** de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) ). En este caso, una operación present copia el contenido del búfer de reserva directamente en el búfer frontal sin esperar a que se vuelva a realizar el seguimiento vertical.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**Superposición D3DSWAPEFFECT \_**
</dt> <dd>

Use un área dedicada de memoria de vídeo que se puede superponer en la superficie principal. No se realiza ninguna copia cuando se muestra la superposición. La operación de superposición se realiza en el hardware, sin modificar los datos en la superficie principal.

|                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> La \_ superposición D3DSWAPEFFECT solo está disponible en Direct3D9Ex que se ejecuta en Windows 7 (o en el sistema operativo actual).<br/> |

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Designa cuando una aplicación está adoptando el modo Flip, durante el cual se pasa el marco de una aplicación en lugar de copiarse en el Administrador de ventanas de escritorio (DWM) para la composición cuando la aplicación se presenta en modo de ventana. El modo de volteo permite que una aplicación use de forma más eficaz el ancho de banda de memoria, además de permitir que una aplicación aproveche las estadísticas presentes en pantalla completa. El modo de volteo no afecta al comportamiento de la pantalla completa.

> [!Note]  
> Si crea una cadena de intercambio con D3DSWAPEFFECT \_ FLIPEX, no puede invalidar el miembro **hDeviceWindow** de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) cuando presente un nuevo fotograma para su presentación. Es decir, debe pasar **null** al parámetro *hDestWindowOverride* de [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) para indicar al Runtime que use el miembro **hDeviceWindow** de **D3DPRESENT \_ Parameters** para la presentación.

|                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> D3DSWAPEFFECT \_ FLIPEX solo está disponible en Direct3D9Ex que se ejecuta en Windows 7 (o en el sistema operativo actual).<br/> |

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El estado del búfer de reserva después de una llamada a present está bien definido por cada uno de estos efectos de intercambio, y si el dispositivo Direct3D se creó con una cadena de intercambio de pantalla completa o si una cadena de intercambio en ventanas no tiene ningún efecto en este estado. En concreto, el \_ efecto D3DSWAPEFFECT Flip swap funciona de la misma forma que la ventana o la pantalla completa, y el tiempo de ejecución de Direct3D lo garantiza mediante la creación de búferes adicionales. Como resultado, se recomienda que las aplicaciones usen D3DSWAPEFFECT \_ discard siempre que sea posible para evitar estas penalizaciones. Esto se debe a que este efecto de intercambio siempre será el más eficaz en lo que se refiere al consumo de memoria y al rendimiento.

Las aplicaciones que usan D3DSWAPEFFECT \_ Flip o D3DSWAPEFFECT \_ discard no deben esperar que Alpha de destino de pantalla completa funcione. Esto significa que el estado de representación de D3DRS \_ DESTBLEND no funcionará según lo esperado porque las cadenas de intercambio de pantalla completa con estos efectos de intercambio no tienen un formato de píxel explícito desde el punto de vista del controlador. El controlador deduce que debe tomar el formato de presentación, que no tiene un canal alfa. Para solucionar este fin, realice los pasos siguientes:

-   Usar copia de D3DSWAPEFFECT \_ .
-   Active la \_ marca D3DCAPS3 alpha \_ Fullscreen \_ Flip \_ o \_ discard en el miembro Caps3 de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Esta marca indica si el controlador puede realizar la mezcla alfa cuando \_ se usa D3DSWAPEFFECT Flip o D3DSWAPEFFECT \_ discard.
-   Las aplicaciones que usan el efecto de intercambio de modo de volteo (D3DSWAPEFFECT \_ FLIPEX) deben llamar a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) después de cambiar el tamaño de una ventana o cambiar la región para asegurarse de que se actualiza el contenido para mostrar.

Una ventana invisible no puede recibir eventos de modo usuario. Además, una ventana invisible de pantalla completa interfiere con la presentación de la ventana de modo de ventana de otra aplicación. Por lo tanto, cada aplicación debe asegurarse de que una ventana de dispositivo esté visible cuando un intercambio se presente en el modo de pantalla completa.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |

## <a name="see-also"></a>Vea también

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
