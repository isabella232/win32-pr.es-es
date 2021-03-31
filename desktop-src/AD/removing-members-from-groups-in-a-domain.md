---
title: Quitar miembros de grupos en un dominio
description: Puede quitar usuarios, grupos o contactos de los grupos.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- agrupa AD, quitar miembros de grupos en un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789484"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Quitar miembros de grupos en un dominio

Puede quitar usuarios, grupos o contactos de los grupos. El atributo **member** del objeto **Group** contiene todos los miembros directos del grupo.

La manera más sencilla de quitar un miembro de un grupo es llamar al método [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) en la interfaz [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del objeto de grupo del que desea quitar miembros.

 

 