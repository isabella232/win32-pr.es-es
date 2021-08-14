---
title: CPROPS. Cpp
description: En el componente de proveedor de ejemplo, se puede encontrar un ejemplo de una implementación de caché de propiedades en cprops.cpp. Los métodos admitidos se enumeran en la tabla siguiente.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66394b7375779f50a97505128178ec35106187c076ca5d6741375a7f71b8ec46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429004"
---
# <a name="cpropscpp"></a>CPROPS. Cpp

En el componente de proveedor de ejemplo, se puede encontrar un ejemplo de una implementación de caché de propiedades en cprops.cpp. Los métodos admitidos se enumeran en la tabla siguiente.



| Método                                           | Descripción                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache::addproperty**                  | Extienda la caché de propiedades agregando una nueva.                                                                      |
| **CPropertyCache::updateproperty**               | Busque la propiedad , libre su contenido y use nuevos valores en su lugar; a continuación, marque la caché modificada para esta propiedad. |
| **CPropertyCache::findproperty**                 | Busque esta propiedad por nombre; guardar su índice.                                                                      |
| **CPropertyCache::getproperty**                  | Busque la propiedad en la memoria caché si está disponible; de lo contrario, llame **a GetInfo**. Establezca el índice y copie los nuevos valores.  |
| **CPropertyCache::p utproperty**                  | Busque la propiedad . Liberar lo que había allí y colocar nuevos valores.                                                       |
| **CPropertyCache::CPropertyCache**               | Constructor estándar.                                                                                               |
| **CPropertyCache::~CPropertyCache**              | Destructor estándar.                                                                                                |
| **CPropertyCache::createpropertycache**          | Cree la memoria caché.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Busque la propiedad en la memoria caché y esta establezca en estos valores.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Serializar los datos y los valores de las propiedades.                                                                                   |
| **CPropertyCache::marshallproperty**             | Serializar una propiedad.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Datos y valores de la propiedad Unmarshal.                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Desmarshal una propiedad.                                                                                               |



 

 

 




