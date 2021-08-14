---
title: Atributos indexados (AD DS)
description: Los atributos se pueden indexar. La indexación de un atributo puede mejorar el rendimiento de las consultas para ese atributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Atributos indexados de AD
- Atributos de AD, indexados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd205fea66b198096a9a9427822eb4ba0ccb609fb3e6fef0854fa91848371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187589"
---
# <a name="indexed-attributes-ad-ds"></a>Atributos indexados (AD DS)

Los atributos se pueden indexar. La indexación de un atributo puede mejorar el rendimiento de las consultas para ese atributo.

Se indexa un atributo cuando el atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) de la definición de esquema del atributo tiene el bit menos significativo establecido en 1. Si se establece el bit menos significativo de la definición de esquema del atributo **searchFlags** en 1, se compilará dinámicamente un índice. Si se establece el bit menos significativo de la definición de esquema del atributo **searchFlags** en 0, se quitará el índice del atributo. El índice se genera automáticamente mediante un subproceso en segundo plano en el controlador de dominio.

Idealmente, los atributos indexados deben tener un solo valor con valores muy únicos distribuidos uniformemente entre el conjunto de instancias. Cuando menos únicos sean los valores de un atributo, menos eficaz será el índice.

Los atributos con varios valores también se pueden indexar, pero el costo de compilar el índice para un atributo de varios valores es mayor en términos de almacenamiento, actualización y tiempo de búsqueda. El requisito de unidad para una propiedad multivalor es el mismo que para una propiedad con un solo valor: cuanto más únicos sean los valores, más efectivo será el índice.

Entre más atributos indexados tenga una clase, más tiempo se necesita para crear nuevas instancias de la clase.

Los índices se aplican a atributos, no a clases. Es decir, cuando un atributo se marca como indexado, todas las instancias del atributo se agregan al índice, no solo las instancias que son miembros de una clase determinada.

Para comprobar que un servidor usa un índice para procesar una consulta, establezca el siguiente valor del Registro en un controlador de dominio en 4. A continuación, realice una consulta en ese controlador de dominio y busque en el registro de eventos del directorio los datos sobre los índices, si los hay, que se usan para procesar la consulta.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

Para obtener más información sobre otros bits de la [**propiedad searchFlags,**](/windows/desktop/ADSchema/a-searchflags) vea [Características de atributos.](characteristics-of-attributes.md)

 

 