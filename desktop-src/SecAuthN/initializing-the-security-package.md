---
description: Enumera y explica los pasos necesarios para inicializar un paquete de seguridad.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inicialización del paquete de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071291"
---
# <a name="initializing-the-security-package"></a>Inicialización del paquete de seguridad

Estos pasos son necesarios antes de usar SSPI:

1.  Se debe llamar a la función de inicialización para obtener la dirección de la tabla de funciones de seguridad.

    El cliente y el servidor llaman a [**InitSecurityInterface para**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) un puntero a una [**tabla de distribución SecurityFunctionTable.**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) Esta tabla contiene punteros a funciones de devolución de llamada declaradas en Sspi.h. Estos punteros proporcionan acceso a las implementaciones del archivo DLL de las distintas funciones de SSPI.

2.  Se debe obtener información sobre los paquetes de seguridad admitidos.

    Aunque la mayoría de las aplicaciones usan paquetes de seguridad que admiten funcionalidades predeterminadas o comunes, los paquetes de seguridad pueden tener funcionalidades únicas de interés para la aplicación. Una aplicación que necesita funcionalidades especiales puede usar un paquete que ofrece esas funcionalidades. Para obtener más información, vea [Obtener información sobre los paquetes de seguridad.](getting-information-about-security-packages.md)

En este momento, la aplicación ha inicializado correctamente un SSP y ha elegido un paquete de seguridad con capacidades suficientes.

El [*paquete Negotiate*](../secgloss/n-gly.md) se puede usar donde el acuerdo entre el cliente y el servidor sobre qué paquete de seguridad usar se realiza en segundo plano. [](../secgloss/s-gly.md) Si no se usa el paquete Negotiate, el cliente y el servidor deben aceptar el paquete de seguridad específico que se usará antes de realizar los pasos de instalación anteriores.

 

 
