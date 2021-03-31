---
description: 'Windows Installer permite que se instale una instancia de un código de producto por contexto, y los dos tipos posibles de contexto son los siguientes: MachineUser si un código de producto permanece inalterado, solo se puede instalar una instancia en el contexto del equipo y solo se puede instalar una instancia en cada contexto de usuario. Para que varias instancias permanezcan aisladas, deben tener distintos códigos de producto y no pueden compartir datos de archivos o datos que no son de archivo. El Windows Installer no puede instalar varias instancias de productos con instalaciones simultáneas. Sin embargo, puede instalar varias instancias de un producto si tiene un paquete de instalación independiente para cada instancia de un producto o revisión. Después, cada paquete puede mantener su propio conjunto de datos y tener su propio código de producto único. A partir del instalador que ejecuta Windows Server 2003 y Windows XP con Service Pack 1 (SP1), puede instalar varias instancias de un producto mediante el uso de transformaciones de código de producto y un paquete. msi o una revisión. También puede usar transformaciones de código de producto para instalar varias instancias de un producto con Windows 2000 con Service Pack 4 (SP4) y Windows Installer&\# 160; 3,0. La única manera de instalar más de una instancia de un producto con versiones anteriores del instalador es tener un paquete de instalación independiente para cada instancia. El uso de transformaciones de instancias reduce significativamente el esfuerzo necesario para admitir varias instancias de un producto. Puede crear un paquete de Windows Installer base para un producto y, a continuación, varias transformaciones de instancia que cambian el código de producto y administran los datos de cada instancia. Para obtener más información, vea crear varias instancias con transformaciones de instancia e instalar varias instancias con transformaciones de instancia.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Instalación de varias instancias de productos y revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3a1de5de7cc63d5eed2e191d77915630761561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278811"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Instalación de varias instancias de productos y revisiones

Windows Installer permite que se instale una instancia de un código de producto por contexto, y los dos tipos posibles de contexto son los siguientes:

-   Máquina
-   Usuario

Si un código de producto permanece inalterado, solo se puede instalar una instancia en el contexto del equipo y solo se puede instalar una instancia en cada contexto de usuario.

Para que varias instancias permanezcan aisladas, deben tener distintos códigos de producto y no pueden compartir datos de archivos o datos que no son de archivo. El Windows Installer no puede instalar varias instancias de productos con [instalaciones simultáneas](concurrent-installations.md). Sin embargo, puede instalar varias instancias de un producto si tiene un paquete de instalación independiente para cada instancia de un producto o revisión. Después, cada paquete puede mantener su propio conjunto de datos y tener su propio código de producto único.

A partir del instalador que ejecuta Windows Server 2003 y Windows XP con Service Pack 1 (SP1), puede instalar varias instancias de un producto mediante el uso de transformaciones de código de producto y un paquete. msi o una revisión. También puede usar transformaciones de código de producto para instalar varias instancias de un producto con Windows 2000 con Service Pack 4 (SP4) y Windows Installer 3,0. La única manera de instalar más de una instancia de un producto con versiones anteriores del instalador es tener un paquete de instalación independiente para cada instancia.

El uso de transformaciones de instancias reduce significativamente el esfuerzo necesario para admitir varias instancias de un producto. Puede crear un paquete de Windows Installer base para un producto y, a continuación, varias transformaciones de instancia que cambian el código de producto y administran los datos de cada instancia.

Para obtener más información, vea [crear varias instancias con transformaciones de instancia](authoring-multiple-instances-with-instance-transforms.md) e [instalar varias instancias con transformaciones de instancia](installing-multiple-instances-with-instance-transforms.md).

 

 



