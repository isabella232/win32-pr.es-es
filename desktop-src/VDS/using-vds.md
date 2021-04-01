---
description: Uso de VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Uso de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c648c5cc2507c4819f98367c367099248a0e723f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278980"
---
# <a name="using-vds"></a>Uso de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona una interfaz para el desarrollo de scripts y GUI que puede simplificar las actividades realizadas por un administrador de Windows Server que administra un conjunto heterogéneo de sistemas de almacenamiento, migrando datos entre diferentes configuraciones de hardware a lo largo del tiempo. Si no está familiarizado con los objetos que se usan en el desarrollo de VDS, consulte el [modelo de objetos de VDS](vds-object-model.md).

Unos cuantos puntos antes de empezar:

-   Aunque VDS incluye un proveedor de software, debe adquirir un proveedor de hardware y el hardware asociado por separado para aprovechar las operaciones del proveedor de hardware. Para obtener instrucciones de instalación, consulte la documentación proporcionada por el fabricante del hardware.
-   Algunas operaciones requieren volúmenes con formato NTFS. Por ejemplo, al montar un volumen en un directorio existente, el volumen que contiene el directorio debe tener el formato NTFS. Otros sistemas de archivos no admiten esta operación. Para obtener información sobre las operaciones que requieren NTFS, consulte cada página de método en [referencia de VDS](vds-reference.md).

## <a name="programming-languages"></a>Lenguajes de programación

Use cualquier lenguaje de programación que sea adecuado para el desarrollo con COM, como el lenguaje C o C++.

## <a name="security"></a>Seguridad

Firewall de Windows está habilitado de forma predeterminada. Esto puede hacer que la autenticación no se realice correctamente en las interfaces de devolución de llamada, como [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink), que se pueden ejecutar de forma remota. Si el Firewall de Windows está habilitado en el cliente o el servidor, debe agregar administración de volumen remoto a la ficha **excepciones** en firewall de Windows.

**Windows Server 2003:** En Windows Server 2003 con Service Pack 2 (SP2) y Windows Server 2003 con Service Pack 1 (SP1), si firewall de Windows está habilitado en el cliente o el servidor y si el servidor está configurado para usar la autenticación NTLM, debe agregar la siguiente configuración a la pestaña **excepciones** del firewall de Windows para el equipo adecuado.

| Computer                 | Configuración de excepciones                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Equipo cliente (local)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Equipo servidor (remoto) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Tenga en cuenta que el Firewall de Windows no está habilitado de forma predeterminada hasta Windows Server 2003 con SP1.

Una aplicación que usa VDS debe ejecutarse en el operador de copia de seguridad o en la cuenta de grupo de administradores. Sin el privilegio adecuado, una aplicación puede crear un objeto de cargador de servicios, pero el objeto no cargará VDS. En su lugar, devuelve un error que indica que se denegó el acceso a VDS.

Si la red utiliza la autenticación NTLM, el equipo cliente debe permitir el acceso anónimo. En este caso, si el equipo cliente está ejecutando un sistema operativo Windows Server, el acceso anónimo está habilitado de forma predeterminada. Si se está ejecutando un sistema operativo de cliente de Windows, el acceso anónimo debe habilitarse mediante Dcomcnfg.exe.

## <a name="configuration-and-query-operations"></a>Operaciones de configuración y consulta

La configuración y las operaciones de consulta están en el ámbito del equipo, proveedor, subsistema o paquete más relevante. Las consultas solo atraviesan un proveedor o un nivel de la jerarquía de enlace. Para compilar una vista completa, el autor de la llamada debe consultar cada nivel por debajo y hacia abajo. La lista siguiente incluye ejemplos:

-   Para ver todos los discos de un equipo, los autores de la llamada deben consultar todos los proveedores de software de los discos que reclaman dichos proveedores.
-   Para determinar qué discos contribuyen a un volumen apilado por software, los autores de la llamada primero determinan los Plex contribuyentes y luego consultan las extensiones de disco para cada complejo.
-   Para ver todas las unidades conectadas a un subsistema determinado, los autores de la llamada deben consultar el subsistema.
-   Para ver todos los LUN que expone un subsistema determinado, los autores de la llamada deben consultar el subsistema.
-   Para ver todo el almacenamiento en una SAN o un clúster, los autores de la llamada deben consultar todos los proveedores de hardware de cada equipo, consultar cada proveedor para todos los subsistemas y, a continuación, consultar cada subsistema.

Aunque cada consulta individual no devolverá duplicados, las consultas repetidas entre equipos o entre proveedores pueden acumular duplicados. Los llamadores deben implementar cualquier filtrado. Tenga en cuenta también que las aplicaciones de administración de SAN pueden utilizar el Active Directory o un repositorio para conservar la información de configuración. es posible que no sea necesario consultar cada equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de disco virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> <dt>

[Referencia de VDS](vds-reference.md)
</dt> </dl>

 

