---
description: La propiedad REINSTALLMODE es una cadena que contiene letras que especifican el tipo de reinstalación que se va a realizar.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab48043ef92770cbc3a1f5ab92e459128c9945ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069665"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE, propiedad

La **propiedad REINSTALLMODE** es una cadena que contiene letras que especifican el tipo de reinstalación que se va a realizar. Las opciones no tienen en cuenta las mayúsculas y minúsculas y no tienen en cuenta el orden. Normalmente, esta propiedad siempre se debe usar junto con la [**propiedad REINSTALL.**](reinstall.md) Sin embargo, esta propiedad también se puede usar durante la instalación, no solo reinstalar.

> [!Note]  
> El Windows omite la propiedad **REINSTALLMODE** durante una [instalación administrativa.](administrative-installation.md)

 

## <a name="reinstall-option-codes"></a>Reinstalar códigos de opción

De forma **predeterminada, REINSTALLMODE** es "omus".



| Código | Opción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Vuelva a instalar solo si falta el archivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Vuelva a instalar si falta el archivo o si es una versión anterior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| e    | Vuelva a instalar si falta el archivo o si es una versión igual o anterior.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Vuelva a instalar si falta el archivo o hay una versión diferente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Compruebe los valores de suma de comprobación y vuelva a instalar el archivo si faltan o están dañados. Esta marca solo repara los archivos que tienen msidbFileAttributesChecksum en la columna Atributos de la [tabla de archivos](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Fuerce la reinstalación de todos los archivos, independientemente de la suma de comprobación o la versión.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Vuelva a escribir todas las entradas del Registro necesarias de la tabla [del Registro](registry-table.md) que vayan al usuario actual **de \_ \_ HKEY**<br/> o **USUARIOS \_ DE HKEY**<br/> subárbol del registro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Reescriba todas las entradas del Registro necesarias de la [tabla del Registro que](registry-table.md) van a **HKEY LOCAL \_ \_ MACHINE**<br/> o **RAÍZ DE CLASES \_ \_ HKEY**<br/> subárbol del registro. Vuelva a escribir toda la información de la tabla de clases , la tabla [](extension-table.md)de verbos, [](verb-table.md)la tabla [PublishComponent,](publishcomponent-table.md)la tabla [ProgID,](progid-table.md)la tabla [MIME,](mime-table.md)la tabla de [iconos,](icon-table.md)la tabla de extensiones y la [tabla AppID,](appid-table.md) independientemente de la asignación de equipo o usuario. [](class-table.md) Vuelva a instalar [**todos los componentes calificados.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Al reinstalar una aplicación, esta opción ejecuta [las acciones RegisterTypeLibraries](registertypelibraries-action.md) e [InstallODBC.](installodbc-action.md)<br/> |
| s    | Vuelva a instalar todos los accesos directos y vuelva a almacenar en caché todos los iconos sobrescribiendo los accesos directos e iconos existentes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Use para ejecutar desde el paquete de origen y volver a almacenar en caché el paquete local. No use el código de la opción v reinstall para la primera instalación de una aplicación o característica.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Si la **propiedad REINSTALLMODE** se define sin definir también la propiedad [**REINSTALL,**](reinstall.md) los modos de "detección" especificados se siguen aplicando y especifican el modo de sobrescritura para una instalación normal. La **propiedad REINSTALLMODE** solo afecta a las características que se seleccionan normalmente para la instalación. La presencia de la **propiedad REINSTALLMODE** no reinstala las características. La reinstalación de características requiere la presencia de la **propiedad REINSTALL.**

Los códigos de opción de esta propiedad corresponden a la opción [de línea de comandos](command-line-options.md) "/f". La opción de línea de comandos tiene el valor predeterminado "pecms".

> [!Note]  
> Solo se comprueban y reparan los archivos que contienen información de suma de comprobación. La marca REINSTALLMODE FILEVERIFY (el código ccode anterior) solo repara los archivos que tienen \_ msidbFileAttributesChecksum en la columna Atributos de la [tabla de archivos](file-table.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




