---
title: Catálogo global
description: Un dominio ejecutado por Active Directory Domain Services puede constar de muchas particiones o contextos de nomenclatura.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- catálogo global Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81abf04ab3e4d95819f91b5db8753a265e49ca79b2f405a32665dc46a8f2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189133"
---
# <a name="global-catalog"></a>Catálogo global

Un dominio ejecutado por Active Directory Domain Services puede constar de muchas particiones o contextos de nomenclatura. El nombre distintivo (DN) de un objeto incluye información suficiente para buscar una réplica de la partición que contiene el objeto. Sin embargo, muchas veces, el usuario o la aplicación no conocen el DN del objeto de destino o qué partición podría contener el objeto. El [*catálogo global (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) permite a los usuarios y aplicaciones buscar objetos en un árbol de dominio Active Directory, dados uno o varios atributos del objeto de destino.

El catálogo global contiene una réplica parcial de cada contexto de nomenclatura del directorio. También contiene los contextos de nomenclatura de esquema y configuración. Esto significa que el GC contiene una réplica de todos los objetos del directorio, pero solo con un pequeño número de sus atributos. Los atributos del GC son los que se usan con más frecuencia en las operaciones de búsqueda (como los nombres y apellidos de un usuario o los nombres de inicio de sesión) y los necesarios para buscar una réplica completa del objeto. El GC permite a los usuarios encontrar rápidamente objetos de interés sin saber qué dominio los contiene y sin necesidad de un espacio de nombres extendido contiguo en la empresa.

El catálogo global se crea automáticamente mediante el sistema Active Directory Domain Services replicación. La topología de replicación para el catálogo global se genera automáticamente. Las propiedades replicadas en el catálogo global incluyen un conjunto base definido por Microsoft. Los administradores pueden especificar propiedades adicionales para satisfacer las necesidades de su instalación.

 

 