---
title: Enumerar miembros de un grupo
description: Los miembros de un grupo se almacenan en un atributo de varios valores denominado Member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerar miembros de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149179"
---
# <a name="enumerating-members-in-a-group"></a>Enumerar miembros de un grupo

Los miembros de un grupo se almacenan en un atributo de varios valores denominado **member**. En el caso de los grupos con una pertenencia de tamaño pequeño a medio, use el método [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obtener un puntero a un objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contiene la lista de todos los miembros. A continuación, use [**IADsMembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obtener un objeto de enumerador que puede usar para enumerar los miembros.

Si la pertenencia al grupo esperada será de 1000 o más miembros, use para recuperar los usuarios de un intervalo a la vez. Para obtener más información sobre cómo utilizar el intervalo para enumerar miembros, vea [enumerar grupos que contienen muchos miembros](enumerating-groups-that-contain-many-members.md).

 

 