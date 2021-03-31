---
title: Catálogo global
description: Un dominio ejecutado por Active Directory Domain Services puede constar de muchas particiones o contextos de nomenclatura.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- Active Directory de catálogo global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4496804d21e53cf2d87947288179e7f96ca75c8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789532"
---
# <a name="global-catalog"></a>Catálogo global

Un dominio ejecutado por Active Directory Domain Services puede constar de muchas particiones o contextos de nomenclatura. El nombre distintivo (DN) de un objeto incluye suficiente información para localizar una réplica de la partición que contiene el objeto. Sin embargo, muchas veces el usuario o la aplicación no conoce el DN del objeto de destino o la partición que puede contener el objeto. El [*catálogo global (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) permite a los usuarios y las aplicaciones buscar objetos en un árbol de dominios de Active Directory, dados uno o más atributos del objeto de destino.

El catálogo global contiene una réplica parcial de cada contexto de nomenclatura en el directorio. También contiene los contextos de nomenclatura de esquema y configuración. Esto significa que el GC contiene una réplica de todos los objetos del directorio, pero solo con un número pequeño de sus atributos. Los atributos del GC son los que se usan con más frecuencia en las operaciones de búsqueda (por ejemplo, los nombres de inicio de sesión y apellidos de un usuario) y los necesarios para buscar una réplica completa del objeto. El GC permite a los usuarios encontrar rápidamente objetos de interés sin saber qué dominio los contiene y sin necesidad de un espacio de nombres extendido contiguo en la empresa.

El catálogo global se genera automáticamente mediante el sistema de replicación de Active Directory Domain Services. La topología de replicación para el catálogo global se genera automáticamente. Las propiedades replicadas en el catálogo global incluyen un conjunto base definido por Microsoft. Los administradores pueden especificar propiedades adicionales para satisfacer las necesidades de su instalación.

 

 