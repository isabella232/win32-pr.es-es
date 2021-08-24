---
description: El instalador establece la propiedad System64Folder en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad System64Folder existente se establece en la carpeta de 32 bits correspondiente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propiedad System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d586451ab596f5b480c74f382659596128a12c041596dec3c530b18307af2820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500435"
---
# <a name="system64folder-property"></a>Propiedad System64Folder

El instalador establece la **propiedad System64Folder** en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad **System64Folder** existente se establece en la carpeta de 32 bits correspondiente.

## <a name="remarks"></a>Comentarios

El instalador establece esta propiedad en archivos de 64 Windows. Por ejemplo, en las ventanas de 64 Windows, el valor puede ser C: \\ Window \\ System32. Esta propiedad no se usa en archivos de 32 Windows.

Normalmente, esta carpeta es un subdirectorio de la Windows carpeta. Sin embargo, reside en un servidor cuando se configura para shared Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




