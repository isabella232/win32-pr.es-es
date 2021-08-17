---
description: Define efectos de intercambio.
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
ms.openlocfilehash: db869d277c98c3e99bd2bbc54f7e40ac86770f647e8258ee5718a96eaedec18c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096620"
---
# <a name="d3dswapeffect-enumeration"></a>Enumeración D3DSWAPEFFECT

Define efectos de intercambio.

## <a name="syntax"></a>Syntax

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

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ DISCARD**
</dt> <dd>

Cuando se crea una cadena de intercambio con un efecto de intercambio de D3DSWAPEFFECT FLIP o D3DSWAPEFFECT COPY, el tiempo de ejecución garantizará que una operación \_ \_ [**IDirect3DDevice9::P resent**](/windows/desktop/api) no afectará al contenido de ninguno de los búferes de reserva. Desafortunadamente, cumplir esta garantía puede implicar importantes sobrecargas de procesamiento o memoria de vídeo, especialmente al implementar semántica de volteo para una cadena de intercambio en ventanas o semántica de copia para una cadena de intercambio de pantalla completa. Una aplicación puede usar el efecto de intercambio D3DSWAPEFFECT DISCARD para evitar estas sobrecargas y permitir que el controlador de pantalla seleccione la técnica de presentación más eficaz para la cadena \_ de intercambio. Este es también el único efecto de intercambio que se puede usar al especificar un valor distinto de D3DMULTISAMPLE NONE para el \_ miembro MultiSampleType de [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

Al igual que una cadena de intercambio que usa D3DSWAPEFFECT FLIP, una cadena de intercambio que usa D3DSWAPEFFECT DISCARD puede incluir más de un búfer de reserva, al que se puede acceder mediante \_ \_ [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer). La cadena de intercambio se considera mejor como una cola en la que 0 siempre indexa el búfer de reserva que se mostrará en la siguiente operación Present y de la que se descartan los búferes cuando se hayan mostrado.

Una aplicación que usa este efecto de intercambio no puede realizar ninguna suposición sobre el contenido de un búfer de reserva descartado y, por tanto, debe actualizar un búfer de reserva completo antes de invocar una operación Present que lo mostraría. Aunque esto no se aplica, la versión de depuración del tiempo de ejecución sobrescribirá el contenido de los búferes de reserva descartados con datos aleatorios para permitir a los desarrolladores comprobar que sus aplicaciones actualizan correctamente todas las superficies del búfer de reserva.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**
</dt> <dd>

La cadena de intercambio puede incluir varios búferes de reserva y se considera mejor como una cola circular que incluye el búfer frontal. Dentro de esta cola, los búferes de reserva siempre se numeran secuencialmente de 0 a (n - 1), donde n es el número de búferes de reserva, de modo que 0 denota el búfer presentado menos recientemente. Cuando se invoca Present, la cola se "gira" para que el búfer front-buffer se convierta en búfer de reserva (n - 1), mientras que el búfer de reserva 0 se convierte en el nuevo búfer front-buffer.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**COPIA D3DSWAPEFFECT \_**
</dt> <dd>

Este efecto de intercambio solo se puede especificar para una cadena de intercambio que consta de un único búfer de reserva. Tanto si la cadena de intercambio es de ventana como de pantalla completa, el tiempo de ejecución garantizará la semántica implícita por una operación Present basada en copia, es decir, que la operación deje el contenido del búfer de reserva sin cambios, en lugar de reemplazarlo por el contenido del búfer frontal como lo haría una operación Present basada en volteo.

Para una cadena de intercambio de pantalla completa, el tiempo de ejecución usa una combinación de operaciones de volteo y operaciones de copia, admitidas si es necesario por búferes de reserva ocultos, para realizar la operación Present. En consecuencia, la presentación se sincroniza con el retroceso vertical del adaptador de pantalla y su velocidad está limitada por el intervalo de presentación elegido. Una cadena de intercambio especificada con la marca D3DPRESENT \_ INTERVAL IMMEDIATE es la única \_ excepción. (Consulte la descripción del miembro **PresentationIntervals** de la [**estructura PARAMETERS D3DPRESENT). \_**](d3dpresent-parameters.md) En este caso, una operación Present copia el contenido del búfer de reserva directamente en el búfer front-in sin esperar a que se vuelva a rastrear verticalmente.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**SUPERPOSICIÓN D3DSWAPEFFECT \_**
</dt> <dd>

Use un área dedicada de memoria de vídeo que se pueda superponer en la superficie principal. No se realiza ninguna copia cuando se muestra la superposición. La operación de superposición se realiza en hardware, sin modificar los datos de la superficie principal.

Diferencias entre Direct3D 9 y Direct3D 9Ex:

- D3DSWAPEFFECT OVERLAY solo está disponible en Direct3D9Ex que se ejecuta \_ Windows 7 (o más sistema operativo actual).

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Designa cuándo una aplicación adopta el modo de volteo, durante el cual se pasa el marco de una aplicación en lugar de copiarse en Administrador de ventanas de escritorio(DWM) para la composición cuando la aplicación se presenta en modo de ventana. El modo de volteo permite que una aplicación use de forma más eficaz el ancho de banda de memoria, así como permitir que una aplicación aproveche las estadísticas de pantalla completa presente. El modo de volteo no afecta al comportamiento de pantalla completa.

> [!Note]  
> Si crea una cadena de intercambio con D3DSWAPEFFECT FLIPEX, no puede invalidar el miembro hDeviceWindow de la estructura \_ [**PARAMETERS D3DPRESENT \_**](d3dpresent-parameters.md) al presentar un nuevo marco para su  presentación. Es decir, debe pasar **NULL** al parámetro *hDestWindowOverride* de [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) para indicar al tiempo de ejecución que use el miembro **hDeviceWindow** de **D3DPRESENT \_ PARAMETERS** para la presentación.

Diferencias entre Direct3D 9 y Direct3D 9Ex:

- D3DSWAPEFFECT FLIPEX solo está disponible en Direct3D9Ex que se ejecuta \_ Windows 7 (o más sistema operativo actual).

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El estado del búfer de reserva después de una llamada a Present está bien definido por cada uno de estos efectos de intercambio, y si el dispositivo Direct3D se creó con una cadena de intercambio de pantalla completa o una cadena de intercambio en ventanas no tiene ningún efecto sobre este estado. En concreto, el efecto de intercambio FLIP D3DSWAPEFFECT funciona de la misma manera tanto en ventanas como en pantalla completa, y el tiempo de ejecución de Direct3D lo garantiza mediante la creación de búferes \_ adicionales. Como resultado, se recomienda que las aplicaciones usen D3DSWAPEFFECT DISCARD siempre que sea \_ posible para evitar tales penalizaciones. Esto se debe a que este efecto de intercambio siempre será el más eficaz en términos de consumo y rendimiento de memoria.

Las aplicaciones que usan D3DSWAPEFFECT FLIP o \_ D3DSWAPEFFECT DISCARD no deben esperar que el destino de pantalla completa \_ alfa funcione. Esto significa que el estado de representación D3DRS DESTBLEND no funcionará según lo previsto porque las cadenas de intercambio de pantalla completa con estos efectos de intercambio no tienen un formato de píxel explícito desde el punto de vista del \_ controlador. El controlador deduce que deben tomar el formato de presentación, que no tiene un canal alfa. Para evitar esto, siga estos pasos:

-   Use D3DSWAPEFFECT \_ COPY.
-   Compruebe la marca D3DCAPS3 ALPHA FULLSCREEN FLIP OR DISCARD en el \_ \_ miembro \_ \_ \_ Caps3 de la [**estructura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Esta marca indica si el controlador puede realizar la combinación alfa cuando se usa D3DSWAPEFFECT FLIP o \_ D3DSWAPEFFECT \_ DISCARD.
-   Las aplicaciones que usan el efecto de intercambio de modo de volteo (D3DSWAPEFFECT FLIPEX) deben llamar a PresentEx después de cambiar el tamaño de una ventana o una región para asegurarse de que se actualiza el contenido \_ para mostrar. [](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)

Una ventana invisible no puede recibir eventos en modo de usuario; Además, una ventana de pantalla completa invisible interferirá con la presentación de la ventana en modo de ventana de otras aplicaciones. Por lo tanto, cada aplicación debe asegurarse de que una ventana del dispositivo está visible cuando se presenta una cadena de intercambio en modo de pantalla completa.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |

## <a name="see-also"></a>Consulte también

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
