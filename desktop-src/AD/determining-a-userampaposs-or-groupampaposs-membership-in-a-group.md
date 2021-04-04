---
title: Determinar la pertenencia de un usuario o un grupo a un grupo
description: El método IADsGroup. IsMember se puede usar para determinar si un objeto es miembro de un grupo.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Determinar la pertenencia de un usuario o un grupo a un grupo de AD
- agrupa AD, determinar la pertenencia de un usuario o un grupo a un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077531"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a>Determinar la pertenencia de un usuario o un grupo a un grupo

El método [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) se puede usar para determinar si un objeto es miembro de un grupo. Este método devuelve **true** si el objeto especificado es un miembro directo del grupo, es decir, la propiedad de miembro del grupo contiene el objeto especificado.

Un grupo puede contener otros grupos. El método [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) no comprueba de forma recursiva los miembros de los grupos en su propiedad de miembro, los grupos dentro de esos grupos, etc. Para comprobar de forma recursiva que un objeto es miembro de un grupo, enumere los grupos en la propiedad de miembro, compruebe los miembros de esos grupos para ver si el objeto es un miembro, y si esos grupos contienen otros grupos, compruebe sus miembros, etc.

> [!Note]  
> Dado que los grupos se pueden anidar, la pertenencia a grupos puede tener bucles. Cualquier script que Enumere muchos grupos debe mantener una lista interna de grupos para finalizar la recursividad si ya se ha visitado un grupo.

 

 

 