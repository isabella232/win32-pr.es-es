---
description: El paquete de autenticación Kerberos se usa al iniciar sesión en una red; MSV1 0 controla los inicios de sesión \_ locales.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: Kerberos SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83bf0830481640fb4c51dc0760ff91f8816bf66a105a1c51305ad94c06fc284a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140978"
---
# <a name="kerberos-sspap"></a>Kerberos SSP/AP

El [*paquete de*](../secgloss/k-gly.md) autenticación Kerberos se usa al iniciar sesión en una red; MSV1 0 controla los inicios de sesión \_ locales.

Cuando un usuario inicia sesión con una cuenta de red, De forma predeterminada, Kerberos intenta conectarse a Kerberos [*Centro de distribución de claves*](../secgloss/k-gly.md) (KDC) en el controlador de dominio y obtener un vale de concesión de vales (TGT) mediante los datos de inicio de sesión proporcionados por el usuario.

Si un KDC de Kerberos no está disponible, Windows la autenticación MSV1 0 y de paso a través, como se describe en Paquete de autenticación \_ [MSV1 \_ 0](msv1-0-authentication-package.md).

El paquete de autenticación Kerberos admite la versión 5, revisión 6 del protocolo Kerberos. Este protocolo se basa en RFC [4120 de](https://www.ietf.org/rfc/rfc4120.txt)Internet. Para más información, consulte el sitio web de IETF:

[https://www.ietf.org](https://www.ietf.org/)

Para obtener más información sobre Kerberos, vea [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Formatos de credenciales de Kerberos

Las credenciales [*de usuario*](../secgloss/c-gly.md) asignadas por el paquete de autenticación Kerberos después de un intento de inicio de sesión correcto son un vale y una clave de cifrado temporal, a menudo denominada clave [*de sesión*](../secgloss/s-gly.md). El vale contiene una copia cifrada de las credenciales del cliente y la clave de sesión.

 

 
