---
title: Objetos accesibles
description: Con Microsoft Active Accessibility, los elementos de la interfaz de usuario se exponen a los clientes como objetos del Modelo de objetos componentes (COM).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9591c4884826ba9d85192e5702d0528f25087797faf83d83314d5c00f172459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994385"
---
# <a name="accessible-objects"></a>Objetos accesibles

Con Microsoft Active Accessibility, los elementos de la interfaz de usuario se exponen a los clientes como objetos del Modelo de objetos componentes (COM). Estos *objetos accesibles* mantienen fragmentos de información, denominados propiedades *,* que describen el nombre del objeto, la ubicación de la pantalla y otra información necesaria para las ayuda de accesibilidad. Los objetos accesibles también *proporcionan métodos* a los que los clientes llaman para hacer que el objeto realice alguna acción. Los objetos accesibles que tienen elementos simples asociados a ellos también se *denominan elementos principales* o *contenedores*.

Los objetos accesibles se implementan mediante Microsoft Active Accessibility interfaz IAccessible basada en [**COM.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Los **métodos y** propiedades IAccessible permiten a las aplicaciones cliente obtener información sobre los elementos de la interfaz de usuario que necesitan los usuarios. Por ejemplo, [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) devuelve un puntero de interfaz al elemento primario de un objeto accesible e [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) proporciona un medio para que los clientes obtengan información sobre otros objetos dentro de un contenedor.

Para obtener más información sobre cómo se relacionan los objetos accesibles y los elementos simples, vea [Elementos simples](simple-elements.md).

 

 




