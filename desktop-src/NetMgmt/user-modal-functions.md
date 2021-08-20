---
title: Funciones modales de usuario
description: Las funciones modales de usuario de administración de redes obtienen y establecen parámetros de todo el sistema relacionados con el comportamiento del sistema de seguridad.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addea3c76d79cbcdb0e359424be154893d2c436c1f6d45157ecf50e748fc9417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796801"
---
# <a name="user-modal-functions"></a>Funciones modales de usuario

Las funciones modales de usuario de administración de redes obtienen y establecen parámetros de todo el sistema relacionados con el comportamiento del sistema de seguridad.

Las funciones modales de usuario se enumeran a continuación.



| Función                                     | Descripción                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Devuelve información global para todos los usuarios y grupos globales de la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Establece información global para todos los usuarios y grupos globales de la base de datos de seguridad.                                                                                                                       |



 

Las funciones **NetUserModalsGet** y **NetUserModalsSet** examinan y modifican la configuración modal, que son parámetros globales que afectan a todas las cuentas de la base de datos de seguridad (por ejemplo, la longitud mínima de contraseña permitido). Toda la configuración modal se puede modificar mediante una llamada a **NetUserModalsSet**. La mayoría de los modales también se pueden modificar mediante el comando **net accounts.** Las funciones modales de usuario de administración de red no requieren que el servidor tenga seguridad de nivel de usuario.

La información modal del usuario está disponible en los niveles siguientes:

-   [**USER \_ MODALS \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**USER \_ MODALS \_ INFO \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**USER \_ MODALS \_ INFO \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**USER \_ MODALS \_ INFO \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

Los niveles de información siguientes solo son válidos para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) y reemplazan la forma anterior de pasar un *Parmnum* para establecer un campo específico:

-   [**USER \_ MODALS \_ INFO \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**USER \_ MODALS \_ INFO \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**USER \_ MODALS \_ INFO \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**USER \_ MODALS \_ INFO \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**USER \_ MODALS \_ INFO \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**INFORMACIÓN \_ DE MODALES \_ DE USUARIO \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**USER \_ MODALS \_ INFO \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Si está programando para Active Directory, puede llamar a determinados métodos de interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones modales del usuario de administración de redes. Para obtener más información, [**vea IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 