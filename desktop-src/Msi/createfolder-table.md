---
description: La tabla CreateFolder contiene referencias a carpetas que deben crearse explícitamente para un componente determinado.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: CreateFolder Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cb926f6df388241a9c779328346a6e1bfb9fba4b365afce778c6e0b7a2548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045095"
---
# <a name="createfolder-table"></a>CreateFolder Table

La tabla CreateFolder contiene referencias a carpetas que deben crearse explícitamente para un componente determinado.

La tabla CreateFolder tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Directorio\_ | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directorio\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Directory](directory-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las carpetas de esta tabla se crean cuando se instala el componente. Se intenta quitar estas carpetas solo cuando el componente se desinstala o se mueve a run-from-source. No se desencadena ninguna eliminación automática si las carpetas están vacías. Por el contrario, las carpetas creadas por el instalador pero que no aparecen en esta tabla se quitan cuando están vacías.

Dado que las carpetas creadas por el instalador se eliminan cuando están vacías, debe crear una entrada en la tabla CreateFolder para instalar un componente que consta de una carpeta vacía.

Se hace referencia a esta tabla cuando se llama [a la acción CreateFolders](createfolders-action.md) o [a la acción RemoveFolders.](removefolders-action.md)

Para obtener información sobre cómo proteger una carpeta, vea [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) y [LockPermissions Table](lockpermissions-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 



