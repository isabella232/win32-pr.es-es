---
description: La propiedad INSTALLLEVEL es el nivel inicial en el que se seleccionan las características &\# 0034; en&\# 0034; para la instalación de de forma predeterminada.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propiedad INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690457"
---
# <a name="installlevel-property"></a>Propiedad INSTALLLEVEL

La propiedad **INSTALLLEVEL** es el nivel inicial en el que se seleccionan las características "ON" para la instalación de forma predeterminada. Una característica se instala solo si el valor del campo nivel de la [tabla de características](feature-table.md) es menor o igual que el valor de INSTALLLEVEL actual. El nivel de instalación de cualquier instalación se especifica mediante la propiedad **INSTALLLEVEL** y puede ser un entero comprendido entre 1 y 32.767. Para obtener más información sobre los niveles de instalación, consulte [tabla de características](feature-table.md).

## <a name="default-value"></a>Valor predeterminado

Si no se especifica ningún valor, el valor predeterminado del nivel de instalación es 1.

## <a name="remarks"></a>Observaciones

El nivel de instalación especificado por la propiedad **INSTALLLEVEL** se puede invalidar con las siguientes propiedades:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**RETIRAR**](remove.md)
-   [**REINSTALAR**](reinstall.md)
-   [**ANUNCIA**](advertise.md)

Por ejemplo, al establecer ADDLOCAL = ALL se instalan todas las características localmente, independientemente del valor de la propiedad **INSTALLLEVEL** . Si el valor de la columna LEVEL de la [tabla de características](feature-table.md) es 0, esa característica no se instala y no se muestra en la interfaz de usuario.

Un administrador puede deshabilitar una característica de forma permanente aplicando una transformación de personalización que establezca un 0 en la columna de nivel para esa característica. La aplicación de la transformación de personalización evita la instalación y visualización de la característica incluso si el usuario selecciona una instalación completa mediante la interfaz de usuario o estableciendo ADDLOCAL en ALL en la línea de comandos. Vea [un ejemplo de transformación de personalización](a-customization-transform-example.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




