---
title: Comprobación del registro
description: Comprobación del registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369675"
---
# <a name="checking-registration"></a>Comprobación del registro

Cada vez que se carga una aplicación, debe comprobar su registro para determinar lo siguiente:

-   Si los CLSID están presentes en el Registro. Si no están presentes, la aplicación debe registrarse como configuración original.
-   Si los CLID de la aplicación están presentes en el registro, pero no tienen información relacionada con OLE 2. Si este es el caso, la aplicación debe registrarse como configuración original.
-   Si la ruta de acceso que contiene las entradas del servidor[(LocalServer](localserver.md) y [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)y [DefaultIcon](defaulticon.md)) apunta a la ubicación en la que la aplicación está instalada actualmente. Si la ruta de acceso no lo hace, vuelva a escribir las entradas de ruta de acceso para que apunten a la ubicación actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 




