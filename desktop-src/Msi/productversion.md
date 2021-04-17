---
description: El valor de la propiedad ProductVersion es la versión del producto en formato de cadena.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propiedad ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653794"
---
# <a name="productversion-property"></a>Propiedad ProductVersion

El valor de la propiedad **ProductVersion** es la versión del producto en formato de cadena. Esta propiedad es obligatoria.

El formato de la cadena es el siguiente:

<dl> principal.secundario.de compilación  
</dl>

El primer campo es la versión principal y tiene un valor máximo de 255. El segundo campo es la versión secundaria y tiene un valor máximo de 255. El tercer campo se denomina versión de compilación o versión de actualización y tiene un valor máximo de 65.535.

## <a name="remarks"></a>Observaciones

Al menos uno de los tres campos de **ProductVersion** debe cambiar para una actualización mediante la [tabla de actualización](upgrade-table.md). Cualquier actualización que solo cambie el código de paquete, pero deja **ProductVersion** y [**ProductCode**](productcode.md) sin modificar se denomina una [actualización pequeña](small-updates.md). Los campos de tres versiones se proporcionan principalmente para mayor comodidad. Por ejemplo, si desea cambiar el **ProductVersion** pero no desea cambiar la versión principal o secundaria, puede cambiar la versión de compilación.

Tenga en cuenta que Windows Installer solo utiliza los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Revisiones y actualizaciones](patching-and-upgrades.md)
</dt> <dt>

[actualización pequeña](small-updates.md)
</dt> </dl>

 

 




