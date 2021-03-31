---
description: Un privilegio es el derecho de una cuenta, como una cuenta de usuario o de grupo, para realizar diversas operaciones relacionadas con el sistema en el equipo local, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Privilegios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cccedffdf5786da07dd2cfd77c3de428ee15ba94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001281"
---
# <a name="privileges"></a>Privilegios

Un [*privilegio*](/windows/desktop/SecGloss/p-gly) es el derecho de una cuenta, como una cuenta de usuario o de grupo, para realizar diversas operaciones relacionadas con el sistema en el equipo local, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema. Los privilegios difieren de los derechos de acceso de dos maneras:

-   Los privilegios controlan el acceso a los recursos del sistema y a las tareas relacionadas con el sistema, mientras que los derechos de acceso controlan el acceso a los [objetos protegibles](securable-objects.md).
-   Un administrador del sistema asigna privilegios a las cuentas de usuario y de grupo, mientras que el sistema concede o deniega el acceso a un objeto protegible en función de los derechos de acceso concedidos en las ACE de la DACL del objeto.

Cada sistema tiene una base de datos de cuentas que almacena los privilegios que mantienen las cuentas de usuario y de grupo. Cuando un usuario inicia sesión, el sistema genera un [token de acceso](access-tokens.md) que contiene una lista de los privilegios del usuario, incluidos los concedidos al usuario o a los grupos a los que pertenece el usuario. Tenga en cuenta que los privilegios solo se aplican al equipo local; una cuenta de dominio puede tener privilegios diferentes en equipos diferentes.

Cuando el usuario intenta realizar una operación con privilegios, el sistema comprueba el token de acceso del usuario para determinar si el usuario contiene los privilegios necesarios y, en ese caso, comprueba si los privilegios están habilitados. Si el usuario produce un error en estas pruebas, el sistema no realiza la operación.

Para determinar los privilegios que se mantienen en un token de acceso, llame a la función [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) , que también indica los privilegios que están habilitados. La mayoría de los privilegios están deshabilitados de forma predeterminada.

La API de Windows define un conjunto de constantes de cadena, como el \_ \_ nombre ASSIGNPRIMARYTOKEN, para identificar los distintos privilegios. Estas constantes son las mismas en todos los sistemas y se definen en Winnt. h. Para obtener una tabla de los privilegios definidos por Windows, consulte [constantes de privilegios](authorization-constants.md). Sin embargo, las funciones que obtienen y ajustan los privilegios de un token de acceso usan el tipo de [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) para identificar los privilegios. Los valores de **LUID** para un privilegio pueden diferir de un equipo a otro y de un arranque a otro en el mismo equipo. Para obtener el **LUID** actual que corresponde a una de las constantes de cadena, utilice la función [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) . Utilice la función [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) para convertir un **LUID** en su constante de cadena correspondiente.

El sistema proporciona un conjunto de nombres para mostrar que describen cada uno de los privilegios. Resultan útiles cuando es necesario mostrar una descripción de un privilegio para el usuario. Use la función [**LookupPrivilegeDisplayName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) para recuperar una cadena de descripción que corresponda a la constante de cadena de un privilegio. Por ejemplo, en los sistemas que usan Inglés de EE. UU., el nombre para mostrar del \_ privilegio de nombre SYSTEMTIME de se \_ es "cambiar la hora del sistema".

Puede usar la función [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar si un token de acceso contiene un conjunto de privilegios especificado. Esto resulta útil principalmente para las aplicaciones de servidor que suplantan a un cliente.

Un administrador del sistema puede usar herramientas administrativas, como administrador de usuarios, para agregar o quitar privilegios para cuentas de usuario y de grupo. Los administradores pueden usar mediante programación las funciones de la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) para trabajar con privilegios. Las funciones [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) y [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) agregan o quitan privilegios de una cuenta. La función [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera los privilegios que mantiene una cuenta especificada. La función [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera las cuentas que contienen un privilegio especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de autorización](authorization-constants.md)
</dt> <dt>

[Habilitar y deshabilitar privilegios en C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
