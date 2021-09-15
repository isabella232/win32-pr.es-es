---
description: Los archivos binarios de Windows Server 2003 con Service Pack 1 (SP1) son compatibles con Windows Vista y Windows Server 2008. Sin embargo, los archivos binarios de versiones anteriores de Windows deben volver a compilarse.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Porte de aplicaciones de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473360"
---
# <a name="porting-backup-applications"></a>Porte de aplicaciones de copia de seguridad

Los archivos binarios de Windows Server 2003 con Service Pack 1 (SP1) son compatibles con Windows Vista y Windows Server 2008. Sin embargo, los archivos binarios de versiones anteriores de Windows deben volver a compilarse.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Porting Windows XP Backup Applications to Windows Vista

Varias interfaces de VSS han cambiado desde Windows XP. Como mínimo, las Windows XP deben volver a compilarse mediante archivos de encabezado y bibliotecas del SDK de VSS 7.2 o del SDK de Windows Vista o Windows Server 2008.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Porting Windows Server 2003 SP1 Backup Applications to Windows Vista

Los archivos binarios de Windows Server 2003 con SP1 son compatibles con Windows Vista y Windows Server 2008. Sin embargo, la mayoría Windows Server 2003 con aplicaciones de copia de seguridad de SP1 deben actualizarse para tener en cuenta las nuevas características, que se describen en las secciones siguientes.

## <a name="compiling-backup-applications-for-windows-vista"></a>Compilar aplicaciones de copia de seguridad para Windows Vista

Las aplicaciones que usan interfaces disponibles en Windows Server 2003 se pueden compilar mediante archivos de encabezado y bibliotecas proporcionados en el SDK de VSS 7.2. Para usar nuevas interfaces, las aplicaciones deben volver a compilarse con los archivos de encabezado y las bibliotecas incluidas en el SDK Windows Vista.

> [!Note]  
> Los archivos binarios compilados con Windows Vista o Windows Server 2008 no son compatibles con Windows Server 2003 con SP1 o versiones anteriores de Windows.

 

 

 



