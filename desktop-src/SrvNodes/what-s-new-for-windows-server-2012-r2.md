---
description: En la lista siguiente se describen las áreas de características nuevas y actualizadas para Windows Server 2012 y Windows Server 2012 R2. Para obtener más información sobre las nuevas tecnologías de Windows 8 y Windows 8.1, vea Windows 8 y Windows 8.1 Technologies.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Novedades: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911241"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Novedades: Windows Server 2012 R2 & Windows Server 2012

En la lista siguiente se describen las áreas de características nuevas y actualizadas para Windows Server 2012 y Windows Server 2012 R2. Para obtener más información sobre las nuevas tecnologías de Windows 8 y Windows 8.1, vea [Windows 8 y Windows 8.1 Technologies](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Novedades de Windows Server 2012 R2

-   [Desduplicación de datos](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    La desduplicación de datos busca y elimina la duplicación en los datos de un volumen, a la vez que garantiza que los datos siguen siendo correctos y completos. Esto posibilita almacenar más datos de archivo en menos espacio del volumen. En Windows Server 2012 R2, se han activado varios parámetros y códigos de error, y se ha agregado la clase [**msft \_ DedupFileMetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) .

-   [Registro de inventario de software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **¡Nuevo!** El registro de inventario de software recopila datos de licencias sobre el software instalado en un servidor de Windows y proporciona acceso remoto a los datos para que un centro de datos pueda agregarlos fácilmente.

-   [Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    La API del servidor de destino iSCSI proporciona proveedores de Instrumental de administración de Windows (WMI) para administrar el servidor de destino iSCSI de Microsoft, como la creación de discos virtuales y su presentación en el cliente. Se han agregado varias características nuevas para Windows Server 2012 R2.

-   [Registro de administración de dispositivos móviles](../mdmreg/mobile-device-management-registration-portal.md)

    **¡Nuevo!** Se ha desarrollado una tendencia del sector en la que los empleados conectan sus dispositivos informáticos personales a la red corporativa y los recursos (ya sea de forma local o a través de la nube) para realizar tareas del área de trabajo. Esta tendencia requiere compatibilidad para la configuración sencilla de la red y los recursos, de manera que los empleados puedan registrar dispositivos personales con la empresa para fines de trabajo. Las aplicaciones y la tecnología que admiten la configuración fácil también deben permitir que los profesionales de ti administren el riesgo asociado a tener dispositivos sin control conectados a la red corporativa. El registro de administración de dispositivos móviles (MDM) inscribe un dispositivo en un servicio de administración.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell es un shell de línea de comandos basado en tareas y un lenguaje de scripting diseñado especialmente para la administración del sistema. Como novedad en Windows Server 2012 R2, Windows PowerShell V4 es compatible con la configuración de estado deseado, que es una nueva plataforma de administración de Windows PowerShell que permite implementar y administrar datos de configuración de servicios de software y administrar el entorno en el que se ejecutan estos servicios.

## <a name="whats-new-for-windows-server-2012"></a>Novedades de Windows Server 2012

-   [Agrupación en clústeres de Windows](/previous-versions/windows/desktop/mscs/windows-clustering)

    La organización por clústeres de Windows permite administrar clústeres con equilibrio de carga de red, así como clústeres de conmutación por error. En esta versión se han agregado varias características nuevas, incluidas las nuevas características de administración de grupos, las propiedades comunes y la integración con WMI.

-   [Registro de acceso de usuarios](/previous-versions/windows/desktop/ual/user-access-logging)

    **¡Nuevo!** El registro de acceso de usuarios (UAL) es un marco común para que los roles de Windows Server informen de sus métricas de consumo respectivos. Este marco de trabajo de UAL es un componente fundamental y crítico de la solución de administración de licencias más grande.

-   [Administración remota de Windows](../winrm/portal.md)

    La Administración remota de Windows (WinRM) es la implementación de Microsoft del protocolo WS-Management, un protocolo estándar de acceso a objetos simples basado en SOAP y compatible con firewall que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores. Windows Server 2012 incluye una serie de API de conexión que se centran en interactuar con las instancias y los shells en ejecución.

-   [Infraestructura de administración de Windows](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **¡Nuevo!** Las características de la infraestructura de administración de Windows (MI) representan la versión más reciente de las tecnologías de Instrumental de administración de Windows (WMI), que se basan en el estándar CIM de DMTF (Distributed Management Task Force). MI es totalmente compatible con las versiones anteriores de WMI y proporciona un host de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes.

-   [Desduplicación de datos](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **¡Nuevo!** La desduplicación de datos busca y elimina la duplicación en los datos de un volumen, a la vez que garantiza que los datos siguen siendo correctos y completos. Esto posibilita almacenar más datos de archivo en menos espacio del volumen.

-   [Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **¡Nuevo!** La API del servidor de destino iSCSI proporciona proveedores de Instrumental de administración de Windows (WMI) para administrar el servidor de destino iSCSI de Microsoft, como la creación de discos virtuales y su presentación en el cliente.

-   [Proveedor NFS para WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **¡Nuevo!** El proveedor WMI de NFS proporciona un medio para administrar la configuración de cliente y servidor NFS, recursos compartidos de archivos, netgroups y grupos de clientes.

-   [Archivos sin conexión](../devnotes/offline-files.md)

    La API de Archivos sin conexión permite a las aplicaciones controlar y supervisar el comportamiento de Archivos sin conexión mediante programación. Windows Server 2012 agrega las funciones [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) y [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) .

-   [Administración de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **¡Nuevo!** La API de administración de SMB proporciona clases y métodos de WMI para administrar los recursos compartidos y el acceso compartido.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server proporciona opciones mínimas de instalación de servidor para equipos que ejecutan el sistema operativo Windows Server 2008 o posterior. Windows Server 2012 ofrece Server Core como configuración y como opciones de instalación.

-   [Copias de seguridad de Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    La característica Copias de seguridad de Windows Server realiza automáticamente una copia de seguridad y restaura los datos de la aplicación. Windows Server 2012 incluye la API del proveedor de copias de seguridad en la nube.

-   [Uso compartido del escritorio de Windows](/previous-versions/windows/desktop/rdp/rdp-portal)

    El uso compartido de escritorio de Windows es una tecnología de uso compartido de pantalla de varias partes. Windows Server 2012 implementa esta tecnología mediante la API de duplicación de Windows.

-   [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md)

    El uso compartido del escritorio de Windows permite al usuario acceder de forma remota a una instancia del sistema operativo. Windows Server 2012 incluye una serie de características nuevas, como las sesiones secundarias, la redirección de medios RemoteFX y el cliente de Escritorio remoto Broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell es un shell de línea de comandos basado en tareas y un lenguaje de scripting diseñado especialmente para la administración del sistema. Como novedad en Windows Server 2012, Windows PowerShell V3 es compatible con el flujo de trabajo de Windows PowerShell, que aprovecha las ventajas de Windows Workflow Foundation para permitir la automatización de tareas de ejecución prolongada.

-   [Management OData](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **¡Nuevo!** También conocido como servicios Web de Windows PowerShell, Management OData, nuevo en Windows PowerShell V3, permite la creación de un punto de conexión de servicio Web ASP.NET que exponga los datos de administración, mediante los comandos de Windows PowerShell, como entidades de servicio Web de OData.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Server 2012 R2 en TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 y Windows Server 2012 en la biblioteca de TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 en Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
