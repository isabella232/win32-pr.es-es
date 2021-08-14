---
title: REGDSAPI. Cpp
description: En el componente de proveedor de ejemplo, las funciones que representan una API que accede directamente al sistema operativo nativo se encuentran en Regdsapi.cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80179650c51f3561b8ab73bb5b28cd428867f7feac79a8341b315a1f2a510d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307665"
---
# <a name="regdsapicpp"></a>REGDSAPI. Cpp

En el componente de proveedor de ejemplo, las funciones que representan una API que accede directamente al sistema operativo nativo se encuentran en Regdsapi.cpp. El componente de proveedor de ejemplo implementa su servicio de directorio en el Registro. Para escribir un proveedor que acceda a su propio servicio de directorio, cree sus propias implementaciones de esta API. Las funciones admitidas se enumeran en la tabla siguiente.



| Método                             | Descripción                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Abra este objeto por nombre. Si el parámetro de tipo de clase de esquema **es NULL,** rellene el tipo encontrado. Recupera un identificador en el objeto .                                                             |
| **SampleDSCloseObject**            | Use el identificador recuperado por **SampleDSOpenObject**.                                                                                                                                            |
| **SampleDSRDNEnum**                | Recupere el identificador de un objeto enumerador para administrar la enumeración de nombres distintivos relativos (RDN) de un objeto contenedor.                                                          |
| **SampleDSNextRDN**                | Con el identificador recuperado por **SampleDSRDNEnum,** obtenga el siguiente nombre distintivo relativo de este objeto contenedor.                                                                        |
| **SampleDSFreeEnum**               | Libera el objeto enumerador asignado en **SampleDSRDNEnum**.                                                                                                                                   |
| **SampleDSModifyObject**           | Modifique las propiedades de un objeto en el servicio de directorio según el identificador del objeto y una lista de atributos y sus valores.                                                              |
| **SampleDSReadObject**             | Lea las propiedades del objeto desde el servicio de directorio. Asigne la sintaxis del almacenamiento nativo a los valores de sintaxis ads adecuados. Controle las propiedades con varios valores en consecuencia. |
| **SampleDSGetPropertyDefinition**  | En el esquema, busque todas las definiciones de propiedad y sus atributos para este tipo de objeto de clase de esquema.                                                                                     |
| **SampleDSGetPropertyDefinition**  | En el esquema, busque esta propiedad y sus atributos por nombre.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Memoria libre asignada por **GetPropertyDefinition.**                                                                                                                                            |
| **SampleDSGetTypeText**            | Obtiene el tipo de clase de esquema de un objeto en formato de texto.                                                                                                                                         |
| **SampleDSGetType**                | Obtiene el tipo de clase de esquema de un objeto .                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | Dado un identificador en el objeto de clase de esquema y un nombre de propiedad, recupere la información de la propiedad, como la sintaxis, y así sucesivamente.                                                                      |
| **FreeList**                       | Liberar la memoria usada por LPWSTR \_ LIST.                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Recupere el conjunto de todas las definiciones de clase de esquema y sus datos asociados del esquema.                                                                                                    |
| **SampleDSGetClassDefinition**     | Recuperar datos sobre una clase de esquema determinada en el esquema.                                                                                                                                   |
| **SampleDSGetClassInfo**           | Dado el nombre de una clase de esquema, busque sus datos asociados, como las propiedades obligatorias.                                                                                                      |
| **SampleDSAddObject**              | Agregue un objeto en el servicio de directorio.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Quite un objeto del servicio de directorio.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Cree un búfer de memoria para los datos de atributo y los datos de operación.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Libera el búfer creado en **SampleDSCreateBuffer.**                                                                                                                                           |



 

 

 




