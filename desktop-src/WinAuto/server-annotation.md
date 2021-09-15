---
title: Anotación del servidor
description: En esta sección se proporciona información sobre el uso de la anotación de servidor.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567377"
---
# <a name="server-annotation"></a>Anotación del servidor

En esta sección se proporciona información sobre el uso de la anotación de servidor.

## <a name="summary"></a>Resumen

Defina una clase que implemente [**IAccPropServer,**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)cree una instancia de ella e informe al sistema de que desea que invalide propiedades específicas en elementos de interfaz de usuario específicos. Cuando un cliente solicita una de las propiedades de uno de los elementos de la interfaz de usuario, se llama al objeto y se le da la oportunidad de proporcionar un valor. Si el objeto devuelve un valor, ese valor se devuelve al cliente. Si el objeto no devuelve un valor, el valor predeterminado de ese elemento de interfaz de usuario se devuelve al cliente.

## <a name="when-to-use-this-technique"></a>Cuándo usar esta técnica

Use esta técnica cuando desee invalidar las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un objeto . Esta técnica es mucho más sencilla que las **técnicas IAccessible** anteriores. Para obtener más información, vea [Alternativas a la anotación dinámica](alternatives-to-dynamic-annotation.md).

No se puede usar la anotación de servidor para modificar la estructura de objetos expuestos. Para cambiar la estructura de un objeto, debe implementar un puntero de [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.

Para obtener más información sobre la anotación del servidor, vea los temas siguientes:

-   [Usar anotación de servidor](using-server-annotation.md)
-   [Ejemplo de anotación de servidor](server-annotation-sample.md)

 

 




