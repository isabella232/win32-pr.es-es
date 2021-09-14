---
description: El editor de control de acceso puede incluir una página de propiedades Auditoría que permite al usuario ver y editar las entradas de control de acceso (ACE) en una lista de control de acceso del sistema (SACL) de objetos. Para obtener más información sobre las SACL, vea listas de Access Control listas de control de acceso (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Página de propiedades Auditoría
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069124"
---
# <a name="auditing-property-page"></a>Página de propiedades Auditoría

El editor de control  de acceso puede incluir una página de propiedades Auditoría que permite al usuario ver y editar las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) en la lista de control de acceso del sistema (SACL) de un objeto. [](/windows/desktop/SecGloss/s-gly) Para obtener más información sobre las SACL, [vea listas de Access Control](access-control-lists.md) listas de control de acceso (ACL).

**Para ver la página de propiedades Auditoría**

-   En la página [de propiedades de seguridad básica](basic-security-property-page.md), haga clic en **Avanzadas.** La **página de propiedades** Auditoría se encuentra en la hoja de propiedades de seguridad [avanzada](advanced-security-property-sheet.md).

Para incluir  la página de propiedades Auditoría, establezca las marcas **SI \_ ADVANCED** y **SI \_ EDIT \_ AUDITS** en la estructura [**SI OBJECT \_ \_ INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) devuelta por la implementación [**de ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)

 

 
