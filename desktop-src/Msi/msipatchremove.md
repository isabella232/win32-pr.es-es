---
description: La propiedad MSIPATCHREMOVE especifica la lista de revisiones que se quitarán durante una instalación.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propiedad MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169766"
---
# <a name="msipatchremove-property"></a>Propiedad MSIPATCHREMOVE

La **propiedad MSIPATCHREMOVE** especifica la lista de revisiones que se quitarán durante una instalación. Las revisiones individuales de la lista están separadas por punto y coma y se pueden representar mediante el GUID del código de revisión o la ruta de acceso completa a la revisión. La [**función MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) y el [**método RemovePatches**](installer-removepatches.md) del [objeto Installer](installer-object.md) establecen la **propiedad MSIPATCHREMOVE.**

La **propiedad MSIPATCHREMOVE** se puede establecer en la línea de comandos como se muestra a continuación para quitar una revisión.

**msiexec /i A: \\Example.msi MSIPATCHREMOVE=c: \\ patches \\ qfe1.msp;{ 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/qb**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




