---
description: La tabla CreateFolder contiene referencias a las carpetas que se deben crear explícitamente para un componente determinado.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: CreateFolder (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277983"
---
# <a name="createfolder-table"></a>CreateFolder (tabla)

La tabla CreateFolder contiene referencias a las carpetas que se deben crear explícitamente para un componente determinado.

La tabla CreateFolder tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Directorio\_ | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de directorio](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las carpetas de esta tabla se crean cuando se instala el componente. Se realiza un intento de quitar estas carpetas solo cuando el componente se desinstala o se mueve a ejecutar desde el origen. No se desencadena ninguna eliminación automática si las carpetas están vacías. Por el contrario, las carpetas creadas por el instalador pero que no aparecen en esta tabla se quitan cuando están vacías.

Dado que las carpetas creadas por el instalador se eliminan cuando están vacías, debe crear una entrada en la tabla CreateFolder para instalar un componente que se compone de una carpeta vacía.

Se hace referencia a esta tabla cuando se llama a la acción [CreateFolders](createfolders-action.md) o a la acción [RemoveFolders](removefolders-action.md) .

Para obtener información sobre cómo proteger una carpeta, vea la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) y la [tabla LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



