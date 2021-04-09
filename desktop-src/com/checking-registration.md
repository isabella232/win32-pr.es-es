---
title: Comprobando registro
description: Comprobando registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994043"
---
# <a name="checking-registration"></a>Comprobando registro

Cada vez que se carga una aplicación, debe comprobar su registro para determinar lo siguiente:

-   Si los CLSID están presentes en el registro. Si no están presentes, la aplicación debe registrarse como la configuración original.
-   Si los CLSID de la aplicación están presentes en el registro pero no tienen ninguna información relacionada con OLE 2. En este caso, la aplicación debe registrarse como la configuración original.
-   Si la ruta de acceso que contiene entradas del servidor ([LocalServer](localserver.md) y [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) y [InProcServer32](inprocserver32.md)y [DefaultIcon](defaulticon.md)) apunta a la ubicación en la que la aplicación está instalada actualmente. Si la ruta de acceso no es, vuelva a escribir las entradas de ruta de acceso para que apunten a la ubicación actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 




