---
title: Instalación de aplicaciones en sistemas de 64 bits
description: El instalador de Windows de 64 bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en aplicaciones de 64 Windows.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalación de aplicaciones de 64 bits Windows programación
- programación de instalación de Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f06eaa527142145791e4ed29e2420d16b1d7a2f4fbe9a77801857a844ed7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643605"
---
# <a name="application-installation-on-64-bit-systems"></a>Instalación de aplicaciones en sistemas de 64 bits

El instalador de Windows de [64](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) bits puede instalar sin problemas aplicaciones basadas en MSI de 32 bits en aplicaciones de 64 Windows. En el caso de las aplicaciones anteriores que usan un código auxiliar de 16 bits para iniciar un motor de instalación de 32 bits, Windows de 64 bits reconoce programas específicos del instalador de 16 bits y sustituye una versión de 32 bits porteada.

Las aplicaciones DOS, Windows o OS/2 de 16 bits suelen usar un código auxiliar de 16 bits para comprobar el tipo de máquina y, a continuación, iniciar un motor de instalación de 32 bits para realizar realmente la instalación. Para habilitar la instalación de aplicaciones que usan esta técnica, el Windows de 64 bits sustituye las versiones de 32 bits por los siguientes programas de instalador de 16 bits:

* Instalación de Microsoft para Windows 1.2  
* Instalación de Microsoft para Windows 2.6  
* Instalación de Microsoft para Windows 3.0  
* Instalación de Microsoft para Windows 3.01  
* InstallShield 5.x  

La lista de sustituciones se almacena en el Registro con la siguiente clave: **HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Este mecanismo solo se proporciona por compatibilidad con aplicaciones de 32 bits que usan los programas de instalador de Microsoft de 16 bits que se enumeran en este tema. No se admite la adición de programas de instalador de terceros.

 

> [!Note]  
> Este mecanismo no se incluye en Windows 10 en ARM.

 

 

 