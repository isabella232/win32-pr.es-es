---
title: Agregar usuarios a un grupo
description: Joe Worden, el administrador de la empresa, agregará Julia Bankert al grupo de administración. Para agregar un objeto a un grupo, use el método IADsGroup. Add.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Agregar usuarios a un grupo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356718"
---
# <a name="adding-users-to-a-group"></a>Agregar usuarios a un grupo

Joe Worden, el administrador de la empresa, agregará Julia Bankert al grupo de administración. Para agregar un objeto a un grupo, use el método [**IADsGroup. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) .


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un nuevo grupo](creating-a-new-group.md)
</dt> </dl>

 

 




