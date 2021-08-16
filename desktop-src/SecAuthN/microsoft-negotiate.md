---
description: Microsoft Negotiate es un proveedor de soporte técnico de seguridad que actúa como una capa de aplicación entre la interfaz del proveedor de soporte técnico de seguridad y los demás SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd223267a2e7d0e4dc23ae356a6fa2e6224c742c491e428369f15fb6d46ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786957"
---
# <a name="microsoft-negotiate"></a>Microsoft Negotiate

Microsoft Negotiate es un proveedor [*de soporte*](../secgloss/s-gly.md) técnico de seguridad [](../secgloss/s-gly.md) (SSP) que actúa como una capa de aplicación entre la interfaz del proveedor de soporte técnico de seguridad [(SSPI)](sspi.md)y los demás SSP. Cuando una aplicación llama en SSPI para iniciar sesión en una red, puede especificar un SSP para que procese la solicitud. Si la aplicación especifica Negotiate, Negotiate analiza la solicitud y elige el mejor SSP para controlar la solicitud en función de la directiva de seguridad configurada por el cliente.

Actualmente, el paquete de seguridad Negotiate selecciona entre [Kerberos](microsoft-kerberos.md) y [NTLM.](microsoft-ntlm.md) Negotiate selecciona Kerberos a menos que no lo pueda usar uno de los sistemas implicados en la autenticación o que la aplicación que realiza la llamada no proporcionara información suficiente para usar Kerberos.

Para permitir que Negotiate seleccione el proveedor de seguridad [kerberos,](microsoft-kerberos.md) la aplicación cliente debe proporcionar un nombre de entidad de seguridad de servicio [](../secgloss/s-gly.md) (SPN), un nombre principal de usuario (UPN) o un nombre de cuenta NetBIOS como nombre de destino. De lo contrario, Negotiate siempre selecciona el [proveedor de seguridad NTLM.](microsoft-ntlm.md)

Un servidor que usa el paquete Negotiate puede responder a las aplicaciones cliente que seleccionan específicamente el proveedor de seguridad [Kerberos](microsoft-kerberos.md) [o NTLM.](microsoft-ntlm.md) Sin embargo, una aplicación cliente debe saber que un servidor admite el paquete Negotiate para solicitar la autenticación mediante Negotiate. Un servidor que no admite Negotiate no siempre puede responder a las solicitudes de los clientes que especifican Negotiate como SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Motivos para usar el paquete Negotiate

-   Permite que el sistema use el protocolo más seguro disponible.
-   Garantiza la compatibilidad de reenvío para la aplicación.
-   Garantiza que la aplicación muestra un comportamiento que se ajuste a la directiva de seguridad establecida por el cliente.

 

 
