---
description: Los binarios de Windows Server 2003 con Service Pack 1 (SP1) son compatibles con Windows Vista y Windows Server 2008. Sin embargo, se deben volver a compilar los archivos binarios de versiones anteriores de Windows.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Trasladar aplicaciones de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544971"
---
# <a name="porting-backup-applications"></a>Trasladar aplicaciones de copia de seguridad

Los binarios de Windows Server 2003 con Service Pack 1 (SP1) son compatibles con Windows Vista y Windows Server 2008. Sin embargo, se deben volver a compilar los archivos binarios de versiones anteriores de Windows.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Trasladar aplicaciones de copia de seguridad de Windows XP a Windows Vista

Varias interfaces VSS han cambiado desde Windows XP. Como mínimo, las aplicaciones de Windows XP se deben volver a compilar mediante archivos de encabezado y bibliotecas del SDK de VSS 7,2 o el SDK de Windows Vista o Windows Server 2008.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Trasladar aplicaciones de copia de seguridad de Windows Server 2003 SP1 a Windows Vista

Los archivos binarios de Windows Server 2003 con SP1 son compatibles con Windows Vista y Windows Server 2008. Sin embargo, la mayoría de las aplicaciones de copia de seguridad de Windows Server 2003 con SP1 se deben actualizar para tener en cuenta las nuevas características, que se describen en las secciones siguientes.

## <a name="compiling-backup-applications-for-windows-vista"></a>Compilar aplicaciones de copia de seguridad para Windows Vista

Las aplicaciones que usan interfaces disponibles en Windows Server 2003 se pueden compilar mediante archivos de encabezado y bibliotecas proporcionadas en el SDK de VSS 7,2. Para usar nuevas interfaces, las aplicaciones se deben volver a compilar con los archivos de encabezado y las bibliotecas incluidas en el SDK de Windows Vista.

> [!Note]  
> Los archivos binarios compilados con Windows Vista o Windows Server 2008 no son compatibles con Windows Server 2003 con SP1 o versiones anteriores de Windows.

 

 

 



