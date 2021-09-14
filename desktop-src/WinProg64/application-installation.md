---
title: Instalación de aplicaciones en sistemas de 64 bits
description: El instalador de Windows de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en aplicaciones de 64 Windows.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalación de aplicaciones de 64 bits Windows programación
- instalación de programación de Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068306"
---
# <a name="application-installation-on-64-bit-systems"></a>Instalación de aplicaciones en sistemas de 64 bits

El instalador de Windows de [64](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en aplicaciones de 64 Windows. En el caso de las aplicaciones anteriores que usan un código auxiliar de 16 bits para iniciar un motor de instalación de 32 bits, Windows de 64 bits reconoce programas de instalador de 16 bits específicos y sustituye una versión de 32 bits porteada.

Las aplicaciones DOS, Windows o OS/2 de 16 bits suelen usar un código auxiliar de 16 bits para comprobar el tipo de máquina y, a continuación, iniciar un motor de instalación de 32 bits para realizar realmente la instalación. Para habilitar la instalación de aplicaciones que usan esta técnica, el Windows de 64 bits sustituye las versiones de 32 bits por los siguientes programas de instalador de 16 bits:

* Instalación de Microsoft para Windows 1.2  
* Configuración de Microsoft para Windows 2.6  
* Instalación de Microsoft para Windows 3.0  
* Instalación de Microsoft para Windows 3.01  
* InstallShield 5.x  

La lista de sustituciones se almacena en el Registro con la siguiente clave: **HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Este mecanismo solo se proporciona por compatibilidad con aplicaciones de 32 bits que usan los programas del instalador de Microsoft de 16 bits que se enumeran en este tema. No se admite la adición de programas de instalador de terceros.

 

> [!Note]  
> Este mecanismo no se incluye en Windows 10 en ARM.

 

 

 