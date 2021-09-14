---
description: El instalador establece la propiedad SystemFolder en la ruta de acceso completa de la carpeta System.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propiedad SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069625"
---
# <a name="systemfolder-property"></a>Propiedad SystemFolder

El instalador establece la **propiedad SystemFolder** en la ruta de acceso completa de la carpeta System.

## <a name="remarks"></a>Observaciones

El instalador establece esta propiedad. Por ejemplo, en 32 bits Windows el valor puede ser C: \\ Windows \\ System32. En las Windows de 64 bits, el valor puede ser C: \\ Windows \\ SysWow64.

Normalmente, esta carpeta es un subdirectorio de la Windows carpeta. Sin embargo, reside en un servidor cuando se configura para shared Windows.

Esta carpeta es local, incluso cuando se configura para el Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




