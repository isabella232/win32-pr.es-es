---
description: La propiedad de la \_ unidad CCP se establece en la ruta de acceso raíz del volumen extraíble en el que se buscará RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: Propiedad CCP_DRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670745"
---
# <a name="ccp_drive-property"></a>Propiedad de la \_ unidad CCP

La propiedad de la **\_ unidad CCP** se establece en la ruta de acceso raíz del volumen extraíble en el que se buscará [RMCCPSearch](rmccpsearch-action.md). La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.

Esta propiedad se establece normalmente a través de la interfaz de usuario o una acción personalizada. Esta propiedad debe establecerse antes de que se ejecute la acción [RMCCPSearch](rmccpsearch-action.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




