---
title: Comprobación del registro
description: Comprobación del registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501655"
---
# <a name="checking-registration"></a>Comprobación del registro

Cada vez que se carga una aplicación, debe comprobar su registro para determinar lo siguiente:

-   Si los CLSID están presentes en el Registro. Si no están presentes, la aplicación debe registrarse como configuración original.
-   Si los CLID de la aplicación están presentes en el registro, pero no tienen información relacionada con OLE 2. Si este es el caso, la aplicación debe registrarse como configuración original.
-   Si la ruta de acceso que contiene las entradas del servidor ([LocalServer](localserver.md) y [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)y [DefaultIcon](defaulticon.md)) apunta a la ubicación en la que la aplicación está instalada actualmente. Si la ruta de acceso no lo hace, vuelva a escribir las entradas de ruta de acceso para que apunten a la ubicación actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 




