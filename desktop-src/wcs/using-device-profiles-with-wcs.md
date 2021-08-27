---
title: Uso de perfiles de dispositivo con WCS
description: Los perfiles de dispositivo son una herramienta básica para la administración de colores.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Sistema de colores (WCS), perfiles de dispositivo
- WCS (Windows color), perfiles de dispositivo
- administración del color de imagen, perfiles de dispositivo
- administración de colores, perfiles de dispositivo
- colors,device profiles
- Windows Sistema de colores (WCS),perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- perfiles de dispositivo
- conversión de colores
- perfiles de vínculo de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8211ff883f8e30e7b67b0168e6da980744b252cbb1b89412fc834ac6370cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090075"
---
# <a name="using-device-profiles-with-wcs"></a>Uso de perfiles de dispositivo con WCS

Los perfiles de dispositivo son una herramienta básica para la administración de colores. Un [perfil de dispositivo](d.md) es un archivo que contiene información sobre [](./g.md) cómo convertir colores en el espacio de colores y la gama de colores de un dispositivo específico en un espacio de colores independiente del dispositivo. El espacio de color independiente del dispositivo que usa ICM2 se denomina Espacio de conexión de perfil (PCS). Un perfil de dispositivo también contiene información sobre cómo convertir colores del PCS en el espacio de colores y la gama de colores de un dispositivo específico.

Estos dos conjuntos de información de conversión se usan para la [conversión de colores y](c.md) la administración de colores. Por ejemplo, se puede crear una imagen en el espacio de color y la gama de colores de una presentación de vídeo. La información de los archivos de perfil de dispositivo se puede usar para mostrar una representación de una imagen impresa. A menudo, los usuarios quieren ver en la pantalla cómo cambiarán los colores cuando se imprima una imagen. Esto se denomina prueba. Una imagen se puede probar si se convierten los colores de la gama de colores de origen (la pantalla) en colores [PCS](p.md) y, a continuación, se convierten desde el PCS en la gama de colores de destino (la impresora). La imagen resultante se puede mostrar en la pantalla, lo que permite al usuario ver el aspecto que tendrá la imagen final cuando se imprima.

Los perfiles de dispositivo también permiten usos más complejos. Por ejemplo, se pueden usar para obtener una idea del aspecto que tendría una imagen creada en una pantalla de vídeo cuando se imprime en una impresora de rayos de alta resolución. El ejemplo es más complejo si solo hay una impresora inkjet estándar en la que probarla. ICM2 convertirá la imagen de la [gama](./g.md) de la pantalla en la gama de la impresora inkjet. A partir de ahí, se convierte en la gama de la impresora de rayos. La imagen resultante se puede imprimir en la impresora inkjet. Por supuesto, la imagen tendría una resolución más alta cuando se imprime en la impresora de color de rayos. Sin embargo, los colores de la imagen de prueba impresa en la impresora inkjet coincidirían estrechamente con los colores que imprimiría la impresora de rayos.

Las conversiones de un perfil de dispositivo se pueden concatenar en un único archivo, denominado perfil *de vínculo de dispositivo*. Si se usa una serie de conversiones varias veces, la creación de un perfil de vínculo de dispositivo para ellas acortará el tiempo de conversión.

Los propios perfiles de dispositivo se pueden administrar. La administración de perfiles es el proceso de asociar perfiles de color a instancias de dispositivo. Cualquier dispositivo de salida de color puede tener un conjunto de uno o varios perfiles de color asociados. Los fabricantes de hardware y terceros que proporcionan perfiles de color deben realizar la administración de perfiles.

Los conjuntos de perfiles se pueden compartir entre dispositivos o se pueden dedicar a dispositivos específicos. Por ejemplo, suponga que tiene dos impresoras de color del mismo modelo. Cada impresora requeriría que se asociara un conjunto de perfiles de color. El conjunto de perfiles de color de una impresora corresponde a las distintas configuraciones posibles en ese modelo. Al ser del mismo modelo, ambas impresoras podrían compartir un conjunto de perfiles. La alternativa es proporcionar a cada impresora su propio conjunto de perfiles distinto. En el último caso, los perfiles de color del conjunto se pueden calibrar con precisión según la salida individual de la impresora, no solo las características generales de salida del modelo.

Hay tres clases diferentes de perfiles DE JAVA: perfiles de entrada, perfiles de presentación y perfiles de salida. Los perfiles de entrada suelen estar asociados a un dispositivo, como un analizador. Los perfiles de visualización suelen estar asociados a un monitor de equipo. Los perfiles de salida se asocian normalmente a impresoras.

La especificación también permite perfiles de dispositivo, perfiles abstractos, perfiles de vínculo de dispositivo, perfiles de color con nombre y perfiles de espacio de color.

Un perfil de dispositivo describe el espacio de color de un dispositivo determinado.

Un perfil abstracto proporciona un método genérico para que los usuarios realicen cambios de color subjetivos en imágenes u objetos gráficos mediante la transformación de los datos de color dentro del PCS.

Como se mencionó anteriormente, un perfil de vínculo de dispositivo concatena una serie de perfiles en una transformación.

Los perfiles de color con nombre se pueden pensar como perfiles del mismo nivel que los perfiles de dispositivo. Para un dispositivo determinado, habría uno o varios perfiles de dispositivo para controlar las conversiones de color de proceso y uno o varios perfiles de color con nombre para controlar los colores con nombre. Puede haber varios perfiles de color con nombre para tener en cuenta diferentes consumibles o varios proveedores de colores con nombre.

Un perfil de espacio de color describe un espacio de colores independiente del dispositivo.

En la tabla siguiente se resumen los distintos tipos de perfiles.



| Tipo de perfil        | Descripción                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Perfil abstracto    | Un perfil que se ha ajustado para adaptarse a las preferencias concretas de un usuario.                                                     |
| Perfil de espacio de color | Perfil que describe un espacio de colores independiente del dispositivo.                                                                    |
| Perfil de Vínculo de dispositivo | Una serie de perfiles que se concatenan en un único perfil.                                                    |
| Perfil de dispositivo      | Perfil que describe el espacio de color de un dispositivo determinado.                                                              |
| Mostrar perfil     | Clase o categoría de perfiles que incluye cualquier tipo de perfil asociado a una presentación.                                  |
| Perfil de entrada       | Clase o categoría de perfiles que incluye cualquier tipo de perfil asociado a un dispositivo de entrada, como un analizador.          |
| Perfil de color con nombre | Perfil de un espacio de colores que consta de colores con nombre.                                                                    |
| Perfiles de salida     | Clase o categoría de perfiles que incluye cualquier tipo de perfil asociado a un dispositivo de salida de copia de seguridad, como una impresora. |



 

Las transformaciones de color se pueden crear con uno o varios perfiles. Si se crea una transformación con un solo perfil, el perfil debe ser un perfil de vínculo de dispositivo. Una transformación también puede tener dos o más perfiles en una cadena. Si lo hace, no puede contener perfiles de vínculo de dispositivo. Los perfiles abstractos solo pueden estar en medio de la cadena. El primer y el último perfil deben ser perfiles de dispositivo o perfiles de espacio de color.

 

 