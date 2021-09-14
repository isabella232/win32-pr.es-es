---
description: La propiedad INSTALLLEVEL es el nivel inicial en el que se seleccionan las características &\# 0034;ON&0034; para la instalación de \# forma predeterminada.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: InstallLEVEL, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072040"
---
# <a name="installlevel-property"></a>InstallLEVEL, propiedad

La **propiedad INSTALLLEVEL** es el nivel inicial en el que las características se seleccionan "ON" para la instalación de forma predeterminada. Solo se instala una característica si el valor del campo Nivel de la tabla [Característica](feature-table.md) es menor o igual que el valor INSTALLLEVEL actual. El nivel de instalación de cualquier instalación se especifica mediante la **propiedad INSTALLLEVEL** y puede ser una integral de 1 a 32 767. Para obtener más información sobre los niveles de instalación, vea [Tabla de características](feature-table.md).

## <a name="default-value"></a>Valor predeterminado

Si no se especifica ningún valor, el nivel de instalación tiene como valor predeterminado 1.

## <a name="remarks"></a>Observaciones

El nivel de instalación especificado por la **propiedad INSTALLLEVEL** se puede reemplazar por las siguientes propiedades:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**ELIMINAR**](remove.md)
-   [**REINSTALAR**](reinstall.md)
-   [**ANUNCIAR**](advertise.md)

Por ejemplo, al establecer ADDLOCAL=ALL se instalan todas las características localmente, independientemente del valor de la **propiedad INSTALLLEVEL.** Si el valor de la columna Nivel de la [tabla Característica](feature-table.md) es 0, esa característica no está instalada y no se muestra en la interfaz de usuario.

Un administrador puede deshabilitar permanentemente una característica aplicando una transformación de personalización que establece un 0 en la columna Nivel de esa característica. La aplicación de la transformación de personalización impide la instalación y presentación de la característica incluso si el usuario selecciona una instalación completa mediante la interfaz de usuario o estableciendo ADDLOCAL en ALL en la línea de comandos. Vea [un ejemplo de transformación de personalización.](a-customization-transform-example.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




