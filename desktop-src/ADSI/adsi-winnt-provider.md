---
title: Proveedor WinNT de ADSI
description: El proveedor ADSI de Microsoft implementa un conjunto de objetos ADSI para admitir varias interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI del proveedor WinNT ADSI
- ADSI del proveedor de servicios de Winnt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418359"
---
# <a name="adsi-winnt-provider"></a>Proveedor WinNT de ADSI

El proveedor ADSI de Microsoft implementa un conjunto de objetos ADSI para admitir varias interfaces ADSI. El nombre del espacio de nombres para el proveedor de Windows es "WinNT" y este proveedor se conoce comúnmente como proveedor de Winnt. Para tener acceso al proveedor de WinNT, enlace a cualquiera de los [objetos ADSI de WinNT](adsi-objects-of-winnt.md)mediante el [AdsPath de WinNT](winnt-adspath.md).

El proveedor de WinNT se incluye en el componente del sistema ADSI para Windows y Windows Server.

> [!Note]  
> No se puede suponer que el proveedor de WinNT predeterminado sea totalmente seguro para subprocesos. Los escritores de aplicaciones multiproceso deben controlar el multithreading para coordinar correctamente el acceso entre subprocesos mediante el uso correcto de objetos de sincronización como semáforos, exclusiones mutuas, secciones críticas, etc.

 

 

 




