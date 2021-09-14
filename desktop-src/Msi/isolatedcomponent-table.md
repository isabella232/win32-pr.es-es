---
description: Cada registro de la tabla IsolatedComponent asocia el componente especificado en la columna Aplicación de componentes (normalmente un .exe) con el componente especificado en la columna Component Shared (normalmente un \_ archivo DLL \_ compartido).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabla IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071997"
---
# <a name="isolatedcomponent-table"></a>Tabla IsolatedComponent

Cada registro de la tabla IsolatedComponent asocia el componente especificado en la columna Aplicación de componentes (normalmente un .exe) con el componente especificado en la columna Component Shared (normalmente un \_ archivo DLL \_ compartido). La [acción IsolateComponents](isolatecomponents-action.md) instala una copia de Componente compartido en \_ una ubicación privada para que la use la aplicación de \_ componentes. Esto aísla la aplicación de componentes de otras copias de componente compartido que se pueden \_ instalar en una ubicación compartida del \_ equipo. Vea [Componentes aislados](isolated-components.md).

Para vincular un componente compartido a varias aplicaciones de componentes, incluya un registro \_ independiente para cada par en la tabla \_ IsolatedComponents. El instalador copia los archivos de Componente \_ compartido en el directorio de cada aplicación de componente que esté \_ instalada.

La tabla IsolatedComponent tiene las columnas siguientes.



| Columna                 | Tipo                         | Clave | Nullable |
|------------------------|------------------------------|-----|----------|
| Componente \_ compartido      | [Identificador](identifier.md) | Y   | N        |
| Aplicación \_ de componentes | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ compartido
</dt> <dd>

Clave externa en la [tabla Component](component-table.md). Componente que contiene el archivo compartido, normalmente un archivo DLL. El archivo DLL debe ser el archivo de clave para este componente. Debe ser un componente diferente del que aparece en la columna Aplicación \_ de componentes.

El componente compartido controla el registro de todas las copias aisladas del componente y debe tener la marca **msidbComponentAttributesSharedDllRefCount** establecida en la columna Atributos de la tabla Component. Esto garantiza que el instalador pueda administrar la vida útil del componente compartido.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Aplicación \_ de componentes
</dt> <dd>

Clave externa en la [tabla Component](component-table.md). Componente que contiene el .exe que carga el archivo compartido. El .exe debe ser el archivo de clave para este componente. Debe ser un componente diferente del que aparece en la columna \_ Componente compartido.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



