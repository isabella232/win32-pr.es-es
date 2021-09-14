---
title: Funciones de servicio de directorio (administración de redes)
description: Las funciones del servicio de directorio de administración de redes permiten a los desarrolladores trabajar con el controlador de dominio y la pertenencia al dominio en el servicio de directorio.
ms.assetid: 9eeb8f40-85c0-49db-a307-193703e4f463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e843e06762b4a7ef55b3f979b12a62ee6adf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069418"
---
# <a name="directory-service-functions"></a>Funciones del servicio de directorio

Las funciones del servicio de directorio de administración de redes permiten a los desarrolladores trabajar con el controlador de dominio y la pertenencia al dominio en el servicio de directorio.

A continuación se enumeran las funciones del servicio de directorio de administración de redes.



| Función                                                                 | Descripción                                                                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)       | Agrega un nombre alternativo para el equipo especificado.                                                                                                                                          |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)           | Enumera los nombres del equipo especificado.                                                                                                                                                |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                           | Recupera una lista de unidades organizativas (UO) en las que se puede crear una cuenta de equipo.                                                                                                  |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                   | Recupera la información de estado de combinación para el equipo especificado.                                                                                                                               |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                   | Une un equipo a un grupo de trabajo o dominio.                                                                                                                                                  |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)       | Aprovisiona una cuenta de equipo para su uso posterior en una operación de unión a un dominio sin conexión.                                                                                                           |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername) | Quita un nombre alternativo para el equipo especificado.                                                                                                                                       |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)             | Cambia el nombre de un equipo de un dominio.                                                                                                                                                 |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)           | Establece el nombre del equipo principal para el equipo especificado.                                                                                                                                  |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                               | Une un equipo de un grupo de trabajo o un dominio.                                                                                                                                            |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                               | Comprueba la validez de un nombre de equipo, nombre de grupo de trabajo o nombre de dominio.                                                                                                                   |



 

Para obtener más información sobre la programación Active Directory, vea la [referencia Active Directory .](/windows/desktop/AD/active-directory-domain-services-reference) Para obtener más información sobre las unidades organizativas, consulte [Administración de usuarios](/windows/desktop/AD/managing-users) en la documentación Active Directory organización.

 

 