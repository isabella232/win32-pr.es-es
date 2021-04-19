---
title: Uso de perfiles de dispositivo con WCS
description: Los perfiles de dispositivo son una herramienta básica para la administración del color.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Sistema de color de Windows (WCS), perfiles de dispositivo
- WCS (sistema de colores de Windows), perfiles de dispositivo
- Administración del color de imagen, perfiles de dispositivo
- Administración del color, perfiles de dispositivo
- colores, perfiles de dispositivo
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- perfiles de dispositivo
- conversión de color
- perfiles de vínculo de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf58b46cbee67d437e7d6fe343c7f3a0fab451b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721383"
---
# <a name="using-device-profiles-with-wcs"></a>Uso de perfiles de dispositivo con WCS

Los perfiles de dispositivo son una herramienta básica para la administración del color. Un [Perfil de dispositivo](d.md) es un archivo que contiene información sobre cómo convertir colores en el espacio de colores y la [gama](./g.md) de colores de un dispositivo específico en un espacio de colores independiente del dispositivo. El espacio de colores independiente del dispositivo que usa ICM2 se denomina espacio de conexión de perfil (PC). Un perfil de dispositivo también contiene información sobre cómo convertir colores de los equipos en el espacio de colores y la gama de colores de un dispositivo específico.

Estos dos conjuntos de información de conversión se utilizan para la [conversión de color](c.md) y la administración del color. Por ejemplo, se puede crear una imagen en el espacio de colores y la gama de colores de una pantalla de vídeo. La información de los archivos de Perfil de dispositivo se puede usar para mostrar una representación de una imagen impresa. A menudo, los usuarios quieren ver en la pantalla cómo cambiarán los colores cuando se imprima una imagen. Esto se denomina prueba. Una imagen se puede probar convirtiendo los colores de la gama de colores de origen (la pantalla) en colores de [equipos](p.md) y, a continuación, convirtiéndolos desde los equipos a la gama de colores de destino (la impresora). La imagen resultante se puede mostrar en la pantalla, lo que permite al usuario ver el aspecto que tendrá la imagen final cuando se imprima.

Los perfiles de dispositivo también permiten usos más complejos. Por ejemplo, se pueden usar para hacerse una idea del aspecto que tendrá una imagen creada en una pantalla de vídeo cuando se imprima en una impresora láser de alta resolución. El ejemplo se obtiene más complejo si solo hay una impresora de inyección de tinta estándar en la que se va a probar. ICM2 convertirá la imagen de la [gama](./g.md) de la pantalla en la gama de la impresora de inyección de tinta. Desde allí, se convierte en la gama de la impresora láser. La imagen resultante se puede imprimir en la impresora de inyección de tinta. Por supuesto, la imagen tendría una resolución más alta cuando se imprimiera en la impresora láser de color. Sin embargo, los colores de la imagen de prueba que se imprimen en la impresora de inyección de tinta serían una coincidencia aproximada con los colores que imprimiría la impresora láser.

Las conversiones de un perfil de dispositivo se pueden concatenar en un único archivo, denominado perfil de *vínculo de dispositivo*. Si se usa varias veces una serie de conversiones, la creación de un perfil de vínculo de dispositivo para ellas acortará el tiempo de conversión.

Los perfiles de dispositivo se pueden administrar. La administración de perfiles es el proceso de asociar perfiles de color a instancias de dispositivos. Cualquier dispositivo de salida de color puede tener un conjunto de uno o varios perfiles de color asociados. Los fabricantes de hardware y terceros que proporcionan perfiles de color necesitan realizar la administración de perfiles.

Los conjuntos de perfiles pueden compartirse entre dispositivos o pueden estar dedicados a dispositivos específicos. Por ejemplo, supongamos que tiene dos impresoras de color del mismo modelo. Cada impresora requeriría que se asociara un conjunto de perfiles de color. El conjunto de perfiles de color de una impresora corresponde a las distintas configuraciones posibles en ese modelo. Al ser del mismo modelo, ambas impresoras podrían compartir un conjunto de perfiles. La alternativa es dar a cada impresora su propio conjunto de perfiles distinto. En el último caso, los perfiles de color del conjunto se pueden calibrar con precisión a la salida individual de la impresora, no solo a las características de salida generales del modelo.

Hay tres clases diferentes de perfiles ICC: perfiles de entrada, perfiles de presentación y perfiles de salida. Los perfiles de entrada suelen estar asociados a un dispositivo, como un escáner. Los perfiles de visualización suelen estar asociados a un monitor de equipo. Los perfiles de salida suelen estar asociados a las impresoras.

La especificación también permite perfiles de dispositivo, perfiles abstractos, perfiles de vínculo de dispositivo, perfiles de color con nombre y perfiles de espacio de colores.

Un perfil de dispositivo describe el espacio de colores de un dispositivo determinado.

Un perfil abstracto proporciona un método genérico para que los usuarios realicen cambios de color subjetivas en imágenes u objetos gráficos transformando los datos de color de los equipos.

Como se mencionó anteriormente, un perfil de vínculo de dispositivo Concatena una serie de perfiles en una transformación.

Los perfiles de color con nombre se pueden considerar como perfiles del mismo nivel para los perfiles de dispositivo. Para un dispositivo determinado, debería haber uno o varios perfiles de dispositivo para controlar las conversiones de color del proceso y uno o varios perfiles de color con nombre para controlar los colores con nombre. Puede haber varios perfiles de color con nombre para tener en cuenta los distintos consumibles o varios proveedores de colores con nombre.

Un perfil de espacio de colores describe un espacio de colores independiente del dispositivo.

En la tabla siguiente se resumen los distintos tipos de perfiles.



| Tipo de perfil        | Descripción                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Perfil abstracto    | Perfil que se ha ajustado para adaptarse a las preferencias específicas de un usuario.                                                     |
| Perfil de espacio de colores | Perfil que describe un espacio de colores independiente del dispositivo.                                                                    |
| Perfil de vínculo de dispositivo | Serie de perfiles que se concatenan en un único perfil.                                                    |
| Perfil de dispositivo      | Perfil que describe el espacio de colores de un dispositivo determinado.                                                              |
| Mostrar perfil     | Clase o categoría de perfiles que incluye cualquier tipo de perfil asociado a una pantalla.                                  |
| Perfil de entrada       | Clase o categoría de perfiles que incluye cualquier tipo de perfil asociado a un dispositivo de entrada, como un escáner.          |
| Perfil de color con nombre | Perfil para un espacio de colores compuesto por colores con nombre.                                                                    |
| Perfiles de salida     | Clase o categoría de perfiles que incluye cualquier tipo de perfil asociado a un dispositivo de salida impreso, como una impresora. |



 

Las transformaciones de color se pueden crear con uno o varios perfiles. Si una transformación se crea con un solo perfil, el perfil debe ser un perfil de vínculo de dispositivo. Una transformación también puede tener dos o más perfiles en una cadena. Si lo hace, puede que no contenga perfiles de vínculo de dispositivo. Los perfiles abstractos solo pueden estar en medio de la cadena. El primer y el último perfil deben ser perfiles de dispositivo o perfiles de espacio de colores.

 

 