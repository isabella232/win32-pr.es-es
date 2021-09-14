---
description: Después de desarrollar una biblioteca de vínculos dinámicos de paquetes de autenticación/proveedor de compatibilidad de seguridad (DLL de SSP/AP) que contenga uno o varios paquetes de seguridad personalizados, debe registrarlo.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registro de archivos DLL de SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069131"
---
# <a name="registering-sspap-dlls"></a>Registro de archivos DLL de SSP/AP

Después de desarrollar una [*biblioteca*](../secgloss/s-gly.md)de vínculos dinámicos de paquetes de autenticación del proveedor de compatibilidad de seguridad (DLL de SSP/AP) que contiene uno o varios paquetes de seguridad / [](../secgloss/a-gly.md) personalizados, debe registrarlo. [](../secgloss/s-gly.md) Para ello, agregue el nombre del archivo DLL de SSP/AP personalizado a los datos del siguiente valor del Registro:

**HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Lsa** Security \\ **Packages**

Los datos de este valor del Registro son una lista de los nombres de archivos DLL de SSP/AP, sin la extensión ".dll". El tipo de datos de esta lista es **REG \_ MULTI \_ SZ,** por lo que debe haber un carácter nulo ('0') entre cada nombre \\ de ARCHIVO DLL de la lista.

Normalmente, los archivos DLL de SSP/AP se almacenan en el directorio %systemroot%/system32. Si esta es la ruta de acceso al archivo DLL de SSP/AP personalizado, no incluya la ruta de acceso como parte del nombre del archivo DLL. Sin embargo, si el archivo DLL está en una ruta de acceso diferente, incluya la ruta de acceso completa al archivo DLL en el nombre.

Cada vez que se inicia el sistema, el LSA carga los archivos DLL de SSP/AP de esta lista y realiza la secuencia de inicialización descrita en Inicialización en modo [LSA](lsa-mode-initialization.md).

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registro de un paquete de seguridad personalizado como SSP tls predeterminado

Después de desarrollar un proveedor de compatibilidad de seguridad TLS personalizado y registrarlo como se ha descrito anteriormente, también debe registrarlo como el "SSP tls predeterminado". Para ello, rellene el nombre del paquete del SSP personalizado con los datos del siguiente valor del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Lsa** \\ **Default TLS SSP**

Los datos de este valor del Registro son el nombre del paquete de SSP, no el nombre de dll. El tipo de datos de es **REG \_ SZ.**

Las aplicaciones en modo de usuario que usan "SSP tls predeterminado" usarán el valor predeterminado registrado aquí. Este cambio no afectará a las aplicaciones en modo kernel o a las aplicaciones en modo de usuario que usan "Proveedor de protocolo de seguridad unificado de Microsoft" u otros nombres de SSP tls específicos.

> [!Note]  
> Esta información del Registro pertenece solo al archivo DLL de SSP/AP. Para obtener información sobre cómo registrar proveedores de soporte técnico de seguridad (SSP), vea [Escribir e instalar un proveedor de soporte técnico de seguridad](writing-and-installing-a-security-support-provider.md). Para obtener información sobre las diferencias entre archivos DLL de SSP/AP y SSP, vea [SSP/AP frente a SSP](ssp-aps-versus-ssps.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones en torno al registro e instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
