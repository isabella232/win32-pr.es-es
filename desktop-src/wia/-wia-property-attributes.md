---
description: Todos los objetos de elemento tienen propiedades.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Atributos de propiedad (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdee1cdee48bba6183f9bcae2abc521ac9f53dfb33eec544ab3ed6bead4947b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007535"
---
# <a name="property-attributes-wia"></a>Atributos de propiedad (WIA)

Todos los objetos de elemento tienen propiedades. Las propiedades tienen atributos. Por ejemplo, los atributos de propiedad indican si una propiedad se lee, se escribe en o se elimina. También indican los valores de propiedad válidos. Las siguientes constantes son atributos de propiedad válidos: 

| Atributo de propiedad        | Significado                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| WIA \_ PROP \_ CACHEABLE      | El dispositivo puede almacenar en caché el valor de la propiedad.                                                               |
| WIA \_ PROP \_ FLAG           | La propiedad tiene una lista de valores de marca legal. Los valores de marca se combinan mediante una operación **OR bit** a bit. |
| LISTA DE PROPIEDADES DE WIA \_ \_           | La propiedad tiene una lista de valores legales.                                                                 |
| WIA \_ PROP \_ NONE           | La propiedad no tiene ningún valor válido asociado.                                          |
| INTERVALO DE PROPIEDADES DE WIA \_ \_          | La propiedad tiene un intervalo de valores válidos.                                                                |
| WIA \_ PROP \_ READ           | La aplicación puede leer el valor de la propiedad.                                                           |
| WIA \_ PROP \_ RW             | La aplicación puede leer y escribir el valor de la propiedad.                                                 |
| SE REQUIERE \_ SINCRONIZACIÓN DE \_ PROP DE WIA \_ | No debe usarse.                                                                                              |
| ESCRITURA DE PROP DE WIA \_ \_          | La aplicación puede escribir el valor de la propiedad.                                                          |



 

 

 



