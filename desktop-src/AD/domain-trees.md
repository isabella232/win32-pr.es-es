---
title: Árboles de dominio
description: Un árbol de dominio está compuesto por varios dominios que comparten un esquema y una configuración comunes, formando un espacio de nombres contiguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- árbol de dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a1e2ed05284d2a08735b048fb41d97d6597634f711094d0a3763c2d7f8be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430526"
---
# <a name="domain-trees"></a>Árboles de dominio

Un *árbol de dominio* está compuesto por varios dominios que comparten un esquema y una configuración comunes, formando un espacio de nombres contiguo. Los dominios de un árbol también se vinculan entre sí mediante relaciones de confianza. Active Directory es un conjunto de uno o varios árboles.

Los árboles se pueden ver de dos maneras. Una vista son las relaciones de confianza entre dominios. La otra vista es el espacio de nombres del árbol de dominio.

## <a name="viewing-trust-relationships"></a>Ver relaciones de confianza

Puede dibujar un diagrama de un árbol de dominio basado en los dominios individuales y la relación de confianza existente.

Windows 2000 establece relaciones de confianza entre dominios en función del protocolo de seguridad Kerberos. La confianza de Kerberos es transitiva y jerárquica: si el dominio A confía en el dominio B y el dominio B confía en el dominio C, el dominio A confía en el dominio C.

![relación de confianza del árbol de dominio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Ver el espacio de nombres

También puede dibujar un diagrama de un árbol de dominio basado en el espacio de nombres . Puede determinar el nombre distintivo de un objeto siguiendo la ruta de acceso hasta la jerarquía del espacio de nombres del árbol de dominio. Esta vista es útil para agrupar objetos en una jerarquía lógica. La principal ventaja de un espacio de nombres contiguo es que una búsqueda en profundidad desde la raíz del espacio de nombres busca en toda la jerarquía.

![árbol de dominio de espacio de nombres](images/namespace.png)

 

 




