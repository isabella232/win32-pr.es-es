---
title: Funciones Get
description: Las funciones de obtención de administración de red recuperan información sobre un dominio. También puede llamar a estas funciones para recuperar información acerca de las cuentas de usuario locales, globales, de estación de trabajo y de servidor.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532236"
---
# <a name="get-functions"></a>Funciones Get

Las funciones de obtención de administración de red recuperan información sobre un dominio. También puede llamar a estas funciones para recuperar información acerca de las cuentas de usuario locales, globales, de estación de trabajo y de servidor.

A continuación se enumeran las funciones de obtención de administración de red.



| Función                                                               | Descripción                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Devuelve el nombre de cualquier controlador de dominio para un dominio que sea de confianza directa para un servidor especificado.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Devuelve el nombre del controlador de dominio principal (PDC) para el dominio especificado.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Devuelve el índice de la primera entrada de información de visualización cuyo nombre comienza con una cadena especificada o que sigue alfabéticamente a la cadena. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Devuelve la información de la cuenta de usuario, equipo o grupo global.                                                                             |



 

La información devuelta por la función [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) está disponible en los siguientes niveles:

-   [**NET \_ Display \_ Group**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**NET \_ Display \_ Machine**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**NET \_ Display \_ User**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




