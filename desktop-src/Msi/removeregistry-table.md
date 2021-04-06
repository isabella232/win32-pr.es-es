---
description: La tabla RemoveRegistry contiene la información del registro que la aplicación necesita para eliminar del registro del sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabla RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002198"
---
# <a name="removeregistry-table"></a>Tabla RemoveRegistry

La tabla RemoveRegistry contiene la información del registro que la aplicación necesita para eliminar del registro del sistema.

La tabla RemoveRegistry tiene las columnas siguientes.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identificador](identifier.md) | Y   | N        |
| Root           | [Entero](integer.md)       | N   | N        |
| Clave            | [RegPath](regpath.md)       | N   | N        |
| Nombre           | [Formatea](formatted.md)   | N   | Y        |
| Componente\_    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

La clave de esta tabla.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíces
</dt> <dd>

Clave raíz predefinida para el valor del registro.



| Constante                          | Hexadecimal | Decimal | Clave raíz                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (ninguno)                            | \- 0x001    | -1      | **HKEY \_ El instalador del \_ usuario actual** establece esta clave mientras realiza una instalación por usuario.<br/>                                                                                                                    |
| (ninguno)                            | -0x001      | -1      | **HKEY \_ El instalador del \_ equipo local** establece esta clave mientras se realiza una instalación de todos los usuarios con [**AllUsers**](allusers.md) establecida en 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASES \_ raíz** el instalador quita el valor de la subárbol de **\\ \\ clases de software HKCU** durante las instalaciones en el [contexto de instalación](installation-context.md)por usuario y por equipo.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ Current \_ User**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ local \_ Machine**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **\_usuarios HKEY**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

La clave localizable para el valor del registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre del valor del registro localizable.

La cadena siguiente en la columna Name tiene una importancia especial.



| String | Significado                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | La clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se instale el componente. |



 

Tenga en cuenta que la [tabla del registro](registry-table.md) se debe utilizar para crear o quitar una clave del registro cuando se quita el componente.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la eliminación del valor del registro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La información del registro se elimina del registro del sistema cuando se ha seleccionado el componente correspondiente para instalarse localmente o ejecutarse desde el origen.

Se hace referencia a esta tabla cuando se ejecuta la [acción RemoveRegistryValues](removeregistryvalues-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




