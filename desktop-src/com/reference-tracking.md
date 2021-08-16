---
title: Seguimiento de referencias
description: Seguimiento de referencias
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1321c922cc0a7493e3e4792f7c0f925618330c2e42665296fb06792635a4ea70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309768"
---
# <a name="reference-tracking"></a>Seguimiento de referencias

El seguimiento de referencias puede evitar la liberación anticipada involuntaria o malintencionada de objetos.

Al habilitar el seguimiento de referencias, solicita que COM autentique las llamadas [**a AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuidas. Cuando el seguimiento de referencias está habilitado, COM realiza un seguimiento de los recuentos de referencias por usuario para que un usuario pueda llamar a **Release** solo en los objetos en los que el usuario **llamó anteriormente a AddRef.** Aunque el seguimiento de referencias puede reducir el rendimiento, garantiza que, independientemente de cuántas veces un usuario determinado llame a **Release,** los objetos y los códigos auxiliares seguirán existiendo si otra persona tiene una referencia a ellos.

El cliente puede establecer el seguimiento de referencias para un proceso pasando la marca de funcionalidad EOAC SECURE REFS en una llamada \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). También puede habilitar o deshabilitar el seguimiento de referencias para todas las aplicaciones de un equipo mediante Dcomcnfg.exe.

Si el seguimiento de referencias está habilitado, [**IUnknown siempre**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) usa la configuración de seguridad predeterminada. En este caso, se producirá un error en las llamadas a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) **en IUnknown.**

 

 