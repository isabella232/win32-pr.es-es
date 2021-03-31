---
description: Windows Installer 5,0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave para el componente.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Enumerar componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea314ee91c35fb021f5a8da64b6430e8cf950ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812715"
---
# <a name="enumerating-components"></a>Enumerar componentes

Windows Installer 5,0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave para el componente. Un paquete creado para Windows Installer 5,0 puede usar las funciones [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)y [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) para buscar componentes y productos entre cuentas de usuario y contextos de instalación. Las funciones [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)y [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) solo devuelven información de componentes y productos instalados para la cuenta de usuario que llamó a la función. Se requieren varias llamadas a estas funciones, al menos una vez por cada cuenta de usuario, para recopilar información de todo el equipo.

La función [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) enumera los componentes instalados. La función recupera un código de componente cada vez que se llama. El [**objeto de componente**](components.md) recibe información sobre un componente instalado por esta función.

La función [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) enumera los productos que son clientes de un componente instalado especificado. El [**objeto de cliente**](client.md) recibe información sobre un cliente mediante esta función.

La función [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) devuelve la ruta de acceso completa a un componente instalado. La función devuelve la clave del registro si la ruta de acceso de la clave para el componente es una clave del registro. El [**objeto ComponentInfo**](componentinfo.md) recibe información sobre un componente instalado por esta función.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta funcionalidad está disponible a partir de Windows Installer 5,0 que se ejecuta en Windows 7 o Windows Server 2008 R2.

 

 



