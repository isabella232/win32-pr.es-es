---
description: El valor de la propiedad ProductVersion es la versión del producto en formato de cadena.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propiedad ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09d2fb436dffba5ae2fa98144d39e5824d09796472297db116a2a4543d55168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074645"
---
# <a name="productversion-property"></a>Propiedad ProductVersion

El valor de la **propiedad ProductVersion** es la versión del producto en formato de cadena. Esta propiedad es REQUIRED.

El formato de la cadena es el siguiente:

<dl> principal.secundario.de compilación  
</dl>

El primer campo es la versión principal y tiene un valor máximo de 255. El segundo campo es la versión secundaria y tiene un valor máximo de 255. El tercer campo se denomina versión de compilación o versión de actualización y tiene un valor máximo de 65 535.

## <a name="remarks"></a>Comentarios

Al menos uno de los tres campos de **ProductVersion** debe cambiar para una actualización mediante la [tabla Upgrade](upgrade-table.md). Cualquier actualización que cambie solo el código del paquete, pero deje **ProductVersion** y [**ProductCode**](productcode.md) sin cambios se denomina actualización [pequeña.](small-updates.md) Los tres campos de versiones se proporcionan principalmente para mayor comodidad. Por ejemplo, si desea cambiar **ProductVersion**, pero no quiere cambiar las versiones principales o secundarias, puede cambiar la versión de compilación.

Tenga en cuenta Windows instalador usa solo los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Aplicación de revisiones y actualizaciones](patching-and-upgrades.md)
</dt> <dt>

[actualización pequeña](small-updates.md)
</dt> </dl>

 

 




