---
title: Instalación de aplicaciones en sistemas de 64 bits
description: El Windows Installer de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalación de la aplicación 64 programación de Windows de bits
- instalación 64 programación de Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149406"
---
# <a name="application-installation-on-64-bit-systems"></a>Instalación de aplicaciones en sistemas de 64 bits

El [Windows Installer de 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en Windows de 64 bits. En el caso de las aplicaciones anteriores que usan un código auxiliar de 16 bits para iniciar un motor de instalación de 32 bits, Windows de 64 bits reconoce programas de instalador específicos de 16 bits y sustituye una versión de 32 bits por puerto.

las aplicaciones DOS de 16 bits, Windows u OS/2 suelen usar un código auxiliar de 16 bits para comprobar el tipo de máquina y, a continuación, iniciar un motor de instalación de 32 bits para realizar realmente la instalación. Para habilitar la instalación de aplicaciones que usan esta técnica 64, Windows sustituye a las versiones de 32 bits de los siguientes programas de instalador de 16 bits:

* Programa de instalación de Microsoft para Windows 1,2  
* Programa de instalación de Microsoft para Windows 2,6  
* Programa de instalación de Microsoft para Windows 3,0  
* Programa de instalación de Microsoft para Windows 3,01  
* InstallShield 5. x  

La lista de sustituciones se almacena en el registro con la siguiente clave: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Este mecanismo solo se proporciona para la compatibilidad con aplicaciones de 32 bits que usan los programas de Microsoft Installer de 16 bits que se enumeran en este tema. No se admite la adición de programas de instalador de terceros.

 

> [!Note]  
> Este mecanismo no se incluye en Windows 10 en ARM.

 

 

 