---
title: Atributos indizados (AD DS)
description: Los atributos se pueden indexar. La indización de un atributo puede mejorar el rendimiento de las consultas para ese atributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Atributos indizados AD
- Atributos AD, indexados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656333"
---
# <a name="indexed-attributes-ad-ds"></a>Atributos indizados (AD DS)

Los atributos se pueden indexar. La indización de un atributo puede mejorar el rendimiento de las consultas para ese atributo.

Los atributos se indexan cuando el atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) de la definición de esquema del atributo tiene el bit menos significativo establecido en 1. Si se establece el bit menos significativo de la definición del esquema del atributo **searchFlags** en 1, se creará un índice de forma dinámica. Si se establece el bit menos significativo de la definición del esquema del atributo **searchFlags** en 0, se quitará el índice del atributo. Un subproceso en segundo plano generará automáticamente el índice en el controlador de dominio.

Idealmente, los atributos indexados deben ser de un solo valor con valores muy únicos distribuidos uniformemente en todo el conjunto de instancias. Cuanto menos únicos sean los valores de un atributo, más eficaz será el índice.

Los atributos con varios valores también se pueden indexar, pero el costo de crear el índice para un atributo con varios valores es mayor en lo que respecta al almacenamiento, la actualización y el tiempo de búsqueda. El requisito de unicidad de una propiedad con varios valores es el mismo que el de una propiedad de un solo valor. cuanto más únicos son los valores, más efectivo es el índice.

Los atributos más indexados que tiene una clase, más tiempo se requiere para crear nuevas instancias de la clase.

Los índices se aplican a los atributos, no a las clases. Es decir, cuando un atributo se marca como indizado, todas las instancias del atributo se agregan al índice, no solo las instancias que son miembros de una clase determinada.

Para comprobar que un servidor utiliza un índice para procesar una consulta, establezca el siguiente valor del registro en un controlador de dominio en 4. A continuación, realice una consulta en ese controlador de dominio y busque en el registro de eventos de directorio los datos sobre los índices, si los hay, utilizados para procesar la consulta.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Para obtener más información sobre otros bits en la propiedad [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , vea [características de los atributos](characteristics-of-attributes.md).

 

 