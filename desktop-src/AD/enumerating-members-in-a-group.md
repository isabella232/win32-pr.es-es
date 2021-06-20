---
title: Enumerar miembros de un grupo
description: Obtenga información sobre cómo enumerar los miembros de un Azure Active Directory grupo. Los miembros de un grupo se almacenan en un atributo de varios valores denominado miembro.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerar miembros de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407428"
---
# <a name="enumerating-members-in-a-group"></a>Enumerar miembros de un grupo

Los miembros de un grupo se almacenan en un atributo de varios valores denominado **miembro**. En el caso de los grupos con una pertenencia de tamaño pequeño a mediano, use el método [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obtener un puntero a un objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contiene la lista de todos los miembros. A continuación, use [**IADsMembers::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obtener un objeto enumerador que puede usar para enumerar los miembros.

Si la pertenencia a grupos prevista será de 1000 o más miembros, use ranging para recuperar usuarios de un intervalo a la vez. Para obtener más información sobre el uso de para enumerar miembros, vea [Enumerating Groups That Contain Many Members](enumerating-groups-that-contain-many-members.md).

 

 