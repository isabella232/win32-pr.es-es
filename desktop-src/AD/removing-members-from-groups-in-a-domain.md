---
title: Quitar miembros de grupos en un dominio
description: Puede quitar usuarios, grupos o contactos de los grupos.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- groups AD , quitar miembros de grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025163"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Quitar miembros de grupos en un dominio

Puede quitar usuarios, grupos o contactos de los grupos. El **atributo** miembro del **objeto de** grupo contiene todos los miembros directos del grupo.

La manera más sencilla de quitar un miembro de un grupo es llamar al método [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) en la [**interfaz IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del objeto de grupo del que desea quitar miembros.

 

 