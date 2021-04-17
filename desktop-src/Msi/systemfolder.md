---
description: El instalador establece la propiedad Carpetadelsistema en la ruta de acceso completa de la carpeta del sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propiedad Carpetadelsistema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680561"
---
# <a name="systemfolder-property"></a>Propiedad Carpetadelsistema

El instalador establece la propiedad **carpetadelsistema** en la ruta de acceso completa de la carpeta del sistema.

## <a name="remarks"></a>Observaciones

El instalador establece esta propiedad. Por ejemplo, en Windows de 32 bits, el valor puede ser C: \\ Windows \\ system32. En Windows de 64 bits, el valor puede ser C: \\ Windows \\ SysWow64.

Esta carpeta suele ser un subdirectorio de la carpeta Windows. Sin embargo, reside en un servidor cuando se configura para las ventanas compartidas.

Esta carpeta es local, incluso cuando está configurada para ventanas compartidas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




