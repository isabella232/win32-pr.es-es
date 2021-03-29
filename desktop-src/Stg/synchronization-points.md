---
title: Puntos de sincronización
description: Cuando se admiten conjuntos de propiedades en el mismo objeto que IStorage, es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780101"
---
# <a name="synchronization-points"></a>Puntos de sincronización

Cuando se admiten conjuntos de propiedades en el mismo objeto que [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.

El almacenamiento del conjunto de propiedades contiene el flujo del conjunto de propiedades en un búfer interno hasta que dicho búfer se confirma a través del método [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) . Esto es así si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se abrió en modo de transacción o en modo directo.

 

 




