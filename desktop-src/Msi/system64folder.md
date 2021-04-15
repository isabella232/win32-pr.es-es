---
description: El instalador establece la propiedad System64Folder en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad System64Folder existente se establece en la carpeta de 32 bits correspondiente.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propiedad System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653948"
---
# <a name="system64folder-property"></a>Propiedad System64Folder

El instalador establece la propiedad **System64Folder** en la ruta de acceso completa a la carpeta System64 predefinida. La propiedad **System64Folder** existente se establece en la carpeta de 32 bits correspondiente.

## <a name="remarks"></a>Observaciones

El instalador establece esta propiedad en Windows de 64 bits. Por ejemplo, en Windows de 64 bits, el valor puede ser C: \\ Window \\ system32. Esta propiedad no se utiliza en Windows de 32 bits.

Esta carpeta suele ser un subdirectorio de la carpeta Windows. Sin embargo, reside en un servidor cuando se configura para las ventanas compartidas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




