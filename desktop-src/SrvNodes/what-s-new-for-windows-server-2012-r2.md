---
description: En la lista siguiente se describen las áreas de características nuevas y actualizadas para Windows Server 2012 y Windows Server 2012 R2. Para obtener más información sobre las nuevas tecnologías Windows 8 y Windows 8.1, consulte Windows 8 y Windows 8.1 Technologies.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Novedades: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df654e7c448ef4e4f6f4f1599204883cad11bf5e56ccd13c47c76d204f7587f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867514"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Novedades: Windows Server 2012 R2 & Windows Server 2012

En la lista siguiente se describen las áreas de características nuevas y actualizadas para Windows Server 2012 y Windows Server 2012 R2. Para obtener más información sobre las nuevas tecnologías Windows 8 y Windows 8.1, vea Windows 8 [y Windows 8.1 Technologies](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Novedades de Windows Server 2012 R2

-   [Desduplicación de datos](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    La desduplicación de datos busca y quita la duplicación dentro de los datos de un volumen, al tiempo que garantiza que los datos permanecen correctos y completos. Esto posibilita almacenar más datos de archivo en menos espacio del volumen. Para Windows Server 2012 R2, se activaron varios parámetros y códigos de error, y se agregó la clase [**MSFT \_ DedupFileMetadata.**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata)

-   [Registro de inventario de software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **¡Nuevo!** El registro de inventario de software recopila datos de licencias sobre el software instalado en un servidor de Windows y proporciona acceso remoto a los datos para que un centro de datos pueda agregarlo fácilmente.

-   [Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    La API Servidor de destino iSCSI proporciona proveedores de instrumental de administración de Windows (WMI) para administrar Microsoft Servidor de destino iSCSI, como la creación de discos virtuales y para presentarlos al cliente. Se agregaron varias características nuevas para Windows Server 2012 R2.

-   [Registro de Administración de dispositivos móviles](../mdmreg/mobile-device-management-registration-portal.md)

    **¡Nuevo!** Se ha desarrollado una tendencia del sector en la que los empleados conectan sus dispositivos informáticos móviles personales a la red corporativa y a los recursos (ya sea de forma local o a través de la nube) para realizar tareas en el área de trabajo. Esta tendencia requiere soporte técnico para una configuración sencilla de la red y los recursos, de forma que los empleados puedan registrar dispositivos personales en la empresa con fines relacionados con el trabajo. Las aplicaciones y la tecnología para admitir una configuración sencilla también deben permitir que los profesionales de IT administren el riesgo asociado a tener dispositivos no controlados conectados a la red corporativa. El registro Administración de dispositivos móvil (MDM) inscribe un dispositivo en un servicio de administración.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell es un shell de línea de comandos basado en tareas y un lenguaje de scripting diseñado especialmente para la administración del sistema. Como novedad de Windows Server 2012 R2, Windows PowerShell v4 admite Desired State Configuration, que es una nueva plataforma de administración de Windows PowerShell que permite implementar y administrar datos de configuración para servicios de software y administrar el entorno en el que se ejecutan estos servicios.

## <a name="whats-new-for-windows-server-2012"></a>Novedades de Windows Server 2012

-   [Windows Clustering](/previous-versions/windows/desktop/mscs/windows-clustering)

    Windows La agrupación en clústeres permite administrar clústeres de carga equilibrada de red, así como clústeres de conmutación por error. En esta versión se han agregado varias características nuevas, incluidas nuevas características de administración de grupos, propiedades comunes e integración con WMI.

-   [Registro de acceso de usuarios](/previous-versions/windows/desktop/ual/user-access-logging)

    **¡Nuevo!** El registro de acceso de usuario (UAL) es un marco común para que los roles Windows Server informen de sus respectivas métricas de consumo. Este marco de UAL es un componente fundamental y crítico de la solución de administración de licencias más grande.

-   [Administración remota de Windows](../winrm/portal.md)

    La Administración remota de Windows (WinRM) es la implementación de Microsoft del protocolo WS-Management, un protocolo estándar de acceso a objetos simples basado en SOAP y compatible con firewall que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores. Windows Server 2012 incluye una serie de API de conexión que se centran en interactuar con instancias y shells en ejecución.

-   [Windows Infraestructura de administración](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **¡Nuevo!** Las características Windows Management Infrastructure (MI) de Windows representan la versión más reciente de las tecnologías de instrumental de administración de Windows (WMI), que se basan en el estándar CIM de DMTF (Distributed Management Task Force). MI es totalmente compatible con versiones anteriores de WMI y proporciona una serie de características y ventajas que facilitan el diseño y el desarrollo de proveedores y clientes que nunca.

-   [Desduplicación de datos](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **¡Nuevo!** La desduplicación de datos busca y quita la duplicación dentro de los datos de un volumen, al tiempo que garantiza que los datos permanecen correctos y completos. Esto posibilita almacenar más datos de archivo en menos espacio del volumen.

-   [Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **¡Nuevo!** La API Servidor de destino iSCSI proporciona proveedores de instrumental de administración de Windows (WMI) para administrar Microsoft Servidor de destino iSCSI, como la creación de discos virtuales y para presentarlos al cliente.

-   [Proveedor NFS para WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **¡Nuevo!** El proveedor WMI de NFS proporciona un medio para administrar la configuración de cliente y servidor NFS, recursos compartidos de archivos, grupos de redes y grupos de clientes.

-   [Archivos sin conexión](../devnotes/offline-files.md)

    La API Archivos sin conexión permite a las aplicaciones controlar y supervisar el comportamiento de Archivos sin conexión mediante programación. Windows Server 2012 agrega las funciones [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) y [**RenameItem.**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem)

-   [Administración de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **¡Nuevo!** El servicio SMB API de Administración clases y métodos WMI para administrar recursos compartidos y el acceso a recursos compartidos.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server proporciona opciones de instalación de servidor mínimas para equipos que se ejecutan en el Windows operativo Server 2008 o posterior. Windows Server 2012 ofrece Server Core como una configuración, así como opciones de instalación.

-   [Copias de seguridad de Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    La Windows Copia de seguridad del servidor realiza automáticamente una copia de seguridad y restaura los datos de la aplicación. Windows Server 2012 incluye cloud backup provider API.

-   [Windows Uso compartido de escritorio](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows Uso compartido de escritorio es una tecnología de uso compartido de pantalla de varias partes. Windows Server 2012 implementa esta tecnología mediante la API Windows Duplication.

-   [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md)

    Windows Uso compartido de escritorio permite al usuario acceder de forma remota a una instancia del sistema operativo. Windows Server 2012 incluye una serie de características nuevas, incluidas las sesiones secundarias, RemoteFX redireccionamiento multimedia y el cliente Escritorio remoto Broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell es un shell de línea de comandos basado en tareas y un lenguaje de scripting diseñado especialmente para la administración del sistema. Como novedad Windows Server 2012, Windows PowerShell v3 admite Windows PowerShell Workflow, que aprovecha las ventajas de Windows Workflow Foundation para permitir la automatización de tareas de ejecución larga.

-   [OData de administración](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **¡Nuevo!** También conocido como Windows PowerShell Web Services, Management OData, nuevo en Windows PowerShell v3, permite la creación de un punto de conexión de servicio web de ASP.NET que expone datos de administración, a través de comandos Windows PowerShell, como entidades de servicio web de OData.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Server 2012 R2 en TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 y Windows Server 2012 biblioteca de TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 en Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
