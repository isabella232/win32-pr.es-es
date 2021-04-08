---
description: Para tener acceso a una aplicación de servidor COM+ de forma remota desde otro equipo (cliente), el equipo cliente debe tener un subconjunto de los atributos de la aplicación de servidor instalada, incluidos los archivos dll de proxy/stub y las bibliotecas de tipos para la comunicación remota de la interfaz DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Implementación de servidores proxy de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000841"
---
# <a name="deploying-application-proxies"></a>Implementación de servidores proxy de aplicación

Para tener acceso a una aplicación de servidor COM+ de forma remota desde otro equipo (cliente), el equipo cliente debe tener un subconjunto de los atributos de la aplicación de servidor instalada, incluidos los archivos dll de proxy/stub y las bibliotecas de tipos para la comunicación remota de la interfaz DCOM/QC. Este subconjunto se denomina *proxy de aplicación*.

A través de la herramienta administrativa Servicios de componentes, puede exportar fácilmente una aplicación de servidor COM+ como un proxy de aplicación. Para que COM+ genere un proxy de aplicación, es importante que todos los componentes de la aplicación de servidor se hayan instalado y no se hayan importado. (Para obtener más información sobre esta distinción, vea [importar componentes](importing-components.md)). Esto garantiza que la aplicación incluya toda la información de registro necesaria.

> [!Note]  
> Se recomienda separar las definiciones de interfaz de las implementaciones de clase. De lo contrario, el conjunto de dll o bibliotecas de tipos incluidos en el proxy de aplicación COM+ incluirá el código de servidor real.

 

Los proxies de aplicación generados por COM+ son Windows Installer paquetes de instalación. Después de la instalación, los proxies de aplicación aparecen en el panel de control Agregar o quitar programas del equipo cliente (a menos que se modifique el archivo. msi mediante una herramienta de creación de Windows Installer).

## <a name="remote-access-via-application-proxies"></a>Acceso remoto a través de servidores proxy de aplicación

Al generar un proxy de aplicación, COM+ proporciona automáticamente la siguiente información, necesaria para que el proxy de aplicación tenga acceso remoto a una aplicación de servidor COM+:

-   Información de identidad de clase (CLSID y ProgID). Un proxy de aplicación admite hasta dos ProgID.
-   Identidad de la aplicación y relación de las clases con las aplicaciones (AppID).
-   Información de ubicación por aplicación (nombre del servidor remoto).
-   Información de cálculo de referencias para todas las interfaces expuestas por la aplicación (por ejemplo, bibliotecas de tipos y proxy/código auxiliar).
-   Nombres e identificadores de cola MSMQ (si el servicio de componentes en cola está habilitado para la aplicación).
-   Atributos de clase, interfaz y método, excluyendo la información del rol.
-   Atributos de la aplicación.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Instalación de proxy de aplicación en otros sistemas operativos

A diferencia de las aplicaciones de servidor COM+, los proxies de aplicación se pueden instalar en cualquier sistema operativo que admita DCOM (y Windows Installer). En los equipos que no ejecutan COM+, solo se instala el subconjunto de información necesario para la comunicación remota de DCOM. Esta información se instala en el registro de Windows (mediante las \_ claves de clase HKEY \_ raíz, AppID/CLSID).

> [!Note]  
> Al instalar un proxy de aplicación (archivo. msi) en equipos que no ejecutan COM+, es necesario que Windows Installer se ejecute en esos equipos. Se recomienda que los desarrolladores envíen el Windows Installer archivo redistribuible (instmsi.exe) junto con el archivo. msi de la aplicación. Así se asegurará de que los administradores del sistema tienen Windows Installer disponible al implementar servidores proxy de aplicación en clientes que no ejecutan COM+.

 

En los equipos que ejecutan COM+, la información del proxy de aplicación se instala en el catálogo de COM+ y está visible en la herramienta administrativa Servicios de componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear paquetes de instalación para aplicaciones COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[El catálogo de COM+](the-com--catalog.md)
</dt> <dt>

[La utilidad de replicación COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



