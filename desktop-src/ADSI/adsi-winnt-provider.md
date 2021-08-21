---
title: Proveedor ADSI WinNT
description: El proveedor adsi de Microsoft implementa un conjunto de objetos ADSI para admitir varias interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- adsi winnt provider ADSI
- ADSI del proveedor de servicios WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb0984b150355099e1609481432f01d9b00be110b64bb82d08a938c02acb7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692795"
---
# <a name="adsi-winnt-provider"></a>Proveedor ADSI WinNT

El proveedor adsi de Microsoft implementa un conjunto de objetos ADSI para admitir varias interfaces ADSI. El nombre del espacio de nombres Windows proveedor es "WinNT" y este proveedor se conoce normalmente como proveedor de WinNT. Para acceder al proveedor de WinNT, enlace a cualquiera de los objetos [ADSI](adsi-objects-of-winnt.md)de WinNT mediante [AdsPath de WinNT.](winnt-adspath.md)

El proveedor WinNT se incluye en el componente del sistema ADSI para Windows y Windows Server.

> [!Note]  
> No se puede suponer que el proveedor de WinNT predeterminado sea completamente seguro para subprocesos. Los escritores de aplicaciones multiproceso deben controlar el multithreading para coordinar correctamente cualquier acceso entre subprocesos mediante el uso adecuado de objetos de sincronización, como semáforos, exclusiones mutuas, secciones críticas, y así sucesivamente.

 

 

 




