---
description: La propiedad REINSTALLMODE es una cadena que contiene letras que especifican el tipo de reinstalación que se va a realizar.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab48043ef92770cbc3a1f5ab92e459128c9945ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680292"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE (propiedad)

La propiedad **REINSTALLMODE** es una cadena que contiene letras que especifican el tipo de reinstalación que se va a realizar. Las opciones no distinguen mayúsculas de minúsculas y son independientes del orden. Normalmente, esta propiedad siempre se debe utilizar junto con la propiedad [**REINSTALL**](reinstall.md) . Sin embargo, esta propiedad también se puede usar durante la instalación, no solo reinstalar.

> [!Note]  
> El Windows Installer omite la propiedad **REINSTALLMODE** durante una [instalación administrativa](administrative-installation.md).

 

## <a name="reinstall-option-codes"></a>Códigos de opciones de reinstalación

De forma predeterminada, el **REINSTALLMODE** es "OMUs".



| Código | Opción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Vuelva a instalar solo si falta el archivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Vuelva a instalar si falta el archivo o si es una versión anterior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| h    | Vuelva a instalar si falta el archivo o si es una versión igual o anterior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Vuelva a instalar si falta el archivo o hay una versión diferente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Compruebe los valores de la suma de comprobación y reinstale el archivo si faltan o están dañados. Esta marca solo repara archivos que tienen msidbFileAttributesChecksum en la columna Attributes de la [tabla File](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Forzar la reinstalación de todos los archivos, independientemente de la suma de comprobación o la versión.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Vuelva a escribir todas las entradas del registro necesarias de la [tabla del registro](registry-table.md) que van al **\_ \_ usuario actual HKEY**<br/> o **\_ los usuarios HKEY**<br/> subárbol del registro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Vuelva a escribir todas las entradas del registro necesarias de la [tabla del registro](registry-table.md) que vayan al **\_ \_ equipo local HKEY**<br/> o **\_ clases HKEY \_ raíz**<br/> subárbol del registro. Vuelva a escribir toda la información de la [tabla de clases](class-table.md), la [tabla de verbos](verb-table.md), la [tabla PublishComponent](publishcomponent-table.md), la tabla [ProgID](progid-table.md), la tabla [MIME](mime-table.md), la tabla de [iconos](icon-table.md), la tabla de [extensión](extension-table.md)y la [tabla AppID](appid-table.md) , independientemente de la asignación de equipo o usuario. Vuelva a instalar todos los [**componentes calificados.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Al volver a instalar una aplicación, esta opción ejecuta las acciones [RegisterTypeLibraries](registertypelibraries-action.md) y [InstallODBC](installodbc-action.md) .<br/> |
| s    | Reinstalar todos los accesos directos y volver a almacenar en caché todos los iconos que sobrescribirán los accesos directos e iconos existentes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Use para ejecutar desde el paquete de origen y volver a almacenar en caché el paquete local. No utilice el código de la opción de reinstalación de v para la primera instalación de una aplicación o característica.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Si se define la propiedad **REINSTALLMODE** sin definir también la propiedad [**REINSTALL**](reinstall.md) , los modos de "detección" especificados se siguen aplicando y especificando el modo de sobrescritura para una instalación normal. La propiedad **REINSTALLMODE** solo afecta a las características seleccionadas normalmente para la instalación. La presencia de la propiedad **REINSTALLMODE** no reinstala características. La reinstalación de las características requiere la presencia de la propiedad **REINSTALL** .

Los códigos de opción para esta propiedad corresponden a la [opción de línea de comandos](command-line-options.md) '/f '. La opción de línea de comandos tiene un valor predeterminado de ' pecms '.

> [!Note]  
> Solo se comprueban y reparan los archivos que contienen información de suma de comprobación. La \_ marca REINSTALLMODE FILEVERIFY (CCODE anterior) solo repara archivos que tienen msidbFileAttributesChecksum en la columna Attributes de la [tabla File](file-table.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




