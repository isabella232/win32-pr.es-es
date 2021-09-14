---
description: ModuleSignature Table es una tabla obligatoria.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261132"
---
# <a name="modulesignature-table"></a>ModuleSignature Table

ModuleSignature Table es una tabla obligatoria. Contiene toda la información necesaria para identificar un módulo de combinación. La herramienta de combinación agrega esta tabla al .msi archivo si aún no existe. La tabla ModuleSignature de un módulo de combinación solo tiene una fila que contiene ModuleID, Language y Version. Sin embargo, la tabla ModuleSignature de un archivo .msi tiene una fila que contiene esta información para cada archivo .msm que se ha combinado en él.

Las herramientas de combinación y comprobación comprueban la tabla ModuleSignature en los archivos .msi para determinar si tiene todos los módulos de combinación dependientes requeridos por el módulo de combinación actual (vea [ModuleDependency Table](moduledependency-table.md)) y si el paquete de instalación se ha combinado previamente con cualquier módulo de combinación en conflicto (vea [ModuleExclusion Table](moduleexclusion-table.md)).

La tabla ModuleSignature tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [Identificador](identifier.md) | Y   | N        |
| Idioma | [Entero](integer.md)       | Y   | N        |
| Versión  | [Versión](version.md)       |     | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificador que identifica de forma única el módulo de combinación. Dos módulos de combinación no pueden tener el mismo ModuleID a menos que el módulo de combinación sea totalmente compatible con su predecesor. Puede crear un GUID para este campo mediante una utilidad como GUIDGEN. La columna ModuleID es una clave principal para la tabla y, por lo tanto, debe seguir la convención de nomenclatura en Nomenclatura de claves principales en bases de datos [de módulos de mezcla](naming-primary-keys-in-merge-module-databases.md). Por ejemplo, si el nombre legible del módulo de combinación es MyLibrary y el GUID es {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la entrada de la columna ModuleID se convierte en MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lengua
</dt> <dd>

El identificador de idioma especifica el idioma predeterminado para el módulo de combinación. El identificador de idioma está en formato decimal, por ejemplo, inglés de EE. UU. es 1033. El lenguaje utilizado por el módulo de combinación se puede cambiar aplicando una transformación al módulo de combinación antes de la combinación.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versión
</dt> <dd>

El campo Versión contiene una cadena que describe las versiones principales y secundarias del módulo de combinación.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Módulos de combinación de varios idiomas](multiple-language-merge-modules.md)
</dt> </dl>

 

 



