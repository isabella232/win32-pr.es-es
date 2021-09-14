---
description: 'Windows El instalador permite instalar una instancia de un código de producto por contexto y los dos posibles tipos de contexto son los siguientes: MachineUser Si un código de producto permanece sin cambios, solo se puede instalar una instancia en el contexto de la máquina y solo se puede instalar una instancia en cada contexto de usuario. Para que varias instancias permanezcan aisladas, deben tener códigos de producto diferentes y no pueden compartir datos de archivo o datos que no son de archivos. El Windows no puede instalar varias instancias de productos mediante instalaciones simultáneas. Sin embargo, puede instalar varias instancias de un producto si tiene un paquete de instalación independiente para cada instancia de un producto o revisión. A continuación, cada paquete puede mantener su propio conjunto de datos y tener su propio código de producto único. A partir del instalador que ejecuta Windows Server 2003 y Windows XP con Service Pack 1 (SP1), puede instalar varias instancias de un producto mediante transformaciones de código de producto y un paquete .msi o una revisión. También puede usar transformaciones de código de producto para instalar varias instancias de un producto con Windows 2000 con Service Pack 4 (SP4) y Windows Installer&\# 160; 3.0. La única manera de instalar más de una instancia de un producto con versiones anteriores del instalador es tener un paquete de instalación independiente para cada instancia. El uso de transformaciones de instancia reduce significativamente el esfuerzo necesario para admitir varias instancias de un producto. Puede crear un paquete base Windows Installer para un producto y, a continuación, varias transformaciones de instancia que cambien el código del producto y administren los datos de cada instancia. Para obtener más información, vea Creación de varias instancias con transformaciones de instancia e Instalación de varias instancias con transformaciones de instancia.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Instalación de varias instancias de productos y revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3a1de5de7cc63d5eed2e191d77915630761561
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072054"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Instalación de varias instancias de productos y revisiones

Windows El instalador permite instalar una instancia de un código de producto por contexto y los dos tipos posibles de contexto son los siguientes:

-   Máquina
-   Usuario

Si un código de producto permanece sin cambios, solo se puede instalar una instancia en el contexto de la máquina y solo se puede instalar una instancia en cada contexto de usuario.

Para que varias instancias permanezcan aisladas, deben tener códigos de producto diferentes y no pueden compartir datos de archivo o datos que no son de archivos. El Windows no puede instalar varias instancias de productos mediante instalaciones [simultáneas.](concurrent-installations.md) Sin embargo, puede instalar varias instancias de un producto si tiene un paquete de instalación independiente para cada instancia de un producto o revisión. A continuación, cada paquete puede mantener su propio conjunto de datos y tener su propio código de producto único.

A partir del instalador que ejecuta Windows Server 2003 y Windows XP con Service Pack 1 (SP1), puede instalar varias instancias de un producto mediante transformaciones de código de producto y un paquete .msi o una revisión. También puede usar transformaciones de código de producto para instalar varias instancias de un producto con Windows 2000 con Service Pack 4 (SP4) y Windows Installer 3.0. La única manera de instalar más de una instancia de un producto con versiones anteriores del instalador es tener un paquete de instalación independiente para cada instancia.

El uso de transformaciones de instancia reduce significativamente el esfuerzo necesario para admitir varias instancias de un producto. Puede crear un paquete base Windows Installer para un producto y, a continuación, varias transformaciones de instancia que cambien el código del producto y administren los datos de cada instancia.

Para obtener más información, [vea Creación de varias](authoring-multiple-instances-with-instance-transforms.md) instancias con transformaciones de instancia e Instalación de varias instancias con [transformaciones de instancia.](installing-multiple-instances-with-instance-transforms.md)

 

 



