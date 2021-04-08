---
description: Microsoft Negotiate es un proveedor de soporte técnico de seguridad que actúa como un nivel de aplicación entre la interfaz del proveedor de compatibilidad para seguridad y el resto de SSP.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001087"
---
# <a name="microsoft-negotiate"></a>Microsoft Negotiate

Microsoft Negotiate es un [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) que actúa como un nivel de aplicación entre la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) ([SSPI](sspi.md)) y el otro SSP. Cuando una aplicación llama en SSPI para iniciar sesión en una red, puede especificar un SSP para que procese la solicitud. Si la aplicación especifica Negotiate, Negotiate analiza la solicitud y elige el mejor SSP para controlar la solicitud en función de la Directiva de seguridad configurada por el cliente.

Actualmente, el paquete de seguridad Negotiate selecciona entre [Kerberos](microsoft-kerberos.md) y [NTLM](microsoft-ntlm.md). Negotiate selecciona Kerberos a menos que no pueda usarse en uno de los sistemas implicados en la autenticación o la aplicación que realiza la llamada no haya proporcionado información suficiente para usar Kerberos.

Para permitir que Negotiate Seleccione el proveedor de seguridad de [Kerberos](microsoft-kerberos.md) , la aplicación cliente debe proporcionar un [*nombre principal de servicio*](../secgloss/s-gly.md) (SPN), un nombre principal de usuario (UPN) o un nombre de cuenta NetBIOS como nombre de destino. De lo contrario, Negotiate siempre selecciona el proveedor de seguridad [NTLM](microsoft-ntlm.md) .

Un servidor que usa el paquete Negotiate puede responder a las aplicaciones cliente que seleccionan específicamente el proveedor de seguridad [Kerberos](microsoft-kerberos.md) o [NTLM](microsoft-ntlm.md) . Sin embargo, una aplicación cliente debe saber que un servidor admite el paquete Negotiate para solicitar autenticación mediante Negotiate. Un servidor que no admita Negotiate no podrá responder siempre a las solicitudes de clientes que especifiquen Negotiate como SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Razones para usar el paquete Negotiate

-   Permite que el sistema use el protocolo disponible más seguro (más seguro).
-   Garantiza la compatibilidad con versiones posteriores de la aplicación.
-   Garantiza que la aplicación exhibe el comportamiento que se ajusta a la Directiva de seguridad establecida por el cliente.

 

 
