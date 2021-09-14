---
description: Windows El instalador 5.0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de clave para el componente.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Enumeración de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea314ee91c35fb021f5a8da64b6430e8cf950ecd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158478"
---
# <a name="enumerating-components"></a>Enumeración de componentes

Windows El instalador 5.0 que se ejecuta en Windows Server 2008 R2 o Windows 7 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de clave para el componente. Un paquete de Windows Installer 5.0 puede usar las funciones [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)y [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) para buscar componentes y productos en cuentas de usuario y contextos de instalación. Las [**funciones MsiEnumComponents,**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)y [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) solo devuelven información de los componentes y productos instalados para la cuenta de usuario que llamó a la función. Se requieren varias llamadas a estas funciones, al menos una vez para cada cuenta de usuario, para recopilar información de todo el equipo.

La [**función MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) enumera los componentes instalados. La función recupera un código de componente cada vez que se llama a ella. El [**objeto component**](components.md) recibe información sobre un componente instalado por esta función.

La [**función MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) enumera los productos que son clientes de un componente instalado especificado. El [**objeto de**](client.md) cliente recibe información sobre un cliente por esta función.

La [**función MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) devuelve la ruta de acceso completa a un componente instalado. La función devuelve la clave del Registro si la ruta de acceso de la clave del componente es una clave del Registro. El [**objeto ComponentInfo**](componentinfo.md) recibe información sobre un componente instalado por esta función.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta funcionalidad está disponible a partir de Windows Installer 5.0 que se ejecuta en Windows 7 o Windows Server 2008 R2.

 

 



