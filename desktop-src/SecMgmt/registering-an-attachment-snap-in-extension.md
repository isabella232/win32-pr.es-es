---
description: Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que los complementos MMC y Configuración de seguridad la busquen y usen.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registro de una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7af8b586f0071a5718b420612fd552d578bf30bb083cca45a43f38198e1aee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005023"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registro de una extensión de complemento de datos adjuntos

Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que los complementos MMC y Configuración de seguridad la busquen y usen.

El complemento de datos adjuntos debe extender el espacio de nombres de complementos de configuración de seguridad agregando su propio nodo, como se describe en el procedimiento siguiente.

**Para instalar y registrar la extensión de complemento de datos adjuntos**

1.  Registre la extensión de complemento en la siguiente clave del Registro. No cree una clave StandAlone en el complemento; Las extensiones de complementos de datos adjuntos solo deben ser extensiones.

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  Registre la extensión de complemento de datos adjuntos en las subclaves siguientes. Esto puede hacerse como parte de las implementaciones de **funciones DllRegisterServer** y **DllUnregisterServer.**

    [Espacio de nombres de plantillas de](security-templates.md) seguridad:

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

    [Espacio de nombres de análisis y configuración de](security-configuration-and-analysis.md) seguridad:

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

 

 



