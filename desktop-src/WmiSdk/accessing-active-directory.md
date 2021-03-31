---
description: Active Directory es el servicio de directorio para Windows y es la base de las redes distribuidas de Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Obtener acceso a Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278775"
---
# <a name="accessing-active-directory"></a>Obtener acceso a Active Directory

Active Directory es el servicio de directorio para Windows y es la base de las redes distribuidas de Windows. Puede usar Active Directory para buscar objetos en un dominio de red del equipo, como usuarios, directivas de seguridad, impresoras, componentes distribuidos y otros recursos. El nombre Active Directory hace referencia al servicio de directorio y al propio directorio.

> [!Note]  
> Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

 

Windows hace Active Directory accesible a través de WMI mediante la creación de un conjunto de referencias a cada clase y objeto incluidos en Active Directory. Al tener acceso al proveedor de servicios de directorio a través de WMI, puede crear aplicaciones habilitadas para WMI que puedan tener acceso a la riqueza de la información contenida en Active Directory.

Con estas interfaces, puede:

-   Recuperar clases e instancias.
-   Enumerar clases e instancias.
-   Cree nuevas instancias.
-   Modifique las instancias existentes.
-   Elimine las instancias existentes.
-   Active Directory de consultas.

Los temas siguientes pueden ayudarle a usar Active Directory con WMI:

-   [Usar la sintaxis de Active Directory adecuada](using-the-proper-active-directory-syntax.md)
-   [Asignación de Active Directory a WMI](mapping-active-directory-to-wmi.md)

 

 



