---
title: Puntos de sincronización
description: Cuando se admiten conjuntos de propiedades en el mismo objeto que IStorage, es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf924458d81003e2cc211ff810ebb714399ac28e91189586491b584cff6a3390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034885"
---
# <a name="synchronization-points"></a>Puntos de sincronización

Cuando se admiten conjuntos de propiedades en el mismo objeto que [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.

El almacenamiento del conjunto de propiedades contiene la secuencia del conjunto de propiedades en un búfer interno hasta que ese búfer se confirma mediante el [**método IPropertyStorage::Commit.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) Esto es cierto si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se abrió en modo de transacción o en modo directo.

 

 




