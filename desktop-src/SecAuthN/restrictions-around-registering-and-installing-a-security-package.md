---
description: Acciones por paquetes de seguridad que no se admiten en Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restricciones en relación con el registro y la instalación de un paquete de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808359"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restricciones en relación con el registro y la instalación de un paquete de seguridad

La eliminación, sustitución o ajuste de paquetes de seguridad de bandeja de entrada (por ejemplo, Kerberos o NTLM) no es una acción admitida en Windows y, a partir del 10 de enero de 2017, se impide. Se pueden agregar paquetes de seguridad de terceros (SSP/APs); sin embargo, Windows no admite la eliminación de SSP/APs preconfigurados. En concreto, no se ha admitido nunca la edición de la configuración del registro **HKLM \\ System \\ CurrentControlSet \\ control \\ LSA \\ OSConfig \\ Security Packages** .

A partir de Windows 8.1, los clientes que deseen proporcionar funcionalidad adicional pueden agregar sus paquetes de seguridad mediante la configuración del registro **HKLM \\ System \\ CurrentControlSet \\ control \\ LSA \\ Security Packages** ([registrando dll de SSP/AP](registering-ssp-ap-dlls.md)) y la configuración del registro asociada **SecurityProviders** ([escribir e instalar un proveedor de soporte técnico de seguridad](writing-and-installing-a-security-support-provider.md)), si procede. Además, el propósito de los [paquetes de seguridad](../secgloss/s-gly.md#_security_security_package_gly) es implementar nuevos protocolos de *seguridad* que pueden tener el formato de un proveedor de compatibilidad para seguridad (SSP) o un paquete de [autenticación](../secgloss/a-gly.md#_security_authentication_package_gly) (AP). El propósito de un SSP es proporcionar la *conexión autenticada*, la *integridad del mensaje* y los servicios de *cifrado de mensajes* que aún no se admiten en el sistema, mientras que un AP se usa para agregar una nueva lógica de *autenticación* que se usa para determinar si se permite que un usuario inicie sesión.

Microsoft invierte en la seguridad del cliente y está intentando asegurarse de que los procesos críticos, como SSP y APs, no se pueden deshacer fácilmente del sistema. Por lo tanto, la configuración del registro **HKLM \\ System \\ CurrentControlSet \\ control \\ LSA \\ OSConfig \\ Security Packages** se restringó a partir de Windows 8.1 para evitar cambios en él. Con el fin de facilitar los paquetes de seguridad de terceros, los paquetes de seguridad de la **\\ \\ \\ \\ \\ LSA System CurrentControlSet Control** de la Directiva de usuario se han convertido en el valor designado para SSP/APS personalizados. Además, se recomienda que cualquier funcionalidad de SSP/APs personalizados que esté fuera del ámbito de los paquetes de seguridad definidos por Microsoft se quite de estos SSP o AP personalizados, y que los paquetes de seguridad de bandeja de entrada no se quiten de ningún producto.

 

 
