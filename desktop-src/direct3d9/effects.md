---
description: Un efecto de Microsoft DirectX permite la integración de sombreadores de vértices y píxeles con el estado de canalización para representar objetos. Los efectos son el siguiente paso lógico en la combinación de sombreadores para generar condiciones de representación únicas.
ms.assetid: vs|directx_sdk|~\effects.htm
title: Efectos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ed52a3a75f4b0682be4447f02ed305cf026af6aa30a59e921f4fa23f0e2211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985995"
---
# <a name="effects-direct3d-9"></a>Efectos (Direct3D 9)

Un efecto de Microsoft DirectX permite la integración de sombreadores de vértices y píxeles con el estado de canalización para representar objetos. Los efectos son el siguiente paso lógico en la combinación de sombreadores para generar condiciones de representación únicas.

Los efectos también proporcionan una manera cómoda de escribir sombreadores para distintas versiones de hardware. Dado que las distintas tarjetas de vídeo admiten funcionalidades diferentes, una aplicación puede escribir varias técnicas que se ejecutarán en una variedad de dispositivos. De este modo, si la aplicación se ejecuta en el hardware más reciente y más grande, la aplicación puede ejecutar la técnica de efecto más sofisticada. Por otro lado, las técnicas de efecto menos sofisticadas se pueden elegir automáticamente para ejecutarse en hardware menos costoso o con menos capacidad.

Un efecto puede reemplazar el procesamiento de vértices y parte del procesamiento de píxeles realizado por la canalización de gráficos. Un ejemplo de un efecto que usa un sombreador de vértices y un sombreador de píxeles se encuentra en el ejemplo BasicHLSL. Puede obtener este ejemplo y obtener información sobre él en el SDK de DirectX. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

Para obtener más información sobre los efectos, vea estos temas:

-   [Escribir un efecto](writing-an-effect.md)
-   [Usar un efecto](using-an-effect.md)

## <a name="effects-and-the-3d-pipeline"></a>Efectos y la canalización 3D

En el diagrama siguiente se muestra la canalización.

![diagrama de la canalización 3d](images/effects-block-diagram.png)

La canalización transforma los datos de entrada en píxeles de salida que rellenan el búfer de fotogramas. Los datos de entrada proceden de objetos que están hechos de vértices en el espacio de objetos o superficies de orden superior creadas a partir de N revisiones, revisiones de rectángulos y revisiones de triángulo. Una vez que se han teselado los datos de entrada, la canalización realiza el procesamiento de vértices, el procesamiento primitivo y el procesamiento de píxeles antes de generar los colores de píxel final.

La canalización de función fija puede realizar el procesamiento de vértices y píxeles, o bien se puede implementar con sombreadores programables. La teselación de datos de entrada, el procesamiento primitivo y las salidas de datos se controlan mediante el estado de la canalización. Todo esto se puede integrar en un efecto. Un efecto establece el estado que controla cómo funciona la canalización. Los efectos administran sombreadores programables, así como el estado fijo de la función.

Los efectos pueden guardar y restaurar el estado, dejando el dispositivo en el mismo estado que antes de que se ejecutara el efecto. Los tipos de estado que un efecto puede administrar incluyen:

-   Estado del sombreador. Esto incluye la creación y eliminación de sombreadores, la configuración de constantes de sombreador, la configuración del estado del sombreador y la representación con sombreadores.
-   Textura y estado del muestreador. Esto incluye la especificación de archivos de textura, la inicialización de fases de textura, la creación de objetos sampler y la configuración del estado del muestreador.
-   Otro estado de canalización. Esto incluye estados para establecer transformaciones, iluminación, materiales y opciones de representación. Pueden ser variables globales o locales. Las variables se pueden establecer por el propio efecto o por la aplicación.

Los efectos contienen varias opciones de representación denominadas técnicas. Cada técnica encapsula las variables globales, el estado de canalización, el estado de textura y muestra, y el estado del sombreador. Se implementa un estilo único en un paso de representación. Uno o varios pases se pueden encapsular en una técnica. Todas las técnicas y los pases se pueden validar para ver si el código de efecto se ejecutará en el dispositivo de hardware.

## <a name="effects-save-and-restore-state"></a>Estado de guardado y restauración de efectos

Los efectos administran el estado. La palabra state se usa de forma muy amplia aquí, ya que incluye todo tipo de información que la canalización necesita para especificar las condiciones de representación. Esto incluye casi todas las áreas funcionales de la canalización.

Las opciones de representación se controlan mediante técnicas y pases. Una aplicación representa un efecto estableciendo una técnica activa y representando uno o varios pases. Toda la representación en un efecto se realiza dentro de un par de llamadas [**Begin**](id3dxeffect--begin.md) y [**End**](id3dxeffect--end.md) correspondientes. Cuando **se** llama a Begin, se crea un bloque de estado y se guarda el estado del dispositivo (a menos que especifique lo contrario). Después de que una técnica represente los pases que la aplicación especifica que se represente, se llama a **End** para finalizar la técnica activa. El sistema de efectos responde restaurando automáticamente el estado de canalización que se capturó en el bloque de estado (a menos que decida deshabilitar esta funcionalidad de guardar y restaurar).

Al programar secuencias de representación de varios pasos, cada una de las cuales requiere su propia configuración de estado, los efectos pueden reducir el mantenimiento necesario para realizar el seguimiento de los cambios de estado. Para ver más información sobre los estados que los efectos pueden guardar y restaurar, vea [Estados de efecto (Direct3D 9).](effect-states.md)

## <a name="effects-can-share-parameters"></a>Los efectos pueden compartir parámetros

Los parámetros de efecto son todas las variables no estáticas declaradas en un efecto. Esto puede incluir variables globales y anotaciones. Los parámetros de efecto se pueden compartir entre distintos efectos declarando parámetros con la palabra clave shared y, a continuación, creando el efecto con un grupo de efectos.

Los efectos clonados usan el mismo grupo de efectos que el efecto desde el que se clonan. La clonación de un efecto realiza una copia exacta de un efecto, incluidas variables globales, técnicas, pases y anotaciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 9](dx9-graphics-programming-guide.md)
</dt> </dl>

 

 
