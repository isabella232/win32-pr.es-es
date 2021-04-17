---
description: Explica los dominios integrados y de cuenta en los sistemas basados en Windows.
ms.assetid: 306c258b-950e-4506-99e2-67a3714285ff
title: Dominios integrados y de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d2d4bb18e1ac2ea33aaff008475a44515d9231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688030"
---
# <a name="built-in-and-account-domains"></a>Dominios integrados y de cuenta

Los dominios de un sistema basado en Windows se dividen en las dos categorías siguientes:

-   [Equipos que no son controladores de dominio](#computers-that-are-not-domain-controllers)
-   [Equipos que son controladores de dominio](#computers-that-are-domain-controllers)

## <a name="computers-that-are-not-domain-controllers"></a>Equipos que no son controladores de dominio

La base de datos del administrador de cuentas de seguridad (SAM) reside en cada equipo y administra las cuentas para el dominio integrado y el dominio de la cuenta.



| Domain          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dominio integrado | Este dominio contiene los grupos locales predeterminados, como los grupos administradores y usuarios, que se establecen cuando se instala el sistema operativo. El nombre de este dominio es una versión traducida de Builtin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Dominio de cuenta  | El dominio de la cuenta puede contener cuentas de usuario, grupo y grupo local. La cuenta de administrador está en este dominio. Las cuentas definidas en el dominio de cuenta de una estación de trabajo o un servidor miembro se limitan a tener acceso a los recursos ubicados en el equipo físico en el que reside la cuenta. En un sistema que no forma parte de una red y, por tanto, no tiene un [dominio principal](primary-and-trusted-domains.md), el dominio de la cuenta se usa para alojar todas las cuentas que proporcionan acceso al equipo. En un sistema que forma parte de una red, el dominio de la cuenta del equipo se usa para alojar cuentas que no tienen acceso a recursos de red. Las cuentas que requieran acceso a la red deben definirse en el dominio de cuenta de un controlador de dominio.<br/> El nombre de este dominio se asigna en el momento de la instalación del sistema y viene determinado por el nombre del equipo. Si se cambia el nombre del equipo, el nombre de dominio de la cuenta no se actualizará hasta que se reinicie el equipo.<br/> |



 

## <a name="computers-that-are-domain-controllers"></a>Equipos que son controladores de dominio

Los controladores de dominio no tienen dominios de cuenta o integrados. Además, en lugar de una base de datos de SAM, estos sistemas usan el servicio de directorio de Microsoft Active Directory para almacenar la información de acceso de la cuenta. Para obtener más información, vea [Active Directory](/windows/desktop/AD/active-directory-domain-services).

 

