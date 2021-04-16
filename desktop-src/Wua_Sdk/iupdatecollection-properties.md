---
description: La interfaz IUpdateCollection define las siguientes propiedades.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propiedades de IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705728"
---
# <a name="iupdatecollection-properties"></a>Propiedades de IUpdateCollection

La interfaz [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) define las siguientes propiedades.



| Propiedad                                        | Descripción                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Obtiene una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) que se puede utilizar para enumerar la colección. |
| [**Contabiliza**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Obtiene el número de elementos de la colección.                                                                           |
| [**Elemento**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Obtiene o establece una interfaz [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) en una colección.                                                    |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Obtiene un valor booleano que indica si la colección de actualizaciones es de solo lectura.                                          |



 

 

 
