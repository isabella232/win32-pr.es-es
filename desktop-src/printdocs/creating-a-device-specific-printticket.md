---
description: Obtenga información sobre cómo crear un PrintTicket específico del dispositivo, que tiene como destino un dispositivo determinado y es portátil en varios dispositivos.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Crear un Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b825bd875ada534c8c467cd18d90f2db9a2a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409557"
---
# <a name="creating-a-device-specific-printticket"></a>Crear un Device-Specific PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un PrintTicket específico del dispositivo tiene como destino un dispositivo determinado y, por lo tanto, no suele ser portátil en varios dispositivos.

Los pasos que se muestran en la lista siguiente se deben usar al crear un PrintTicket específico del dispositivo.

1.  Obtenga un documento PrintCapabilities que contenga solo las instancias de características pertinentes para el dispositivo. Solicite un documento PrintCapabilities predeterminado. Esto no requiere que especifique un PrintTicket de entrada porque los atributos de dispositivo (instancias y parámetros de característica y opción) que se usan para construir printTicket son independientes de la configuración.

2.  Cree un documento XML vacío que contenga la raíz PrintTicket. Asigne un prefijo de espacio de nombres al espacio de nombres Esquema de impresión y asigne prefijos para todos los demás espacios de nombres que usará PrintTicket. Especifique la versión del esquema PrintTicket.

3.  Puede definir la configuración en PrintTicket para todas las instancias de Feature y ParameterDef notificadas en el documento PrintCapabilities, o solo las que le interesen. Si se presenta un PrintTicket parcial a la interfaz PrintTicket, los valores predeterminados se proporcionan automáticamente para las instancias de Feature y ParameterDef omitidas durante la validación de PrintTicket.

4.  Examine el documento PrintCapabilities para las instancias de características y determine cuál de ellas desea definir en printticket. Agregue estas instancias de características a PrintTicket, pero no transfiera el contenido de las instancias de características a su PrintTicket. Si transfiere una subfeature, también se debe transferir la característica primaria y la relación de elementos primarios y secundarios se debe conservar en PrintTicket.

    Para cada característica que transfiera, determine qué instancias de Option son aplicables a su PrintTicket. Transfiera toda la opción tal como se define en el documento PrintCapabilities y, a continuación, quite las instancias de propiedad que estén presentes. Las instancias property se usan en documentos PrintCapabilities, pero no sirven para ningún propósito en PrintTicket. Mantenga todas las instancias de ScoredProperty y asegúrese de conservar su ubicación. son una parte intrínseca de la definición de opción.

5.  También puede agregar instancias de propiedad a cualquier instancia de ScoredProperty. Las instancias de propiedad solo se usan si el proveedor PrintTicket admite explícitamente su uso. Cada proveedor debe documentar el propósito y el uso de todas las instancias de propiedad admitidas. Tenga en cuenta que, durante la validación, se quitan todas las instancias de propiedad contenidas en una instancia de Option, a menos que el proveedor PrintCapabilities o PrintTicket de destino reconozca el espacio de nombres de la propiedad, y se encuentra una opción candidata en el documento PrintCapabilities cuyas instancias scoredProperty coinciden perfectamente con las definidas en la opción de referencia.

6.  Si las palabras clave de esquema de impresión establecen la propiedad SelectionType en PickMany para una característica determinada, puede seleccionar más de una opción para esa característica, siempre que la opción designada como IdentityOption no sea una de las seleccionadas. IdentityOption en el esquema de impresión tiene el mismo efecto que la opción None en los archivos PPD postscript y los archivos GPD unidrv; sirve como no operativo.

7.  Examine el documento PrintCapabilities para ver las instancias de ParameterDef que se deben establecer en printticket. Para cada instancia de ParameterDef, seleccione un valor que se usará en la instancia ParameterInit en PrintTicket. Este valor debe ser del tipo de datos correcto y debe estar dentro del intervalo definido en la instancia de ParameterDef y debe cumplir todos los demás requisitos especificados en la instancia de ParameterDef. Use una instancia parameterInit para inicializar el parámetro en el valor que ha seleccionado.

8.  Examine el contenido de cada instancia de Option que aparece en PrintTicket para ver si hay repeticiones de instancias parameterRef. Si aún no aparece una instancia de ParameterInit correspondiente en PrintTicket, siga el paso anterior para crear una instancia de ParameterInit en PrintTicket. El propósito de esta instancia parameterInit es inicializar el parámetro al que hace referencia la instancia ParameterRef.

9.  Tenga en cuenta que los conflictos de restricciones pueden impedir que el dispositivo aplique la configuración que ha especificado en PrintTicket. Si es necesario, el proceso de validación modifica la configuración definida en PrintTicket a una que está libre de conflictos.

10. Examine las palabras clave de esquema de impresión para las instancias de propiedad que deben estar presentes en printticket. Agregue una instancia de Property a PrintTicket para cada que sea necesario y proporcione un valor adecuado para ella mediante el tipo de elemento Value. Asegúrese de que las instancias de propiedad se encuentran correctamente dentro de PrintTicket.

11. Examine las instancias de propiedad opcionales en el esquema PrintTicket. Si hay alguna de estas instancias de propiedad que debe estar en printticket, crámelas en printticket.

12. También puede agregar instancias de propiedad definidas de forma privada en el nivel raíz, o a cualquier instancia de característica, opción o propiedad. Sin embargo, tenga en cuenta que estas instancias de propiedad definidas de forma privada se quitan durante la validación, a menos que el proveedor PrintCapabilities o PrintTicket de destino reconozca el espacio de nombres al que pertenecen. Además, las instancias de propiedad que aparecen en cualquier lugar dentro de una instancia de Opción se quitan durante la validación, a menos que el documento PrintCapabilities contenga una opción que sea una coincidencia perfecta. Dos instancias de Option son una coincidencia perfecta si cada ScoredProperty de una instancia de Option tiene una propiedad ScoredProperty correspondiente en la otra, y los valores de las instancias scoredProperty son los mismos. Consulte el esquema privado del proveedor PrintTicket para obtener una lista de las instancias de propiedad privada reconocidas y sus usos.

13. Los elementos secundarios del mismo tipo de elemento no pueden anidar en una profundidad de más de 10 elementos. Esta regla se aplica de forma independiente a cada tipo de elemento que se puede definir.

> [!Note]  
> El contenido XML de PrintTicket DEBE codificarse mediante UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



