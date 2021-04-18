---
description: Un efecto de Microsoft DirectX permite la integración de sombreadores de vértices y píxeles con estado de canalización para representar objetos. Los efectos son el siguiente paso lógico en la combinación de sombreadores para producir condiciones de representación únicas.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Efectos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48d2ff5548dff29ede4b360bd2c319f85fafa3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714735"
---
# <a name="effects-direct3d-9"></a>Efectos (Direct3D 9)

Un efecto de Microsoft DirectX permite la integración de sombreadores de vértices y píxeles con estado de canalización para representar objetos. Los efectos son el siguiente paso lógico en la combinación de sombreadores para producir condiciones de representación únicas.

Los efectos también proporcionan una manera cómoda de escribir sombreadores para diferentes versiones de hardware. Dado que las distintas tarjetas de vídeo admiten distintas funcionalidades, una aplicación puede escribir varias técnicas que se ejecutarán en una variedad de dispositivos. De este modo, si la aplicación se está ejecutando en el hardware más reciente y más reciente, la aplicación puede ejecutar la técnica de efectos más sofisticada. Por otro lado, las técnicas de efectos menos sofisticadas se pueden elegir automáticamente para ejecutarse en hardware menos costoso o menos compatible.

Un efecto puede reemplazar el procesamiento de vértices y parte del procesamiento de píxeles realizado por la canalización de gráficos. Un ejemplo de un efecto que usa un sombreador de vértices y un sombreador de píxeles está en el ejemplo BasicHLSL. Puede obtener este ejemplo y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

Para obtener más información acerca de los efectos, consulte estos temas:

-   [Escribir un efecto](writing-an-effect.md)
-   [Usar un efecto](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Efectos y la canalización 3D

En el diagrama siguiente se muestra la canalización.

![diagrama de la canalización 3D](images/effects-block-diagram.png)

La canalización transforma los datos de entrada en píxeles de salida que rellenan el búfer de fotogramas. Los datos de entrada provienen de los objetos que se componen de los vértices en el espacio de objeto, o de las superficies de orden superior creadas a partir de N-patches, las revisiones de rectángulo y las revisiones de triángulo. Una vez que los datos de entrada se han teselado, la canalización realiza el procesamiento de vértices, el procesamiento primitivo y el procesamiento de píxeles antes de generar los colores finales de los píxeles.

El procesamiento de vértices y píxeles se puede realizar mediante la canalización de la función fija o se puede implementar con sombreadores programables. El estado de canalización controla la teselación de datos de entrada, el procesamiento primitivo y las salidas de datos. Todo esto se puede integrar en un efecto. Un efecto establece el estado que controla cómo funciona la canalización. Los efectos administran los sombreables programables, así como el estado de la función fija.

Los efectos pueden guardar y restaurar el estado, lo que permite que el dispositivo tenga el mismo estado que antes de ejecutar el efecto. Entre los tipos de estado que puede administrar un efecto se incluyen:

-   Estado del sombreador. Esto incluye la creación y eliminación de sombreadores, el establecimiento de constantes del sombreador, el establecimiento del estado del sombreador y la representación con sombreadores.
-   Estado de la muestra y la textura. Esto incluye la especificación de archivos de textura, la inicialización de fases de textura, la creación de objetos de muestra y el establecimiento del estado del muestrario.
-   Otro estado de canalización. Esto incluye los Estados para establecer las opciones de transformación, iluminación, materiales y representación. Pueden ser variables globales o locales. Las variables pueden establecerse por el efecto en sí o por la aplicación.

Los efectos contienen varias opciones de representación denominadas técnicas. Cada técnica encapsula las variables globales, el estado de la canalización, el estado de la muestra y la textura, y el estado del sombreador. Un solo estilo se implementa en un paso de representación. Una o más fases se pueden encapsular en una técnica. Todas las pasadas y técnicas se pueden validar para ver si el código de efecto se ejecutará en el dispositivo de hardware.

## <a name="effects-save-and-restore-state"></a>Efectos de guardar y restaurar el estado

Los efectos administran el estado. El estado de la palabra se usa muy ampliamente aquí, ya que incluye todo tipo de información que la canalización necesita para especificar las condiciones de representación. Esto incluye prácticamente todas las áreas funcionales de la canalización.

Las opciones de representación se controlan mediante técnicas y pasadas. Una aplicación representa un efecto mediante la configuración de una técnica activa y la representación de una o varias fases. Toda la representación en un efecto se realiza dentro de un par coincidente de llamadas [**Begin**](id3dxeffect--begin.md) y [**End**](id3dxeffect--end.md) . Cuando se llama a **Begin** , se crea un stateblock y se guarda el estado del dispositivo (a menos que se especifique lo contrario). Después de que una técnica representa las pasadas que la aplicación especifica que se representen, se llama a **End** para finalizar la técnica activa. El sistema de efecto responde mediante la restauración automática del estado de canalización capturado en el bloque de estado (a menos que decida deshabilitar esta funcionalidad de guardar y restaurar).

Al programar secuencias de representación de múltiples pases, cada una de las cuales requiere su propia configuración de estado, los efectos pueden reducir el mantenimiento necesario para realizar un seguimiento de los cambios de estado. Para obtener más información sobre los Estados que pueden guardarse y restaurarse por efectos, vea [Estados de efectos (Direct3D 9)](effect-states.md).

## <a name="effects-can-share-parameters"></a>Los efectos pueden compartir parámetros

Los parámetros de efecto son todas las variables no estáticas declaradas en un efecto. Esto puede incluir variables globales y anotaciones. Los parámetros de efecto se pueden compartir entre distintos efectos declarando parámetros con la palabra clave Shared y creando después el efecto con un grupo de efectos.

Los efectos clonados usan el mismo grupo de efectos que el efecto desde el que se clonan. La clonación de un efecto realiza una copia exacta de un efecto, incluidas las variables globales, las técnicas, las pasadas y las anotaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
