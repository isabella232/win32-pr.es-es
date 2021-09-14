---
description: El valor de la propiedad ProductVersion es la versión del producto en formato de cadena.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propiedad ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069759"
---
# <a name="productversion-property"></a>Propiedad ProductVersion

El valor de la **propiedad ProductVersion** es la versión del producto en formato de cadena. Esta propiedad es REQUIRED.

El formato de la cadena es el siguiente:

<dl> principal.secundario.de compilación  
</dl>

El primer campo es la versión principal y tiene un valor máximo de 255. El segundo campo es la versión secundaria y tiene un valor máximo de 255. El tercer campo se denomina versión de compilación o versión de actualización y tiene un valor máximo de 65 535.

## <a name="remarks"></a>Observaciones

Al menos uno de los tres campos de **ProductVersion** debe cambiar para una actualización mediante la [tabla Upgrade](upgrade-table.md). Cualquier actualización que cambie solo el código del paquete, pero deje **ProductVersion** y [**ProductCode**](productcode.md) sin cambios se denomina actualización [pequeña.](small-updates.md) Los tres campos de versiones se proporcionan principalmente para mayor comodidad. Por ejemplo, si desea cambiar **ProductVersion**, pero no quiere cambiar las versiones principales o secundarias, puede cambiar la versión de compilación.

Tenga en cuenta Windows instalador usa solo los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Revisiones y actualizaciones](patching-and-upgrades.md)
</dt> <dt>

[pequeña actualización](small-updates.md)
</dt> </dl>

 

 




