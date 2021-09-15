---
description: Active Directory es el servicio de directorio para Windows y es la base de Windows redes distribuidas.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Acceso a Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465787"
---
# <a name="accessing-active-directory"></a>Acceso a Active Directory

Active Directory es el servicio de directorio para Windows y es la base de Windows redes distribuidas. Puede usar Active Directory para buscar objetos en un dominio de red de equipo, como usuarios, directivas de seguridad, impresoras, componentes distribuidos y otros recursos. El nombre Active Directory hace referencia tanto al servicio de directorio como al propio directorio.

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del [sistema operativo de componentes WMI](operating-system-availability-of-wmi-components.md).

 

Windows hace que Active Directory a través de WMI mediante la creación de un conjunto de referencias a cada clase y objeto incluidos en Active Directory. Al acceder al proveedor de servicios de directorio a través de WMI, puede crear aplicaciones habilitadas para WMI que puedan tener acceso a la gran cantidad de información contenida en Active Directory.

Con estas interfaces, puede:

-   Recuperar clases e instancias.
-   Enumerar clases e instancias.
-   Cree nuevas instancias.
-   Modifique las instancias existentes.
-   Elimine las instancias existentes.
-   Consulta Active Directory.

Los temas siguientes pueden ayudarle a usar Active Directory con WMI:

-   [Usar la sintaxis de Active Directory correcta](using-the-proper-active-directory-syntax.md)
-   [Asignación Active Directory a WMI](mapping-active-directory-to-wmi.md)

 

 



