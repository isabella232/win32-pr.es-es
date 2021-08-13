---
description: La propiedad INSTALLLEVEL es el nivel inicial en el que se seleccionan las características \# &0034;ON&0034; para la instalación de \# forma predeterminada.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propiedad INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e349e8d92a2c480866b04a1ca57885ffa1cdb230d8346b357318fa239ead72a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629964"
---
# <a name="installlevel-property"></a>Propiedad INSTALLLEVEL

La **propiedad INSTALLLEVEL** es el nivel inicial en el que las características se seleccionan como "ON" para la instalación de forma predeterminada. Solo se instala una característica si el valor del campo Nivel de la tabla [Característica](feature-table.md) es menor o igual que el valor INSTALLLEVEL actual. El nivel de instalación de cualquier instalación se especifica mediante la **propiedad INSTALLLEVEL** y puede ser un entero de 1 a 32 767. Para obtener más información sobre los niveles de instalación, vea [Tabla de características](feature-table.md).

## <a name="default-value"></a>Valor predeterminado

Si no se especifica ningún valor, el valor predeterminado del nivel de instalación es 1.

## <a name="remarks"></a>Observaciones

El nivel de instalación especificado por la **propiedad INSTALLLEVEL** se puede invalidar mediante las siguientes propiedades:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**eliminar**](remove.md)
-   [**Reinstalar**](reinstall.md)
-   [**Anunciar**](advertise.md)

Por ejemplo, al establecer ADDLOCAL=ALL se instalan todas las características localmente, independientemente del valor de la **propiedad INSTALLLEVEL.** Si el valor de la columna Nivel de la [tabla Característica](feature-table.md) es 0, esa característica no está instalada y no se muestra en la interfaz de usuario.

Un administrador puede deshabilitar permanentemente una característica aplicando una transformación de personalización que establece un valor 0 en la columna Nivel de esa característica. La aplicación de la transformación de personalización impide la instalación y la presentación de la característica incluso si el usuario selecciona una instalación completa mediante la interfaz de usuario o estableciendo ADDLOCAL en ALL en la línea de comandos. Vea [un ejemplo de transformación de personalización.](a-customization-transform-example.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




