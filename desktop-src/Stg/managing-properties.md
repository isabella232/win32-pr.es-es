---
title: Administrar propiedades
description: Cada propiedad está formada por un identificador de propiedad (único dentro de su conjunto de propiedades), una etiqueta de tipo variante (VT o VarType) que representa el tipo de un valor y el propio valor.
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- Almacenamiento estructurado Strctd STG, usar, administrar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10dd78a1f8a8484090728dba6fe149840e940461
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904668"
---
# <a name="managing-properties"></a>Administrar propiedades

Cada propiedad está formada por un *identificador de propiedad* (único dentro de su conjunto de propiedades), una etiqueta de *tipo variante (VT o VarType)* que representa el tipo de un valor y el propio *valor* . La etiqueta de tipo variante describe la representación de los datos en el valor. Además, una propiedad también puede tener asignado un *nombre de cadena* que se puede usar para identificar la propiedad, en lugar de usar el identificador de propiedad numérico (ID.) necesario. Para crear y administrar propiedades, COM define la interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .

La interfaz [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) incluye métodos para leer y escribir matrices de propiedades o nombres de propiedad. La interfaz incluye métodos [**commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) y [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) que son similares a los métodos [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del mismo nombre. Existen métodos de utilidad que permiten establecer el identificador de clase (CLSID) del conjunto de propiedades, establecer las horas asociadas al conjunto y obtener estadísticas sobre el conjunto de propiedades. Por último, el método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) crea un enumerador y devuelve un puntero a su interfaz [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) . Puede llamar a los métodos de esta interfaz para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) en el objeto, que proporcionará información sobre todas las propiedades del conjunto de propiedades actual.

A continuación se presenta un ejemplo de cómo se representan las propiedades. Si una propiedad específica de un conjunto de propiedades contiene el nombre científico de un animal, ese nombre podría almacenarse como una cadena terminada en cero. Almacenado junto con el nombre sería un indicador de tipo para indicar que el valor es una cadena terminada en cero. Estas propiedades pueden tener las siguientes características:



| Id. de propiedad | Identificador de cadena | Indicador de tipo | Valor representado              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | PID \_ ANIMALNAME   | VT \_ LPWStr     | Cadena Unicode terminada en cero |
| 03          | PID \_ LEGCOUNT     | I2 de VT \_         | WORD                           |



 

Cualquier aplicación que reconozca el formato del conjunto de propiedades, que lo identifica a través de su identificador de formato (FMTID), puede examinar la propiedad con un identificador de PID \_ ANIMALNAME, determinar que es una cadena terminada en cero y leer y escribir el valor. Aunque la aplicación puede llamar a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para leer alguno o todos los conjuntos de propiedades (que primero obtuvieron un puntero), la aplicación debe saber cómo interpretar el conjunto de propiedades.

Un valor de propiedad se pasa a través de las interfaces de propiedad como una instancia del tipo [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).

Es importante distinguir entre estas propiedades almacenadas (persistentes) y las propiedades en tiempo de ejecución. Las constantes de valor de tipo variante tienen nombres que empiezan por VT \_ . Sin embargo, el conjunto de PROPVARIANTs válidos no es totalmente equivalente al conjunto de variantes usadas en Automation y controles ActiveX.

La única diferencia entre las dos estructuras es el conjunto permitido de etiquetas VT \_ (tipo variante/VarType) en cada una de ellas. Cuando se puede usar un tipo de propiedad determinado en una variante y en un PROPVARIANT, la etiqueta de tipo (el valor de VT \_ ) siempre tiene un valor idéntico. Además, para un valor de VT determinado \_ , la representación en memoria utilizada en las variantes y PROPVARIANTs es idéntica. En conjunto, este enfoque permite que el sistema de tipos detecte etiquetas de tipo no permitidas, al mismo tiempo que permite a un cliente con conocimiento de la implementación de un puntero convertido cuando sea necesario.

Para obtener más información, vea la sección siguiente, [consideraciones sobre el almacenamiento de propiedades](property-storage-considerations.md).

 

 