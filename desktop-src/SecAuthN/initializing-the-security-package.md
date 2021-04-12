---
description: Enumera y explica los pasos necesarios para inicializar un paquete de seguridad.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inicializar el paquete de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156028"
---
# <a name="initializing-the-security-package"></a>Inicializar el paquete de seguridad

Estos pasos son necesarios antes de usar SSPI:

1.  Se debe llamar a la función de inicialización para obtener la dirección de la tabla de funciones de seguridad.

    El cliente y el servidor llaman a [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) para un puntero a una tabla de distribución [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) . Esta tabla contiene punteros a las funciones de devolución de llamada declaradas en SSPI. h. Estos punteros proporcionan acceso a las implementaciones del archivo DLL de las diversas funciones SSPI.

2.  Debe obtener información acerca de los paquetes de seguridad admitidos.

    Aunque la mayoría de las aplicaciones usan paquetes de seguridad que admiten funcionalidades predeterminadas o comunes, los paquetes de seguridad pueden tener capacidades únicas de interés para la aplicación. Una aplicación que necesita funcionalidades especiales puede usar un paquete que ofrezca esas funcionalidades. Para obtener más información, consulte [obtener información acerca de los paquetes de seguridad](getting-information-about-security-packages.md).

En este punto, la aplicación ha inicializado correctamente un SSP y ha elegido un paquete de seguridad con las capacidades suficientes.

Se puede usar el paquete [*Negotiate*](../secgloss/n-gly.md) si el acuerdo entre el cliente y el servidor sobre qué [*paquete de seguridad*](../secgloss/s-gly.md) se va a usar se realiza en segundo plano. Si no se utiliza el paquete Negotiate, el cliente y el servidor deben estar de acuerdo en el paquete de seguridad específico que se utilizará antes de realizar los pasos de configuración anteriores.

 

 
