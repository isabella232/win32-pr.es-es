---
title: Obtener funciones
description: Las funciones get de administración de red recuperan información sobre un dominio. También puede llamar a estas funciones para recuperar información sobre las cuentas de usuario locales, globales, de estación de trabajo y de servidor.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069408"
---
# <a name="get-functions"></a>Obtener funciones

Las funciones get de administración de red recuperan información sobre un dominio. También puede llamar a estas funciones para recuperar información sobre las cuentas de usuario locales, globales, de estación de trabajo y de servidor.

Las funciones get de administración de red se enumeran a continuación.



| Función                                                               | Descripción                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Devuelve el nombre de cualquier controlador de dominio para un dominio de confianza directa por un servidor especificado.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Devuelve el nombre del controlador de dominio principal (PDC) para el dominio especificado.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Devuelve el índice de la primera entrada de información para mostrar cuyo nombre comienza con una cadena especificada o sigue alfabéticamente a la cadena. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Devuelve información de cuentas de usuario, equipo o grupo global.                                                                             |



 

La información devuelta por [**la función NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) está disponible en los niveles siguientes:

-   [**NET \_ DISPLAY \_ GROUP**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**NET \_ DISPLAY \_ MACHINE**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**USUARIO \_ DE NET \_ DISPLAY**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




