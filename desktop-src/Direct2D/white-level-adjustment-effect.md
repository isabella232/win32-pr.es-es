---
title: Efecto de mapa de tono blanco
description: Este efecto permite que el nivel de blanco de una imagen se escale linealmente. Esto es especialmente útil cuando se convierte entre el espacio de luminancia al que se hace referencia y el espacio de luminancia que se hace referencia a la escena, o viceversa.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 70a38f37f5a5461b968099bebe4be120a727c053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996630"
---
# <a name="white-level-adjustment-effect"></a>Efecto de ajuste de nivel de blanco

Este efecto permite que el nivel de blanco de una imagen se escale linealmente. Esto es especialmente útil cuando se convierte entre el espacio de luminancia al que se hace referencia y el espacio de luminancia que se hace referencia a la escena, o viceversa.

Las propiedades de este efecto se identifican mediante la [**enumeración D2D1_WHITELEVELADJUSTMENT_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)y el CLSID se **CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Propiedades del efecto

| Enumeración de índice y nombre para mostrar | Tipo y valor predeterminado | Descripción |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | Nivel blanco de la imagen de entrada, en Nits. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | Nivel blanco de la imagen de salida, en Nits. |

## <a name="remarks"></a>Observaciones
Este efecto está pensado para combinarse con el [efecto de mapa de tono de HDR](hdr-tone-map-effect.md) para que pueda representar imágenes HDR en Direct2D con la administración de color y la asignación de tono adecuadas. Vea los **comentarios** de ese tema para obtener más detalles. Los efectos están dirigidos a cualquier marco que quiera proporcionar una mejor experiencia de visualización de imágenes HDR que controle todos los formatos de imagen HDR de Windows y se adapta a las capacidades de la presentación (ya sea HDR o WCG/SDR).

En Windows, se supone que todo el contenido de SDR/WCG está en un espacio de luminancia al que se hace referencia, lo que significa que el nivel de blanco del contenido debe escalarse hasta el nivel de blanco de la pantalla antes de que se presente en última instancia. Sin embargo, no siempre es responsabilidad de la aplicación hacerlo. Por el contrario, se supone que el contenido de HDR está en un espacio de luminancia, lo que significa que, en última instancia, no se debe escalar para que coincida con el nivel de blanco de la pantalla. Dicho esto, es posible que la aplicación tenga que realizar el escalado en algunas circunstancias al representar contenido HDR para asegurarse de que es el resultado neto.

Cuando el escritorio de Windows está en modo SDR o WCG, el escritorio se compone de un espacio de luminancia al que se hace referencia. Pero si el escritorio de Windows está en modo HDR, la composición del escritorio se produce en el espacio de luminancia que se conoce en la escena. Dicho esto, el Administrador de ventanas de escritorio (DWM) realiza ajustes de luminancia (a menudo denominados SDRBoost) para las superficies de composición de 8 bits y que simplifica la aplicación para ese caso. Aun así, el aumento automático significa que el rol de la aplicación en la conversión de un espacio de luminancia a otro depende del formato de composición que usa la aplicación para presentar su contenido.

En la tabla siguiente se describen los casos en los que la aplicación debe y no debe realizar un ajuste de nivel blanco, así como el ajuste que debe tener. En general, el ajuste depende de tres factores.

1. ColorSpace de contenido de entrada. Si el contenido de entrada contiene valores de luminancia de intervalo dinámico alto (HDR) o no. El contenido de WCG se comporta igual que SDR para el comportamiento de luminancia.
2. Formato de composición. Formato de píxel de la superficie de destino que se presenta a DWM &mdash; , por ejemplo, una [cadena de intercambio](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) o una superficie de [composición](/uwp/api/Windows.UI.Composition.ICompositionSurface). Al representar mediante Direct2D, es **UINT8** o **FP16**.
3. Modo de color avanzado del escritorio. Si DWM se está ejecutando en el modo SDR, WCG o HDR para la pantalla actual. Obtenga esta información a través de [**DXGI_OUTPUT_DESC1:: ColorSpace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) o [**AdvancedColorInfo. CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind).

En función de estos tres factores, debe establecer los valores adecuados para las `InputWhiteLevel` `OutputWhiteLevel` propiedades y.

|Contenido de entrada|Formato de composición|Modo de color avanzado|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|Any|N/D|N/D|
|SDR/WCG|**FP16**|SDR/WCG|N/D|N/D|
|SDR/WCG|**FP16**|HDR|SDRWhite|80|
|HDR|Any|SDR/WCG|80|[**DXGI_OUTPUT_DESC1:: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|HDR|**UINT8**|HDR|80|SDRWhite|
|HDR|**FP16**|HDR|N/D|N/D|

En la tabla, el valor 80 es el nivel blanco de referencia, en Nits, para el contenido sRGB o scRGB. Para ello, puede usar la constante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants), que se define en `d2d1effects_2.h` . El valor `SDRWhite` es el número de Nits que la pantalla debe utilizar para mostrar el contenido de sRGB blanco. Puede recuperar este valor mediante el acceso a la propiedad [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) . El valor N/A significa que el ajuste de nivel blanco no se utiliza en este escenario; puede quitar el efecto del gráfico o establecer valores para una operación no operativa.

Tenga en cuenta que, en los casos en los que la aplicación no necesita un ajuste de nivel blanco, el DWM o la pantalla pueden controlar la conversión del espacio de luminancia al que se hace referencia en la escena.

- En el modo SDR/WCG, la conversión se produce después de la composición de DWM y se aplica a todo el contenido que se muestra en esa pantalla. La presentación realiza esta conversión de forma implícita.
- En el modo HDR, el DWM realiza automáticamente la conversión antes de la composición, siempre que la superficie de composición de la aplicación sea SDR.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Windows 10, versión 1809 (10,0; Compilación 17763) \[ aplicaciones para UWP de aplicaciones de escritorio \|\] |
| Encabezado | d2d1effects \_ 2. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Enumeración D2D1_WHITELEVELADJUSTMENT_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
