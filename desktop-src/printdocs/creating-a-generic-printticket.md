---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Crear un PrintTicket genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34281eda82a48ea0ac4077248547522ddc305ea
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707583"
---
# <a name="creating-a-generic-printticket"></a>Crear un PrintTicket genérico

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si el documento de PrintCapabilities para el dispositivo no está disponible o si se desconoce el dispositivo de destino, debe construir un PrintTicket genérico. Dado que no hay ningún documento de PrintCapabilities que proporcione un conjunto de características y elementos de opciones, o parámetros, las instancias admitidas de estos tipos de elemento se deben obtener directamente de las palabras clave del esquema de impresión.

Los pasos que se muestran en la lista siguiente deben usarse cuando se crea un PrintTicket genérico.

1.  Cree un documento XML vacío que contenga la raíz de PrintTicket. Asigne un prefijo de espacio de nombres al espacio de nombres del esquema de impresión. Especifique la versión del esquema.

2.  Examine las instancias de la característica en las palabras clave del esquema de impresión y determine cuáles de ellas desea definir en el PrintTicket. Agregue estas instancias de características a su PrintTicket. Al transferir una subcaracterística, debe transferir la característica primaria y conservar la relación de elementos primarios y secundarios entre la característica y la subcaracterística del PrintTicket.

    Para cada instancia de característica que transfiera, determine qué instancias de opción se aplican a su PrintTicket. En este conjunto de instancias de opción, transfiera cada instancia de opción completa tal como aparece en el esquema de impresión y, a continuación, quite todas las instancias de propiedad que estén presentes, con la posible excepción de aquellas que tengan importancia para su PrintTicket. Mantenga todas las instancias de ScoredProperty, asegurándose de que conserva su ubicación; son una parte intrínseca de la definición de la opción.

3.  También puede Agregar instancias de propiedad a cualquier ScoredProperty. Los elementos de propiedad solo son aplicables si el proveedor de PrintTicket admite explícitamente su uso. Cada proveedor debe documentar el propósito y el uso de todas las instancias de propiedad admitidas. Dado que no sabe qué proveedor procesará el PrintTicket, es posible que desee anexar solo las instancias de propiedad que son compatibles explícitamente con el proveedor de PrintTicket del sistema.

4.  Si las palabras clave de esquema de impresión establecen la propiedad SelectionType en PickMany para una característica determinada, puede seleccionar más de una opción para esa característica, siempre que la opción designada como IdentityOption no sea una de las seleccionadas. IdentityOption en el esquema de impresión tiene el mismo efecto que la opción None en archivos PPD PostScript y archivos GPD de unidrv; sirve como una operación no operativa.

5.  Examine las palabras clave del esquema de impresión para las instancias de ParameterDef que se deben inicializar en el PrintTicket. Para cada instancia de ParameterDef, seleccione el valor que se va a usar en la instancia de ParameterInit en PrintTicket. Este valor debe ser del tipo de datos correcto, debe encontrarse dentro del intervalo definido en la instancia de ParameterDef y debe cumplir todos los demás requisitos especificados en la instancia de ParameterDef. Use una instancia de ParameterInit para inicializar el parámetro en el valor que ha seleccionado.

    Si está desarrollando un componente de interfaz de usuario (IU), diseñe los métodos de generación de PrintTicket para que los usuarios puedan escribir el valor del elemento ParameterInit. Además, el método de entrada de la interfaz de usuario debe observar y cumplir las restricciones de entrada especificadas por el elemento ParameterDef asociado.

6.  Examine el contenido de cada instancia de opción que aparece en el PrintTicket para las repeticiones de ParameterRef. Si una instancia de ParameterInit correspondiente todavía no aparece en el PrintTicket, siga el paso anterior para crear una instancia de ParameterInit en el PrintTicket. El propósito de esta instancia de ParameterInit es inicializar el parámetro al que hace referencia la instancia de ParameterRef.

7.  Tenga en cuenta que es posible que el dispositivo que procesa el trabajo no admita todas las características especificadas en el PrintTicket. Tenga en cuenta también que es posible que se admita una característica con nombre, pero es posible que la opción especificada de esa característica no sea. Las mismas advertencias se aplican a los parámetros. Incluso si un dispositivo admite un parámetro con nombre, es posible que el valor especificado en la instancia de ParameterInit no esté dentro del intervalo válido para el dispositivo.

8.  Examine las palabras clave del esquema de impresión para las instancias de propiedad que deben estar presentes en el PrintTicket. Agregue una instancia de propiedad para cada una de ellas a su PrintTicket y proporcione un valor adecuado para ella mediante el tipo de elemento de valor. Asegúrese de que las instancias de propiedad se encuentran correctamente en el PrintTicket. Asegúrese de consultar el esquema PrintTicket en lugar del esquema PrintCapabilities.

9.  Examine las instancias de propiedad opcionales definidas en el esquema PrintTicket. Si hay alguna instancia de esta propiedad que debe estar en el PrintTicket, créela en el PrintTicket.

10. Los elementos secundarios del mismo tipo de elemento no se pueden anidar en una profundidad de más de 10 elementos. Esta regla se aplica de forma independiente a cada tipo de elemento que se puede definir.

> [!Note]  
> El contenido XML de PrintTicket debe estar codificado mediante UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



