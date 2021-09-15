---
title: Puntos de sincronización
description: Cuando se admiten conjuntos de propiedades en el mismo objeto que IStorage, es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270580"
---
# <a name="synchronization-points"></a>Puntos de sincronización

Cuando se admiten conjuntos de propiedades en el mismo objeto que [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), es importante tener en cuenta los puntos de sincronización entre el almacenamiento base y el almacenamiento de propiedades.

El almacenamiento del conjunto de propiedades contiene la secuencia del conjunto de propiedades en un búfer interno hasta que ese búfer se confirma mediante el [**método IPropertyStorage::Commit.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) Esto es así si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) se abrió en modo de transacción o en modo directo.

 

 




