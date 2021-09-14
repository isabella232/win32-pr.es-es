---
title: Administrar propiedades
description: Cada propiedad consta de un identificador de propiedad (único dentro de su conjunto de propiedades), una etiqueta de tipo variante (VT o VarType) que representa el tipo de un valor y el propio valor.
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- Structured Storage Strctd Stg ,using,managing properties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10dd78a1f8a8484090728dba6fe149840e940461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068914"
---
# <a name="managing-properties"></a>Administrar propiedades

Cada propiedad consta de un identificador de propiedad *(único* dentro de su conjunto de propiedades), una etiqueta de tipo variante (VT o *VarType)* que representa el tipo de un valor y el *propio* valor. La etiqueta de tipo variante describe la representación de los datos en el valor. Además, a una propiedad también  se le puede asignar un nombre de cadena que se pueda usar para identificar la propiedad, en lugar de usar el identificador de propiedad numérico (ID) necesario. Para crear y administrar propiedades, COM define la [**interfaz IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

La [**interfaz IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) incluye métodos para leer y escribir matrices de propiedades o nombres de propiedad. La interfaz incluye [**métodos Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) [**y Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) similares a [**los métodos IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) del mismo nombre. Hay métodos de utilidad que permiten establecer el identificador de clase (CLSID) del conjunto de propiedades, establecer las horas asociadas al conjunto y obtener estadísticas sobre el conjunto de propiedades. Por último, [**el método Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) crea un enumerador y devuelve un puntero a su [**interfaz IEnumSTATPROPSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) Puede llamar a los métodos de esta interfaz para enumerar las estructuras [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) en el objeto , que proporcionará información sobre todas las propiedades del conjunto de propiedades actual.

A continuación se muestra un ejemplo de cómo se representan las propiedades. Si una propiedad específica de un conjunto de propiedades contiene el nombre científico de un animales, ese nombre podría almacenarse como una cadena terminada en cero. Almacenado junto con el nombre sería un indicador de tipo para indicar que el valor es una cadena terminada en cero. Estas propiedades pueden tener las siguientes características:



| Id. de propiedad | Identificador de cadena | Indicador de tipo | Valor representado              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | PID \_ ANIMALNAME   | VT \_ LPWSTR     | Cadena Unicode terminada en cero |
| 03          | PID \_ LEGCOUNT     | VT \_ I2         | WORD                           |



 

Cualquier aplicación que reconozca el formato del conjunto de propiedades (que lo identifica a través de su identificador de formato (FMTID) puede mirar la propiedad con un identificador de PID PIENAME, determinar que es una cadena terminada en cero y leer y escribir \_ el valor. Aunque la aplicación puede llamar a [**IPropertyStorage::ReadMultiple para**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) leer cualquiera o todo un conjunto de propiedades (después de haber obtenido por primera vez un puntero), la aplicación debe saber cómo interpretar el conjunto de propiedades.

Un valor de propiedad se pasa a través de interfaces de propiedad como una instancia del tipo [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).

Es importante distinguir entre estas propiedades almacenadas (persistentes) y las propiedades en tiempo de ejecución. Las constantes de valor de tipo variante tienen nombres que comienzan por \_ VT. Sin embargo, el conjunto de PROPVARIANTs válidos no es totalmente equivalente al conjunto de VARIANT usado en Automation y ActiveX controles.

La única diferencia entre las dos estructuras es el conjunto permitido de etiquetas VT \_ (tipo variante/VarType) en cada una de ellas. Cuando se puede usar un determinado tipo de propiedad en VARIANT y PROPVARIANT, la etiqueta de tipo (el valor \_ VT) siempre tiene un valor idéntico. Además, para un valor VT determinado, la representación en memoria usada en \_ variants y PROPVARIANTs es idéntica. En conjunto, este enfoque permite al sistema de tipos detectar etiquetas de tipo no permitidos, al mismo tiempo que permite a un cliente conocedor implementar una conversión de puntero cuando sea necesario.

Para obtener más información, vea la sección siguiente, [Property Storage Considerations](property-storage-considerations.md).

 

 