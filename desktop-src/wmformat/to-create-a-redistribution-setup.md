---
title: Para crear una configuración de redistribución
description: Para crear una configuración de redistribución
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows SDK de formato multimedia, redistribución de software
- Formato de sistemas avanzados (ASF), redistribución de software
- ASF (formato de sistemas avanzados), redistribución de software
- Windows SDK de formato multimedia, redistribución
- Formato de sistemas avanzados (ASF), redistribución
- ASF (formato de sistemas avanzados), redistribución
- redistribución de software, creación
- redistribución de software, WMFDist.exe
- redistribution,creating
- redistribution,WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360200"
---
# <a name="to-create-a-redistribution-setup"></a>Para crear una configuración de redistribución

1.  Haga que la rutina de instalación instale los archivos de aplicación y realice la configuración necesaria antes de invocar el paquete de redistribución.
2.  Instale WMFDist.exe. Puede usar la marca /Q:A para realizar una instalación silenciosa y desatendida y suprimir la interfaz de usuario de la configuración de redistribución durante la instalación de la aplicación. A continuación, la rutina debe detectar si es necesario reiniciar al final.

    Por ejemplo:

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribución de software**](software-redistribution.md)
</dt> </dl>

 

 




