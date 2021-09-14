---
title: Acceso remoto al Registro en archivos de 64 Windows
description: El redirector del Registro proporciona acceso remoto al registro en un servidor de 64 Windows a través de la función RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- Acceso remoto al Registro de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240914"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Acceso remoto al Registro en archivos de 64 Windows

El redirector del Registro proporciona acceso remoto al registro en un servidor de 64 Windows a través de [**la función RegConnectRegistry.**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya)

Si el cliente es una aplicación de 32 bits, accede a la vista predeterminada del Registro de 32 bits del servidor. Si el cliente es una aplicación de 64 bits, accede a la vista del Registro de 64 bits.

**Windows Server 2003:** Todos los clientes acceden a la vista del Registro de 64 bits a menos que la aplicación use la marca \_ KEY WOW64 \_ 32KEY. Este comportamiento cambió con Windows Server 2003 con Service Pack 1 (SP1) y Windows XP Professional x64 Edition, siempre que el cliente y el servidor ejecuten estas versiones de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redirector del Registro](registry-redirector.md)
</dt> <dt>

[Reflexión del Registro](registry-reflection.md)
</dt> </dl>

 

 