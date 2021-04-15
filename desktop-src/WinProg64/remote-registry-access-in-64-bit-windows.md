---
title: Acceso remoto al registro en Windows de 64 bits
description: El redirector del registro proporciona acceso remoto al registro en Windows de 64 bits a través de la función RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- acceso al registro remoto de 64 bits programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695608"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Acceso remoto al registro en Windows de 64 bits

El redirector del registro proporciona acceso remoto al registro en Windows de 64 bits a través de la función [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Si el cliente es una aplicación de 32 bits, tiene acceso a la vista del registro de 32 bits predeterminada del servidor. Si el cliente es una aplicación de 64 bits, tiene acceso a la vista del registro de 64 bits.

**Windows Server 2003:** Todos los clientes acceden a la vista del registro de 64 bits a menos que la aplicación use la marca de clave \_ WOW64 \_ 32KEY. Este comportamiento cambió con Windows Server 2003 con Service Pack 1 (SP1) y Windows XP Professional x64 Edition, siempre que tanto el cliente como el servidor ejecuten estas versiones de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del registro](registry-redirector.md)
</dt> <dt>

[Reflexión del registro](registry-reflection.md)
</dt> </dl>

 

 