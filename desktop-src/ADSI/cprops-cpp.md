---
title: CPROPS. CPP
description: En el componente proveedor de ejemplo, se puede encontrar un ejemplo de una implementación de la caché de propiedades en cprops. cpp. En la tabla siguiente se enumeran los métodos admitidos.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903068"
---
# <a name="cpropscpp"></a>CPROPS. CPP

En el componente proveedor de ejemplo, se puede encontrar un ejemplo de una implementación de la caché de propiedades en cprops. cpp. En la tabla siguiente se enumeran los métodos admitidos.



| Método                                           | Descripción                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache:: AddProperty**                  | Amplíe la memoria caché de propiedades agregando una nueva.                                                                      |
| **CPropertyCache::updateproperty**               | Buscar la propiedad, liberar su contenido y usar nuevos valores en su lugar. a continuación, marque la memoria caché modificada para esta propiedad. |
| **CPropertyCache::findproperty**                 | Buscar esta propiedad por su nombre; Guarde el índice.                                                                      |
| **CPropertyCache:: GetProperty**                  | Busque la propiedad en la memoria caché si está disponible; de lo contrario, llame a **GetInfo**. Establezca el índice y copie los nuevos valores.  |
| **CPropertyCache::p utproperty**                  | Busque la propiedad. Libere lo que había y coloque los nuevos valores.                                                       |
| **CPropertyCache::CPropertyCache**               | Constructor estándar.                                                                                               |
| **CPropertyCache:: ~ CPropertyCache**              | Destructor estándar.                                                                                                |
| **CPropertyCache::createpropertycache**          | Cree la memoria caché.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Busque la propiedad en la memoria caché y establézcala en estos valores.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Calcula las referencias de los datos y los valores de propiedad.                                                                                   |
| **CPropertyCache::marshallproperty**             | Calcular las referencias de una propiedad.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Anular la serialización de los datos y valores de propiedad.                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Desserialización de una propiedad.                                                                                               |



 

 

 




