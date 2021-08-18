---
title: Elementos simples
description: Un elemento simple es un elemento de interfaz de usuario que comparte un objeto IAccessible con otros elementos y se basa en ese objeto IAccessible (normalmente su elemento primario) para exponer sus propiedades.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9676b8bf4198f8be753b3788fcc6defdec2d6a1d8ad3ff3fed2f41da4f256554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133648"
---
# <a name="simple-elements"></a>Elementos simples

Un *elemento simple es* un elemento de interfaz de usuario que comparte un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con otros elementos y se basa en ese objeto **IAccessible** (normalmente su elemento primario) para exponer sus propiedades. Para diferenciar entre los elementos que comparten un objeto **IAccessible,** el servidor asigna un identificador secundario único y positivo a cada elemento simple. Esta asignación se realiza por instancia de interfaz, por lo que los identificadores deben ser únicos dentro de ese contexto. Muchas implementaciones asignan estos IDs secuencialmente, empezando por 1. Este esquema no permite que los elementos simples tengan elementos secundarios propios. Los elementos simples también se conocen como *elementos secundarios.*

Para identificarse y exponerse de forma única, un elemento simple requiere un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario. Por lo tanto, al comunicarse con un **objeto IAccessible,** los clientes deben proporcionar el identificador secundario adecuado. Se puede usar un identificador **especial, CHILDID \_ SELF,** para hacer referencia al propio objeto accesible, en lugar de a uno de sus elementos secundarios.

El [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) compartido entre elementos simples suele corresponder a un objeto primario común en la interfaz de usuario. Por ejemplo, los cuadros de lista del sistema exponen un objeto accesible para el cuadro de lista general y elementos simples para cada elemento de cuadro de lista. En este caso, el **objeto IAccessible** del cuadro de lista también es el elemento primario o contenedor de los elementos de lista.

Para obtener más información sobre los objetos accesibles, vea [Objetos accesibles.](accessible-objects.md)

 

 




