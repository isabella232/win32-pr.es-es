---
title: Glosario de cadena de intercambio de composición
description: Glosario de términos de cadena de intercambio de composición.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 04450f5107a9c06cc231336449e8ed9563212ad4
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128524021"
---
# <a name="composition-swapchain-glossary"></a>Glosario de cadena de intercambio de composición

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

|Término|Significado|
|-|-|
|**Disponible (búfer de presentación)**|Búfer seguro para que la aplicación se represente sin dañar los presentes anteriores. Para que esté disponible, un búfer no debe tener ningún presente anterior que haga referencia a él que no haya entrado en el estado de retirada o retirada. Un presente puede hacer referencia implícitamente a un búfer de un presente anterior si la aplicación no ha actualizado una superficie, como se muestra en el ejemplo de Diagrama de [búferes, superficies](comp-swapchain.md#diagram-of-buffers-surfaces-and-presents)y presenta .|
|**Composición (modo de presentación)**|Forma de presentación en la que el búfer presentado por la aplicación se copia en el búfer de reserva que DWM representa y envía para mostrar el hardware. Esta forma de presentación tiene requisitos del sistema más bajos que el examen directo o iflip, pero también es menos eficaz.|
|**Controlador de superficie de composición**|Identificador **que** puede enlazar un objeto visual de árbol visual con una cadena de intercambio determinada o una superficie de presentación.|
|**Volteo directo**|Una forma de presentación en la que la presentación del búfer por parte de la aplicación se envía directamente para mostrar el hardware en sistemas que no admiten la superposición de varios planos.|
|**Examen directo**|Forma de presentación en la que el búfer presentado por la aplicación no se vuelve a representar en el búfer que DWM envía a la pantalla, sino que se envía directamente al hardware de examen de GPU. Esto puede implicar que DWM asigne el búfer a un plano superpuesto multiplano o que sea un modo en el que el búfer se envía al hardware de examen directamente a través del volteo *directo.* En un modo de presentación de examen directo, DWM puede estar implicado en la programación del hardware para mostrar el presente, o bien puede omitirse completamente cuando el sistema está en modo *iflip.*|
|**Representación del búfer de front-in-buffer**|Trabajo de dibujo emitido para un búfer que el sistema muestra actualmente. Dependiendo de cómo se muestre el búfer, esto puede dar lugar a daños o a que una aplicación se queje, ya que Direct3D protege contra la emisión de trabajo de representación a los búferes que muestra el hardware de examen.|
|**Cola de volteo de hardware**|Una característica del sistema operativo (SO) compatible con algún hardware de GPU que permite que las GPU se muestren de forma independiente, sin intervención de la CPU, lo que reduce el consumo de energía, pero puede retrasar las actualizaciones de estado de la CPU, como eventos disponibles en búfer, presentar barrera de retirada y presentar estadísticas.|
|**Volteo independiente (iflip)**|Un método más eficaz de presentación de examen directo en el que los presentes se envían directamente al hardware de examen de GPU, omitiendo completamente el DWM. Esta forma de presentación tiene requisitos del sistema más altos, pero permite menores latencias y ahorro de energía del sistema.|
|**Superposición multiplano (MPO)**|Un tipo de hardware de presentación que puede mostrar varios planos que se muestran uno encima del otro. Los presentaciones del administrador de presentación se pueden mostrar como parte de un plano en una configuración de MPO para evitar la necesidad de copiar el búfer de presentación en el búfer de reserva que DWM envía al hardware de presentación.|
|**Presente**|Una única instancia de presentación. Presente que está pensado para mostrar los resultados de una operación de dibujo en un solo búfer en la pantalla.|
|**Identificador presente (id.)**|Identificador de incremento, único dentro de un administrador de presentación determinado, asociado a cada presente para permitir que se haga referencia a él mediante aspectos como las estadísticas de presentación y las barreras presentes.|
|**Cola presente**|Una cola de presenta que un administrador de presentación ha emitido, pero que el sistema todavía no ha procesado. Todos los presentaciones emitidos se procesan en orden de cola, incluso si sus horas de destino no aumentan. Es decir, antes de que se pueda procesar el presente *n,* también se debe procesar *el presente n-1;* Por lo tanto, si los siguientes presentaciones tienen una hora de destino anterior a una determinada presente, invalidarán inmediatamente ese presente concreto.|
|**(Presente) hora de destino**|Hora a la que debe mostrarse un presente determinado en la pantalla. El sistema intentará mostrar el presente lo más cerca posible de esta vez.|
|**Estadísticas de presentación**|información devuelta a la aplicación que describe cómo se procesó un presente determinado. Las estadísticas se ponen en cola en el administrador de presentación para que la aplicación las lea.|
|**Superficie de presentación**|marcador de posición de contenido que se puede enlazar a un objeto visual en un árbol visual. Una superficie de presentación puede tener un único búfer mostrado a la vez. El administrador de presentaciones actualizará los búferes de una o varias superficies de presentación.|
|**Presentación**|El concepto de mostrar los resultados de las operaciones de dibujo en pantalla.|
|**Búfer de presentación**|Una textura de Direct3D que se ha asociado a un administrador de presentación y, por lo tanto, se puede presentar en la pantalla por ese administrador de presentación.|
|**Árbol visual**|Árbol de objetos visuales que describe el diseño de una aplicación. Los problemas de la API de intercambio de composición se presentan a uno o varios objetos visuales de un árbol visual. Para obtener más información, [**consulte Windows.UI.Composition**](/uwp/api/windows.ui.composition) y [**DirectComposition**](/windows/win32/directcomp/directcomposition-portal) API.|
|**Interrupción de VSync**|cuando una GPU muestra un presente, emite una interrupción de VSync para interrumpir la CPU para notificarle que ese presente tuvo lugar. Esto permite que la CPU actualice el estado, como los eventos disponibles del búfer, la barrera de retirada actual y las estadísticas presentes. Si la GPU admite la cola de volteo de hardware, la aplicación puede controlar explícitamente qué presenta debe forzar una interrupción de VSync y un estado de actualización inmediato, y que no debe presentarse, lo que permite una mayor eficacia de energía a costa de comentarios retrasados.|

## <a name="related-topics"></a>Temas relacionados

* [Cadena de intercambio de composición](comp-swapchain-portal.md)
