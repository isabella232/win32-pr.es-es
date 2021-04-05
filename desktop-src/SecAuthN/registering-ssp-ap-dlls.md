---
description: Después de desarrollar un proveedor de compatibilidad de seguridad/biblioteca de vínculos dinámicos (DLL SSP/PA) que contenga uno o varios paquetes de seguridad personalizados, debe registrarlo.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registro de dll de SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813590"
---
# <a name="registering-sspap-dlls"></a>Registro de dll de SSP/AP

Después de desarrollar un paquete de autenticación del [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) / [](../secgloss/a-gly.md) biblioteca de vínculos dinámicos (DLL SSP/PA) que contiene uno o varios [*paquetes de seguridad*](../secgloss/s-gly.md)personalizados, debe registrarlo. Para ello, agregue el nombre del archivo DLL de SSP/AP personalizado a los datos del siguiente valor del registro:

**HKEY \_ \_** Paquetes de \\  \\  \\  \\  \\ **seguridad** de LSA del control System CurrentControlSet de equipo local

Los datos de este valor del registro son una lista de los nombres de los archivos dll de SSP/AP, sin la extensión ". dll". El tipo de datos para esta lista es **reg \_ multi \_ SZ** , por lo que debe haber un carácter nulo (' \\ 0 ') entre cada nombre de dll de la lista.

Normalmente, los archivos dll de SSP/AP se almacenan en el directorio% SystemRoot%/system32 Si esta es la ruta de acceso a la DLL personalizada de SSP/AP, no incluya la ruta de acceso como parte del nombre del archivo DLL. Sin embargo, si el archivo DLL está en una ruta de acceso diferente, incluya la ruta de acceso completa al archivo DLL en el nombre.

Cada vez que se inicia el sistema, LSA carga los archivos dll SSP/AP en esta lista y realiza la secuencia de inicialización descrita en la [inicialización en modo LSA](lsa-mode-initialization.md).

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registro de un paquete de seguridad personalizado como SSP de TLS predeterminado

Después de desarrollar un proveedor de compatibilidad de seguridad de TLS personalizado y registrarlo como se describió anteriormente, también debe registrarlo como "SSP de TLS predeterminado". Para ello, rellene el nombre del paquete de SSP personalizado a los datos del siguiente valor del registro:

**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **control** \\ **LSA** \\ **predeterminado TLS SSP**

Los datos de este valor del registro son el nombre del paquete SSP, no el nombre del archivo dll. El tipo de datos para esta es **reg \_ SZ**.

Las aplicaciones de modo de usuario que usan el "SSP TLS predeterminado" usarán el valor predeterminado registrado aquí. Este cambio no afectará a las aplicaciones en modo kernel ni a las aplicaciones en modo de usuario que usan el "proveedor de protocolo de seguridad unificada de Microsoft" u otros nombres de SSP específicos de TLS.

> [!Note]  
> Esta información del registro pertenece únicamente a la DLL de SSP/PA. Para obtener información sobre cómo registrar proveedores de compatibilidad para seguridad (SSP), consulte [escribir e instalar un proveedor de soporte técnico de seguridad](writing-and-installing-a-security-support-provider.md). Para obtener información acerca de las diferencias entre SSP/AP y dll de SSP, consulte [SSP/APS frente a SSP](ssp-aps-versus-ssps.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones en relación con el registro y la instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
