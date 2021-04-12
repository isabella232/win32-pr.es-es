---
description: Cuando se inicia un cliente, selecciona un paquete de seguridad para sus transacciones con un servidor y, a continuación, se pone en contacto con ese servidor. Un servidor selecciona uno o varios paquetes de seguridad y espera una conexión de cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obtención de información acerca de los paquetes de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154769"
---
# <a name="getting-information-about-security-packages"></a>Obtención de información acerca de los paquetes de seguridad

Cuando se inicia un cliente, selecciona un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) para sus transacciones con un servidor y, a continuación, se pone en contacto con ese servidor. Un servidor selecciona uno o varios paquetes de seguridad y espera una conexión de cliente.

Para obtener información específica sobre los paquetes de seguridad de SSPI disponibles con un SSP determinado, se puede llamar a la función [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) para recuperar una estructura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .

Para recuperar la estructura de salida, el llamador pasa a la función la dirección de un puntero al tipo de la estructura devuelta. La función asigna memoria y devuelve los datos al llamador asignando la dirección del búfer de datos devueltos al argumento. La Convención SSPI es que la función asigna memoria a la estructura y la aplicación que realiza la llamada libera esa memoria mediante [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).

Al llamar a la función [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) se recuperan los atributos de un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly). Tanto el servidor como el cliente pueden llamar a la función **QuerySecurityPackageInfo** para obtener la longitud máxima del token de seguridad del miembro **cbMaxToken** de la estructura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . Para obtener un ejemplo, consulte la llamada a la función **QuerySecurityPackageInfo** que se muestra en [usar SSPI con un servidor de Windows Sockets](using-sspi-with-a-windows-sockets-server.md).

Para obtener más información sobre las funciones de paquete, vea [Administración de paquetes](authentication-functions.md).

 

 
