---
description: Establecer la propiedad DISABLEMEDIA impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto. Sin embargo, si la exploración está habilitada, un usuario todavía puede ir a un origen multimedia.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propiedad DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159310"
---
# <a name="disablemedia-property"></a>Propiedad DISABLEMEDIA

Establecer la [**propiedad DISABLEMEDIA**](disablemedia.md) impide que el instalador registre cualquier origen multimedia, como un CD-ROM, como origen válido para el producto. Sin embargo, si la exploración está habilitada, un usuario todavía puede ir a un origen multimedia.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que [**la propiedad DISABLEMEDIA**](disablemedia.md) tiene un efecto diferente al de establecer la directiva DisableMedia. Al **establecer DISABLEMEDIA** se impide el registro de cualquier origen multimedia y esto también impide la primera instalación de una aplicación desde un origen multimedia.

Para obtener más información sobre [](m-gly.md) cómo proteger los orígenes multimedia de la aplicación administrada frente a la exploración y la instalación por parte de usuarios no [administrativos,](source-resiliency.md)vea Resistencia de origen .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




