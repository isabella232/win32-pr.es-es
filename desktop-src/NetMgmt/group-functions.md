---
title: Funciones de grupo
description: Un grupo global contiene cuentas de usuario de un dominio que se agrupan en un nombre de cuenta de grupo.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069407"
---
# <a name="group-functions"></a>Funciones de grupo

Un *grupo global contiene* cuentas de usuario de un dominio que se agrupan en un nombre de cuenta de grupo. Un grupo global solo puede contener miembros (usuarios) del dominio donde se crea el grupo global; no puede contener grupos locales. Un grupo global está disponible dentro de su propio dominio y dentro de cualquier dominio de confianza.

Las funciones del grupo de administración de red controlan los grupos globales. Las funciones de grupo se enumeran a continuación.



| Función                                     | Descripción                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Crea un grupo global.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Agrega un usuario a un grupo global existente.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Quita un grupo global independientemente de si el grupo tiene o no miembros.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Quita un nombre de usuario de un grupo global.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Enumera todos los grupos globales de un servidor.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Devuelve información sobre un grupo global determinado.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Enumera todos los miembros de un grupo global determinado.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Establece información general sobre un grupo global.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Asigna miembros a un nuevo grupo global; reemplaza los miembros de un grupo existente. |



 

Al llamar a la [**función NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) para crear un grupo global, debe proporcionar un nombre de grupo. Inicialmente, un nuevo grupo no tiene miembros.

Las cuentas de usuario pertenecen automáticamente al grupo global especial Usuarios del dominio. La pertenencia a este grupo se controla indirectamente mediante las funciones [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)y [**NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

La información de la cuenta de grupo global está disponible en los niveles siguientes:

-   [**GROUP \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**GROUP \_ INFO \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**GROUP \_ INFO \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**GROUP \_ INFO \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**GROUP \_ INFO \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**GROUP \_ INFO \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

Los niveles 1002 y 1005 solo son válidos para la [**función NetGroupSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)

La información de los miembros del grupo global está disponible en el siguiente nivel de información:

-   [**GROUP \_ USERS \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

Para obtener más información, vea Funciones de grupo local de [administración de redes](local-group-functions.md).

Si está programando para Active Directory, puede llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones del grupo de administración de red. Para obtener más información, [**vea IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 