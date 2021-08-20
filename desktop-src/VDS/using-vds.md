---
description: Uso de VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Uso de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6406e938a8fb49314511047bb038ec94a5af9151f5c077ad1fb14984e74474f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125871"
---
# <a name="using-vds"></a>Uso de VDS

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona una interfaz para el scripting y el desarrollo de GUI que puede simplificar las actividades que realiza un administrador de servidor de Windows que administra un conjunto heterogéneo de sistemas de almacenamiento, migrando datos entre distintas configuraciones de hardware a lo largo del tiempo. Si no está familiarizado con los objetos que se usan en el desarrollo de VDS, vea [VDS Object Model](vds-object-model.md).

Algunos puntos antes de empezar:

-   Aunque VDS incluye un proveedor de software, debe adquirir un proveedor de hardware y el hardware asociado por separado para aprovechar las operaciones del proveedor de hardware. Para obtener instrucciones de instalación, consulte la documentación proporcionada por el fabricante del hardware.
-   Algunas operaciones requieren volúmenes con formato NTFS. Por ejemplo, al montar un volumen en un directorio existente, el volumen que contiene el directorio debe tener el formato NTFS. Otros sistemas de archivos no admiten esta operación. Para obtener información sobre las operaciones que requieren NTFS, vea cada página de método en [VDS Reference](vds-reference.md).

## <a name="programming-languages"></a>Lenguajes de programación

Use cualquier lenguaje de programación que sea adecuado para el desarrollo con COM, como el lenguaje C o C++.

## <a name="security"></a>Seguridad

Windows El firewall está habilitado de forma predeterminada. Esto puede hacer que la autenticación no se pueda realizar en interfaces de devolución de llamada, como [**IVdsAdviseSink,**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)que se pueden ejecutar de forma remota. Si Windows firewall está habilitado en el cliente o en el servidor, debe agregar Administración remota de volúmenes a la pestaña Excepciones de Windows Firewall. 

**Windows Server 2003:** En Windows Server 2003 con Service Pack 2 (SP2) y Windows Server 2003 con Service Pack 1 (SP1), si Windows Firewall está habilitado en el cliente o en el  servidor y si el servidor está configurado para usar la autenticación NTLM, debe agregar la siguiente configuración a la pestaña Excepciones de Windows Firewall para el equipo adecuado.

| Computer                 | Configuración de excepciones                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Equipo cliente (local)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Equipo servidor (remoto) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Tenga en cuenta Windows firewall no está habilitado de forma predeterminada hasta Windows Server 2003 con SP1.

Una aplicación que usa VDS debe ejecutarse en la cuenta de grupo Operador de copia de seguridad o Administradores. Sin el privilegio adecuado, una aplicación puede crear un objeto de cargador de servicios, pero el objeto no cargará VDS. En su lugar, devuelve un error que indica que se deniega el acceso a VDS.

Si la red usa la autenticación NTLM, el equipo cliente debe permitir el acceso anónimo. En este caso, si el equipo cliente ejecuta un sistema operativo Windows Server, el acceso anónimo está habilitado de forma predeterminada. Si ejecuta un sistema operativo Windows cliente, el acceso anónimo debe habilitarse mediante Dcomcnfg.exe.

## <a name="configuration-and-query-operations"></a>Operaciones de configuración y consulta

Las operaciones de configuración y consulta están en el ámbito del equipo, proveedor, subsistema o paquete más relevantes. Las consultas recorren solo un proveedor o un nivel de la jerarquía de enlace. Para crear una vista completa, el autor de la llamada debe consultar a través y hacia abajo cada nivel. En la lista siguiente se incluyen ejemplos:

-   Para ver todos los discos de un equipo, los autores de la llamada deben consultar en todos los proveedores de software los discos reclamados por esos proveedores.
-   Para determinar qué discos contribuyen a un volumen apilado por software, los autores de la llamada primero determinan los plexos que contribuyen y, a continuación, consultan las extensiones de disco para cada plex.
-   Para ver todas las unidades que están conectadas a un subsistema determinado, los autores de la llamada deben consultar el subsistema.
-   Para ver todos los LUN expuestos por un subsistema determinado, los autores de la llamada deben consultar el subsistema.
-   Para ver todo el almacenamiento en una SAN o un clúster, los autores de la llamada deben consultar todos los proveedores de hardware de cada equipo, consultar todos los subsistemas de cada proveedor y, a continuación, consultar cada subsistema.

Aunque cada consulta individual no devolverá duplicados, las consultas repetidas entre equipos o entre proveedores pueden acumular duplicados. Los llamadores deben implementar cualquier filtrado. Tenga en cuenta también que las aplicaciones de administración de SAN pueden usar Active Directory o un repositorio para conservar la información de configuración; es posible que no sea necesario consultar cada equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de disco virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> <dt>

[Referencia de VDS](vds-reference.md)
</dt> </dl>

 

