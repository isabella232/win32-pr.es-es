---
title: Para crear una configuración de redistribución
description: Para crear una configuración de redistribución
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- SDK de Windows Media Format, redistribución de software
- Advanced Systems Format (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- SDK de Windows Media Format, redistribución
- Advanced Systems Format (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, crear
- redistribución de software, WMFDist.exe
- redistribución, crear
- redistribución, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268705"
---
# <a name="to-create-a-redistribution-setup"></a>Para crear una configuración de redistribución

1.  Haga que su rutina de instalación Instale los archivos de aplicación y realice la configuración necesaria antes de invocar el paquete de redistribución.
2.  Instale WMFDist.exe. Puede usar la marca/Q: a para realizar una instalación silenciosa y desatendida, y suprimir la interfaz de usuario de la configuración de redistribución durante la instalación de la aplicación. A continuación, la rutina debe detectar si es necesario reiniciar al final.

    Por ejemplo:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribución de software**](software-redistribution.md)
</dt> </dl>

 

 




