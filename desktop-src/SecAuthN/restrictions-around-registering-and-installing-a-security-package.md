---
description: Acciones de paquetes de seguridad que no se admiten en Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restricciones en torno al registro e instalación de un paquete de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160975"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restricciones en torno al registro e instalación de un paquete de seguridad

La eliminación, sustitución o ajuste de paquetes de seguridad de bandeja de entrada (por ejemplo, Kerberos o NTLM) no es una acción admitida en Windows y, a partir del 10 de enero de 2017, se impide. Se pueden agregar paquetes de seguridad de terceros (SSP/AP); sin embargo, Windows no admite la eliminación de SSP/AP preconfigurados. En concreto, nunca se ha admitido la edición de la configuración del Registro **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig \\ Security Packages.**

[A](writing-and-installing-a-security-support-provider.md)partir de Windows 8.1, los clientes que quieran proporcionar funcionalidad adicional pueden agregar sus paquetes de seguridad mediante la configuración del Registro **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ Security Packages** (Registrar archivos DLL de [SSP/AP)](registering-ssp-ap-dlls.md)y la configuración del Registro asociada **SecurityProviders** (Escribir e instalar un proveedor de soporte técnico de seguridad), si procede. Además, el propósito [](../secgloss/s-gly.md#_security_security_package_gly) de los paquetes de seguridad es implementar nuevos *protocolos* de seguridad que pueden tener la forma de un proveedor de soporte técnico de seguridad (SSP) o un paquete de autenticación [(AP).](../secgloss/a-gly.md#_security_authentication_package_gly) El propósito de un SSP es proporcionar la  conexión autenticada, la integridad de los mensajes y los  servicios de cifrado de mensajes que aún no se admiten en el sistema, mientras que se usa una API para agregar una nueva lógica de autenticación que se usa para determinar si se permite que un usuario inicie sesión. 

Microsoft se invierte en la seguridad del cliente y está intentando asegurarse de que los procesos críticos, como los SSP y los AP, no se puedan quitar fácilmente del sistema. Por lo tanto, la configuración del Registro **\\ HKLM SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig \\ Security Packages** se restringió a partir de Windows 8.1 con el fin de evitar cambios en ella. Para facilitar los paquetes de seguridad de terceros, **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ Security Packages** se ha hecho la configuración designada para los SSP/AP personalizados. Además, se recomienda que cualquier funcionalidad de los SSP/AP personalizados que esté fuera del ámbito de los paquetes de seguridad definido por Microsoft se quite de dichos SSP/AP personalizados y que ningún producto quite los paquetes de seguridad de la bandeja de entrada.

 

 
