---
description: La interfaz IUpdateCollection define las siguientes propiedades.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propiedades de IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599e7ba6efd20810ad61a8f59f5cfec67ce82b9e95f42df5250360238c43d044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859765"
---
# <a name="iupdatecollection-properties"></a>Propiedades de IUpdateCollection

La [**interfaz IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) define las siguientes propiedades.



| Propiedad                                        | Descripción                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Obtiene una [**interfaz IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que se puede usar para enumerar la colección. |
| [**Count**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Obtiene el número de elementos de la colección.                                                                           |
| [**Elemento**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Obtiene o establece una [**interfaz IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) en una colección.                                                    |
| [**Readonly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Obtiene un valor booleano que indica si la colección de actualizaciones es de solo lectura.                                          |



 

 

 
