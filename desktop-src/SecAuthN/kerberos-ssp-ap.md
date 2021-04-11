---
description: El paquete de autenticación de Kerberos se usa al iniciar sesión en una red; los inicios de sesión locales se controlan mediante MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP/SSP de Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082773"
---
# <a name="kerberos-sspap"></a>SSP/SSP de Kerberos

El paquete de autenticación de [*Kerberos*](../secgloss/k-gly.md) se usa al iniciar sesión en una red; los inicios de sesión locales se controlan mediante MSV1 \_ 0.

Cuando un usuario inicia sesión con una cuenta de red, de forma predeterminada, Kerberos intenta conectarse al [*centro de distribución de claves*](../secgloss/k-gly.md) de Kerberos (KDC) en el controlador de dominio y obtener un vale de concesión de vales (TGT) mediante los datos de inicio de sesión proporcionados por el usuario.

Si un KDC de Kerberos no está disponible, Windows usa MSV1 \_ 0 y la autenticación de paso a través como se describe en el [paquete de \_ autenticación MSV1 0](msv1-0-authentication-package.md).

El paquete de autenticación Kerberos admite la versión 5, revisión 6 del protocolo Kerberos. Este protocolo se basa en el [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)de Internet. Para obtener más información, vea el sitio web de IETF:

[https://www.ietf.org](https://www.ietf.org/)

Para obtener más información acerca de Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Formatos de credenciales de Kerberos

Las [*credenciales*](../secgloss/c-gly.md) de usuario asignadas por el paquete de autenticación Kerberos después de un intento de inicio de sesión correcto son un vale y una clave de cifrado temporal, a menudo denominada [*clave de sesión*](../secgloss/s-gly.md). El vale contiene una copia cifrada de las credenciales del cliente y la clave de sesión.

 

 
