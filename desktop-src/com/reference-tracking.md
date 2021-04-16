---
title: Seguimiento de referencias
description: Seguimiento de referencias
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488318"
---
# <a name="reference-tracking"></a>Seguimiento de referencias

El seguimiento de referencias puede evitar la versión temprana accidental o malintencionada de los objetos.

Al habilitar el seguimiento de referencias, se solicita que COM autentique las llamadas [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuidas. Cuando el seguimiento de referencias está habilitado, COM realiza un seguimiento de los recuentos de referencias por usuario para que un usuario pueda llamar a **Release** solo en los objetos en los que el usuario llamó a **AddRef** previamente. Aunque el seguimiento de referencia puede reducir el rendimiento, garantiza que, independientemente del número de veces que un usuario determinado llame a **Release**, los objetos y códigos auxiliares seguirán existiendo si otra persona tiene una referencia a ellos.

El cliente puede establecer el seguimiento de referencia para un proceso pasando la marca de la capacidad de EOAC \_ Secure \_ Refs en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). También puede habilitar o deshabilitar el seguimiento de referencias para todas las aplicaciones de un equipo mediante Dcomcnfg.exe.

Si está habilitado el seguimiento de referencias, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) siempre usa la configuración de seguridad predeterminada. En este caso, se producirá un error en las llamadas a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) en **IUnknown** .

 

 