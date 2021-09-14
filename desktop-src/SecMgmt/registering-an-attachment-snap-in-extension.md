---
description: Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que los complementos MMC y Configuración de seguridad la busquen y usen.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registro de una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071128"
---
# <a name="registering-an-attachment-snap-in-extension"></a>Registro de una extensión de complemento de datos adjuntos

Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que los complementos MMC y Configuración de seguridad la busquen y usen.

El complemento de datos adjuntos debe extender el espacio de nombres de complementos de configuración de seguridad agregando su propio nodo como se describe en el procedimiento siguiente.

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

 

 



