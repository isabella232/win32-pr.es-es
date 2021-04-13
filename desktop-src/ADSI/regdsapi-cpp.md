---
title: REGDSAPI. CPP
description: En el componente de proveedor de ejemplo, las funciones que representan una API que accede directamente al sistema operativo nativo se encuentran en Regdsapi. cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e160ab212960753c6f793f734ebd96dffdd0f9e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356697"
---
# <a name="regdsapicpp"></a>REGDSAPI. CPP

En el componente de proveedor de ejemplo, las funciones que representan una API que accede directamente al sistema operativo nativo se encuentran en Regdsapi. cpp. El componente de proveedor de ejemplo implementa su servicio de directorio en el registro. Para escribir un proveedor que tenga acceso a su propio servicio de directorio, cree sus propias implementaciones de esta API. En la tabla siguiente se enumeran las funciones admitidas.



| Método                             | Descripción                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Abra este objeto por nombre. Si el parámetro de tipo de clase de esquema es **null**, rellene el tipo encontrado. Recupere un identificador en el objeto.                                                             |
| **SampleDSCloseObject**            | Use el identificador recuperado por **SampleDSOpenObject**.                                                                                                                                            |
| **SampleDSRDNEnum**                | Recupere el identificador de un objeto de enumerador para administrar la enumeración de nombres distintivos relativos (RDN) de un objeto contenedor.                                                          |
| **SampleDSNextRDN**                | Con el identificador recuperado por **SampleDSRDNEnum**, obtenga el siguiente nombre distintivo relativo de este objeto contenedor.                                                                        |
| **SampleDSFreeEnum**               | Libere el objeto de enumerador asignado en **SampleDSRDNEnum**.                                                                                                                                   |
| **SampleDSModifyObject**           | Modifique las propiedades de un objeto en el servicio de directorio dado el identificador del objeto y una lista de atributos y sus valores.                                                              |
| **SampleDSReadObject**             | Lea las propiedades del objeto desde el servicio de directorio. Asigne la sintaxis del almacenamiento nativo a los valores de sintaxis de ADS correspondientes. Controle las propiedades con varios valores según corresponda. |
| **SampleDSGetPropertyDefinition**  | En el esquema, busque todas las definiciones de propiedad y sus atributos para este tipo de objeto de clase de esquema.                                                                                     |
| **SampleDSGetPropertyDefinition**  | En el esquema, buscar esta propiedad y sus atributos por nombre.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Memoria libre asignada por **GetPropertyDefinition**.                                                                                                                                            |
| **SampleDSGetTypeText**            | Obtiene el tipo de clase de esquema de un objeto en formato de texto.                                                                                                                                         |
| **SampleDSGetType**                | Obtiene el tipo de clase de esquema de un objeto.                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | Dado un identificador en el objeto de clase de esquema y un nombre de propiedad, recupere la información de la propiedad, como la sintaxis, etc.                                                                      |
| **FreeList**                       | Libere la memoria usada por una \_ lista LPWStr.                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Recupere el conjunto de todas las definiciones de clase de esquema y sus datos asociados del esquema.                                                                                                    |
| **SampleDSGetClassDefinition**     | Recupere datos sobre una clase de esquema determinada en el esquema.                                                                                                                                   |
| **SampleDSGetClassInfo**           | Dado el nombre de una clase de esquema, buscar los datos asociados, como las propiedades obligatorias.                                                                                                      |
| **SampleDSAddObject**              | Agregue un objeto en el servicio de directorio.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Quitar un objeto del servicio de directorio.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Cree un búfer de memoria para los datos de atributos y datos de operaciones.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Libere el búfer creado en **SampleDSCreateBuffer**.                                                                                                                                           |



 

 

 




