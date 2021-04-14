---
title: Objetos accesibles
description: Con Microsoft Active Accessibility, los elementos de la interfaz de usuario se exponen a los clientes como objetos del modelo de objetos componentes (COM).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419118"
---
# <a name="accessible-objects"></a>Objetos accesibles

Con Microsoft Active Accessibility, los elementos de la interfaz de usuario se exponen a los clientes como objetos del modelo de objetos componentes (COM). Estos *objetos accesibles* mantienen fragmentos de información, denominados *propiedades*, que describen el nombre del objeto, la ubicación de la pantalla y otra información necesaria para las ayudas de accesibilidad. Los objetos accesibles también proporcionan *métodos* a los que llaman los clientes para hacer que el objeto realice alguna acción. Los objetos accesibles que tienen elementos simples asociados a ellos también se denominan elementos *primarios* o *contenedores*.

Los objetos accesibles se implementan mediante la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) basada en com de Microsoft Active Accessibility. Los métodos y propiedades de **IAccessible** permiten a las aplicaciones cliente obtener información sobre los elementos de interfaz de usuario que necesitan los usuarios. Por ejemplo, [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) devuelve un puntero de interfaz a un elemento primario de un objeto accesible, y [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) proporciona un medio para que los clientes obtengan información sobre otros objetos dentro de un contenedor.

Para obtener más información sobre cómo se relacionan los objetos accesibles y los elementos simples, vea [elementos simples](simple-elements.md).

 

 




