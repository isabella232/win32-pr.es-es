---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: Crear un Device-Specific PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31644f25f231f7121e2e492bc3f41a81b82d0b4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707623"
---
# <a name="creating-a-device-specific-printticket"></a>Crear un Device-Specific PrintTicket

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un PrintTicket específico del dispositivo se dirige a un dispositivo determinado y, por lo tanto, no suele ser portable en varios dispositivos.

Los pasos que se muestran en la lista siguiente deben usarse cuando se crea un PrintTicket específico del dispositivo.

1.  Obtenga un documento de PrintCapabilities que contenga solo las instancias de características relevantes para el dispositivo. Solicitar un documento de PrintCapabilities predeterminado. Esto no requiere que especifique un PrintTicket de entrada porque los atributos del dispositivo (instancias de características y opciones y parámetros) que se usan para construir el PrintTicket son independientes de la configuración.

2.  Cree un documento XML vacío que contenga la raíz de PrintTicket. Asigne un prefijo de espacio de nombres al espacio de nombres del esquema de impresión y asigne prefijos para el resto de espacios de nombres que usará el PrintTicket. Especifique la versión del esquema PrintTicket.

3.  Puede definir la configuración en el PrintTicket para cada característica y instancia de ParameterDef que se notifique en el documento de PrintCapabilities, o solo las que le interesen. Si se presenta un PrintTicket parcial a la interfaz PrintTicket, se proporcionan automáticamente los valores predeterminados para las instancias de características y ParameterDef omitidas durante la validación de PrintTicket.

4.  Examine el documento de PrintCapabilities para ver las instancias de características y determine cuáles de ellas desea definir en el PrintTicket. Agregue estas instancias de características al PrintTicket, pero no transfiera el contenido de las instancias de características a su PrintTicket. Si transfiere una subcaracterística, la característica primaria también debe transferirse y la relación de elementos primarios y secundarios se debe conservar en el PrintTicket.

    Para cada característica que transfiera, determine qué instancias de opción se aplican a su PrintTicket. Transfiera toda la opción tal y como se define en el documento de PrintCapabilities y, a continuación, quite todas las instancias de propiedad que estén presentes. Las instancias de propiedad se utilizan en los documentos de PrintCapabilities, pero no sirven para ningún propósito en el PrintTicket. Mantenga todas las instancias de ScoredProperty, asegurándose de que conserva su ubicación; son una parte intrínseca de la definición de la opción.

5.  También puede Agregar instancias de propiedad a cualquier instancia de ScoredProperty. Las instancias de propiedad solo se usan si el proveedor de PrintTicket admite explícitamente su uso. Cada proveedor debe documentar el propósito y el uso de todas las instancias de propiedad admitidas. Tenga en cuenta que durante la validación se quitan todas las instancias de propiedad incluidas en una instancia de opción, a menos que el espacio de nombres de la propiedad sea reconocido por el proveedor de PrintCapabilities o PrintTicket de destino, y se encuentre una opción candidata en el documento de PrintCapabilities cuyas instancias de ScoredProperty coincidan exactamente con las definidas en la opción de referencia.

6.  Si las palabras clave de esquema de impresión establecen la propiedad SelectionType en PickMany para una característica determinada, puede seleccionar más de una opción para esa característica, siempre que la opción designada como IdentityOption no sea una de las seleccionadas. IdentityOption en el esquema de impresión tiene el mismo efecto que la opción None en archivos PPD PostScript y archivos GPD de unidrv; sirve como una operación no operativa.

7.  Examine el documento de PrintCapabilities para las instancias de ParameterDef que se deben establecer en el PrintTicket. Para cada instancia de ParameterDef, seleccione el valor que se va a usar en la instancia de ParameterInit del PrintTicket. Este valor debe ser del tipo de datos correcto y debe estar dentro del intervalo definido en la instancia de ParameterDef y debe cumplir todos los demás requisitos especificados en la instancia de ParameterDef. Use una instancia de ParameterInit para inicializar el parámetro en el valor que ha seleccionado.

8.  Examine el contenido de cada instancia de opción que aparece en el PrintTicket para las apariciones de instancias de ParameterRef. Si una instancia de ParameterInit correspondiente todavía no aparece en el PrintTicket, siga el paso anterior para crear una instancia de ParameterInit en el PrintTicket. El propósito de esta instancia de ParameterInit es inicializar el parámetro al que hace referencia la instancia de ParameterRef.

9.  Tenga en cuenta que los conflictos de restricción podrían impedir que el dispositivo aplique la configuración que ha especificado en el PrintTicket. Si es necesario, el proceso de validación modifica la configuración definida en el PrintTicket en una que está libre de conflictos.

10. Examine las palabras clave del esquema de impresión para las instancias de propiedad que deben estar presentes en el PrintTicket. Agregue una instancia de propiedad a su PrintTicket para cada que sea necesario y proporcione un valor adecuado para ella mediante el tipo de elemento de valor. Asegúrese de que las instancias de propiedad se encuentran correctamente en el PrintTicket.

11. Examine las instancias de propiedad opcionales en el esquema PrintTicket. Si hay alguna instancia de esta propiedad que debe estar en el PrintTicket, créela en el PrintTicket.

12. También puede Agregar instancias de propiedad definidas de forma privada en el nivel raíz o en cualquier característica, opción o instancia de propiedad. Tenga en cuenta, sin embargo, que estas instancias de propiedad definidas de forma privada se eliminan durante la validación, a menos que el proveedor de PrintTicket o PrintTicket de destino reconozca el espacio de nombres al que pertenecen. Además, las instancias de propiedad que aparecen en cualquier parte de una instancia de opción se eliminan durante la validación, a menos que el documento de PrintCapabilities contenga una opción que sea una coincidencia perfecta. Dos instancias de opción son una coincidencia perfecta si cada ScoredProperty en una instancia de opción tiene un ScoredProperty correspondiente en el otro, y los valores de las instancias de ScoredProperty son los mismos. Consulte el esquema privado del proveedor PrintTicket para obtener una lista de instancias de propiedades privadas reconocidas y sus usos.

13. Los elementos secundarios del mismo tipo de elemento no se pueden anidar en una profundidad de más de 10 elementos. Esta regla se aplica de forma independiente a cada tipo de elemento que se puede definir.

> [!Note]  
> El contenido XML de PrintTicket debe estar codificado mediante UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



