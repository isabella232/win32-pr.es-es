---
description: Para acceder a una aplicación de servidor COM+ de forma remota desde otro equipo (cliente), el equipo cliente debe tener instalado un subconjunto de los atributos de la aplicación de servidor, incluidos los archivos DLL de proxy/stub y las bibliotecas de tipos para la comunicación remota de la interfaz DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Implementación de servidores proxy de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264535"
---
# <a name="deploying-application-proxies"></a>Implementación de servidores proxy de aplicación

Para acceder a una aplicación de servidor COM+ de forma remota desde otro equipo (cliente), el equipo cliente debe tener instalado un subconjunto de los atributos de la aplicación de servidor, incluidos los archivos DLL de proxy/stub y las bibliotecas de tipos para la comunicación remota de la interfaz DCOM/QC. Este subconjunto se denomina proxy *de aplicación.*

A través de la herramienta administrativa Servicios de componentes, puede exportar fácilmente una aplicación de servidor COM+ como proxy de aplicación. Para que COM+ genere un proxy de aplicación, es importante que todos los componentes de la aplicación de servidor se instalaron y no se importaron. (Para obtener más información sobre esta distinción, vea [Importar componentes).](importing-components.md) Esto garantiza que la aplicación incluya toda la información de registro necesaria.

> [!Note]  
> Se recomienda separar las definiciones de interfaz de las implementaciones de clase. De lo contrario, el conjunto de archivos DLL o bibliotecas de tipos incluido en el proxy de aplicación COM+ incluirá código de servidor real.

 

Los servidores proxy de aplicación generados por COM+ Windows paquetes de instalación del instalador. Después de la instalación, los servidores proxy de aplicación aparecen en el panel de control Agregar o quitar programas del equipo cliente (a menos que el archivo .msi se modifique mediante una herramienta de creación de Windows Installer).

## <a name="remote-access-via-application-proxies"></a>Acceso remoto a través de Application Proxies

Al generar un proxy de aplicación, COM+ proporciona automáticamente la siguiente información, necesaria para que el proxy de aplicación acceda de forma remota a una aplicación de servidor COM+:

-   Información de identidad de clase (CLID y ProgID). Un proxy de aplicación admite hasta dos ProgID.
-   Identidad de aplicación y relación de clases con aplicaciones (AppID).
-   Información de ubicación por aplicación (nombre del servidor remoto).
-   Serialización de información para todas las interfaces expuestas por la aplicación (por ejemplo, bibliotecas de tipos y proxy/stubs).
-   Nombres e identificadores de cola de MSMQ (si el servicio de componentes en cola está habilitado para la aplicación).
-   Atributos de clase, interfaz y método, excepto la información de roles.
-   Atributos de aplicación.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Instalación de servidores proxy de aplicación en otros sistemas operativos

A diferencia de las aplicaciones de servidor COM+, los servidores proxy de aplicación se pueden instalar en cualquier sistema operativo que admita DCOM (y Windows Instalador). En equipos que no ejecutan COM+, solo se instala el subconjunto de información necesaria para la comunicación remota de DCOM. Esta información se instala en el registro Windows (mediante las claves HKEY \_ CLASSES \_ ROOT, APPID/CLSID).

> [!Note]  
> Al instalar un proxy de aplicación (.msi archivo) en equipos que no ejecutan COM+, es necesario tener un instalador Windows que se ejecute en esos equipos. Se recomienda que los desarrolladores envíe el archivo redistribuible Windows Installer (instmsi.exe) junto con el archivo de .msi aplicación. Esto garantizará que los administradores del sistema Windows instalador disponible al implementar servidores proxy de aplicación en clientes que no ejecutan COM+.

 

En equipos que ejecutan COM+, la información del proxy de aplicación se instala en el catálogo de COM+ y es visible en la herramienta administrativa Servicios de componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear paquetes de instalación para aplicaciones COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[El catálogo de COM+](the-com--catalog.md)
</dt> <dt>

[Utilidad de replicación COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



