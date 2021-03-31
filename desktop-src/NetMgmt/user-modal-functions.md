---
title: Funciones modales de usuario
description: Las funciones modales del usuario de administración de redes obtienen y establecen parámetros en todo el sistema relacionados con el comportamiento del sistema de seguridad.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995562"
---
# <a name="user-modal-functions"></a>Funciones modales de usuario

Las funciones modales del usuario de administración de redes obtienen y establecen parámetros en todo el sistema relacionados con el comportamiento del sistema de seguridad.

A continuación se enumeran las funciones modales de usuario.



| Función                                     | Descripción                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Devuelve información global de todos los usuarios y grupos globales en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Establece la información global de todos los usuarios y grupos globales en la base de datos de seguridad.                                                                                                                       |



 

Las funciones **NetUserModalsGet** y **NetUserModalsSet** examinan y modifican la configuración modal, que son parámetros globales que afectan a todas las cuentas de la base de datos de seguridad (por ejemplo, la longitud mínima de contraseña permitida). Se puede modificar toda la configuración modal llamando a **NetUserModalsSet**. La mayoría de los modales también se pueden modificar mediante el comando **net accounts** . Las funciones modales del usuario de administración de redes no requieren que el servidor tenga seguridad de nivel de usuario.

La información modal del usuario está disponible en los siguientes niveles:

-   [**Información sobre los modos de usuario \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**Información sobre los modos de usuario \_ \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**Información sobre los modos de usuario \_ \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**Información sobre los modos de usuario \_ \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

Los siguientes niveles de información solo son válidos para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) y reemplazan la forma más antigua de pasar un *Parmnum* para establecer un campo específico:

-   [**Información sobre los modos de usuario \_ \_ \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**Información sobre los modos de usuario \_ \_ \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**Información sobre los modos de usuario \_ \_ \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**Información sobre los modos de usuario \_ \_ \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**Información sobre los modos de usuario \_ \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**Información sobre los modos de usuario \_ \_ \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**Información sobre los modos de usuario \_ \_ \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr llamando a las funciones modales del usuario de administración de redes. Para obtener más información, vea [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 