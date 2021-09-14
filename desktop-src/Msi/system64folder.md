---
description: El instalador establece la propiedad System64Folder en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad System64Folder existente se establece en la carpeta de 32 bits correspondiente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propiedad System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069629"
---
# <a name="system64folder-property"></a>Propiedad System64Folder

El instalador establece la **propiedad System64Folder** en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad **System64Folder** existente se establece en la carpeta de 32 bits correspondiente.

## <a name="remarks"></a>Observaciones

El instalador establece esta propiedad en archivos de 64 Windows. Por ejemplo, en las ventanas de 64 Windows, el valor puede ser C: \\ Window \\ System32. Esta propiedad no se usa en archivos de 32 Windows.

Normalmente, esta carpeta es un subdirectorio de la Windows carpeta. Sin embargo, reside en un servidor cuando se configura para shared Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




