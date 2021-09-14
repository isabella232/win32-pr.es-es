---
title: Navegación jerárquica
description: A menudo, los clientes deben moverse entre objetos en función de sus relaciones de elementos primarios y secundarios. Por ejemplo, un cliente podría tener ya información sobre un control de barra de herramientas, pero no tener información sobre los botones contenidos en él.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160561"
---
# <a name="hierarchical-navigation"></a>Navegación jerárquica

A menudo, los clientes deben moverse entre objetos en función de sus relaciones de elementos primarios y secundarios. Por ejemplo, un cliente podría tener ya información sobre un control de barra de herramientas, pero no tener información sobre los botones contenidos en él.

La [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expone las relaciones jerárquicas entre objetos . Los clientes pueden navegar desde un objeto primario a sus elementos secundarios o desde un objeto secundario a su elemento primario llamando a [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) o [**IAccessible::get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 




