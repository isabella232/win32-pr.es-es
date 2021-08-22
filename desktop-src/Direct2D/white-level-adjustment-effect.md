---
title: Efecto de mapa de tono blanco
description: Este efecto permite escalar linealmente el nivel blanco de una imagen. Esto resulta especialmente útil cuando se convierte entre el espacio de luminosidad al que se hace referencia para la presentación y el espacio de luminosidad al que se hace referencia en la escena, o viceversa.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 646ad47ad671618f29d1691878de93b5e5141855787c53fdad44025487835ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292635"
---
# <a name="white-level-adjustment-effect"></a>Efecto de ajuste de nivel blanco

Este efecto permite escalar linealmente el nivel blanco de una imagen. Esto resulta especialmente útil cuando se convierte entre el espacio de luminosidad al que se hace referencia para la presentación y el espacio de luminosidad al que se hace referencia en la escena, o viceversa.

Las propiedades de este efecto se identifican mediante la enumeración [**D2D1_WHITELEVELADJUSTMENT_PROP ,**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)y el CLSID **se CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Propiedades de efecto

| Enumeración de nombre para mostrar e índice | Tipo y valor predeterminado | Descripción |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | Nivel blanco de la imagen de entrada, en nits. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | Nivel blanco de la imagen de salida, en nits. |

## <a name="remarks"></a>Comentarios
Este efecto está pensado para combinarse con el efecto de mapa de tono HDR para permitirle representar imágenes [HDR](hdr-tone-map-effect.md) en Direct2D con una correcta administración de color y asignación de tono. Vea los comentarios de **ese tema** para obtener más detalles. Los efectos están dirigidos a cualquier marco que quiera proporcionar la mejor experiencia de visualización de imágenes HDR en su clase que controle todos los formatos de imagen de Windows HDR y se adapte a las funcionalidades de la pantalla (ya sea HDR o WCG/SDR).

En Windows, se supone que todo el contenido de SDR/WCG está en un espacio de luminosidad al que se hace referencia para mostrar, lo que significa que el nivel blanco del contenido se debe escalar verticalmente hasta el nivel de blanco de la pantalla antes de que se presente en última instancia. Sin embargo, no siempre es responsabilidad de la aplicación hacerlo. En cambio, se supone que el contenido HDR está en un espacio de luminosidad al que se hace referencia a la escena, lo que significa que no se debe escalar en última instancia para que coincida con el nivel de blanco de la pantalla. Dicho esto, es posible que la aplicación tenga que realizar el escalado en algunas circunstancias al representar contenido HDR para asegurarse de que este es el resultado neto.

Cuando el Windows está en modo SDR o WCG, el escritorio se compone de un espacio de luminosidad al que se hace referencia para mostrar. Pero si el escritorio Windows está en modo HDR, la composición del escritorio se produce en el espacio de luminosidad al que se hace referencia en la escena. Dicho esto, el propio Administrador de ventanas de escritorio (DWM) realiza ajustes de luminosidad (a menudo denominados SDRBoost) para superficies de composición de 8 bits, lo que simplifica la aplicación para ese caso. Aun así, la potenciación automática significa que el rol de la aplicación en la conversión de un espacio de luminosidad a otro depende del formato de composición que la aplicación usa para presentar su contenido.

En la tabla siguiente se describen los casos en los que la aplicación debe y no debe realizar un ajuste de nivel de blanco, así como cuál debe ser ese ajuste. En general, el ajuste depende de tres factores.

1. Espacio de colores de contenido de entrada. Si el contenido de entrada contiene valores de luminosidad de alto rango dinámico (HDR) o no. El contenido de WCG se comporta igual que SDR para el comportamiento de luminosidad.
2. Formato de composición. Formato de píxel de la superficie de destino que se presenta al DWM, por ejemplo, una cadena de &mdash; [intercambio](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) o una superficie [de composición](/uwp/api/Windows.UI.Composition.ICompositionSurface). Al representar mediante Direct2D, se trata de **UINT8** o **FP16.**
3. Modo de color avanzado de escritorio. Si el DWM se ejecuta en modo SDR, WCG o HDR para la pantalla actual. Obtenga esta información [**mediante DXGI_OUTPUT_DESC1::ColorSpace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) o [**AdvancedColorInfo.CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind).

En función de estos tres factores, debe establecer los valores adecuados para las `InputWhiteLevel` propiedades `OutputWhiteLevel` y .

|Contenido de entrada|Formato de composición|Modo de color avanzado|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|Any|N/D|N/D|
|SDR/WCG|**FP16**|SDR/WCG|N/D|N/D|
|SDR/WCG|**FP16**|Hdr|SDRWhite|80|
|Hdr|Any|SDR/WCG|80|[**DXGI_OUTPUT_DESC1::MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|Hdr|**UINT8**|Hdr|80|SDRWhite|
|Hdr|**FP16**|Hdr|N/D|N/D|

En la tabla, el valor 80 es el nivel blanco de referencia, en nits, para el contenido de sRGB o scRGB. Para ello, puede usar la constante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants), que se define en `d2d1effects_2.h` . El valor es el número de nits que debe usar la pantalla `SDRWhite` para mostrar contenido sRGB blanco. Puede recuperar este valor accediendo a [**la propiedad AdvancedColorInfo.SdrWhiteLevelInNits.**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) El valor N/A significa que no se usa el ajuste de nivel de blanco en este escenario; puede quitar el efecto del gráfico o establecer valores para una operación no op.

Tenga en cuenta que, en los casos en los que la aplicación no necesita un ajuste de nivel de blanco, el DWM o la pantalla pueden controlar la conversión del espacio de luminosidad al que se hace referencia a la escena.

- En el modo SDR/WCG, la conversión se produce después de la composición de DWM y se aplica a todo el contenido presentado a esa pantalla. La pantalla realiza implícitamente esta conversión.
- En el modo HDR, el DWM realiza automáticamente la conversión antes de la composición, siempre y cuando la superficie de composición de la aplicación sea SDR.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo compatible | Windows 10, versión 1809 (10.0; Compilación de aplicaciones de escritorio UWP 17763) \[ \|\] |
| Header | d2d1effects \_ 2.h |
| Biblioteca | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_WHITELEVELADJUSTMENT_PROP enumeración](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
