---
title: Datos Storage persistentes en el servidor
description: Puede optimizar la aplicación para que el código auxiliar del servidor no libre memoria en el servidor al finalizar una llamada a procedimiento remoto.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161051"
---
# <a name="persistent-storage-on-the-server"></a>Datos Storage persistentes en el servidor

Puede optimizar la aplicación para que el código auxiliar del servidor no libre memoria en el servidor al finalizar una llamada a procedimiento remoto. Por ejemplo, cuando varios procedimientos remotos manipularán un identificador de contexto, puede usar el atributo ACF **\[ allocate(don't \_ free) \]** para conservar la memoria asignada en el servidor.

El **\[ atributo allocate(don't \_ free) \]** se agrega a la declaración **typedef** de ACF en el ACF. Por ejemplo:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

Cuando se especifica el atributo **\[ allocate(don't \_ free), \]** el código auxiliar del servidor asigna, pero no libera, la estructura de datos de árbol. Al hacer que los punteros a estas áreas de datos persistentes estén disponibles para otras rutinas (por ejemplo, copiando los punteros a variables globales), los datos retenidas son accesibles para otras funciones del servidor. El **\[ atributo allocate(don't \_ free) \]** es especialmente útil para mantener estructuras de puntero persistentes como parte de la información de estado del servidor asociada a un tipo de identificador de contexto.

 

 




