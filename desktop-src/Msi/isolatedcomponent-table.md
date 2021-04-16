---
description: Cada registro de la tabla IsolatedComponent asocia el componente especificado en la columna de aplicación de componentes \_ (normalmente, un archivo. exe) con el componente especificado en la \_ columna compartida componente (normalmente es una DLL compartida).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabla IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686809"
---
# <a name="isolatedcomponent-table"></a>Tabla IsolatedComponent

Cada registro de la tabla IsolatedComponent asocia el componente especificado en la columna de aplicación de componentes \_ (normalmente, un archivo. exe) con el componente especificado en la \_ columna compartida componente (normalmente es una DLL compartida). La [acción IsolateComponents](isolatecomponents-action.md) instala una copia del componente \_ compartido en una ubicación privada para su uso por parte de la aplicación de componentes \_ . Esto aísla la \_ aplicación de componentes de otras copias del componente \_ compartido que se puede instalar en una ubicación compartida del equipo. Vea [componentes aislados](isolated-components.md).

Para vincular un componente \_ compartido a una aplicación de varios componentes \_ , incluya un registro independiente para cada par en la tabla IsolatedComponents. El instalador copia los archivos del componente \_ compartido en el directorio de cada aplicación de componente \_ que está instalada.

La tabla IsolatedComponent tiene las columnas siguientes.



| Columna                 | Tipo                         | Clave | Nullable |
|------------------------|------------------------------|-----|----------|
| Componente \_ compartido      | [Identificador](identifier.md) | Y   | N        |
| Aplicación de componentes \_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ compartido
</dt> <dd>

Clave externa en la [tabla de componentes](component-table.md). Componente que contiene el archivo compartido, normalmente un archivo DLL. La DLL debe ser el archivo de clave de este componente. Debe ser un componente diferente del que se muestra en la \_ columna aplicación de componentes.

El componente compartido controla el registro de todas las copias aisladas del componente y debe tener la marca **msidbComponentAttributesSharedDllRefCount** establecida en la columna Attributes de la tabla de componentes. Esto garantiza que el instalador puede administrar la vida del componente compartido.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Aplicación de componentes \_
</dt> <dd>

Clave externa en la [tabla de componentes](component-table.md). Componente que contiene el. exe que carga el archivo compartido. El archivo. exe debe ser el archivo de clave de este componente. Debe ser un componente diferente del que se muestra en la \_ columna Shared del componente.

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

 

 



