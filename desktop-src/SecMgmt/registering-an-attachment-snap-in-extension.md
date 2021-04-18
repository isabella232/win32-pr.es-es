---
description: Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que MMC y los complementos de configuración de seguridad la encuentren y lo usen.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrar una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686676"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registrar una extensión de complemento de datos adjuntos

Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que MMC y los complementos de configuración de seguridad la encuentren y lo usen.

El complemento de datos adjuntos debe extender el espacio de nombres de los complementos de configuración de seguridad mediante la adición de su propio nodo, tal como se describe en el procedimiento siguiente.

**Para instalar y registrar la extensión del complemento de datos adjuntos**

1.  Registre la extensión del complemento en la siguiente clave del registro. No cree una clave independiente en el complemento; las extensiones de complementos de datos adjuntos solo deben ser extensiones.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registre la extensión del complemento de datos adjuntos en las siguientes subclaves. Esto puede realizarse como parte de las implementaciones de la función **DllRegisterServer** y **DllUnregisterServer** .

    Espacio de nombres de [plantillas de seguridad](security-templates.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    Espacio [de nombres de configuración y análisis de seguridad](security-configuration-and-analysis.md) :

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



