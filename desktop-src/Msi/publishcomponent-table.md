---
description: La tabla PublishComponent asocia los componentes enumerados en la tabla Component con una cadena de texto calificadora y un GUID de identificador de categoría.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabla PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069731"
---
# <a name="publishcomponent-table"></a>Tabla PublishComponent

La tabla PublishComponent asocia los componentes enumerados en la [tabla Component](component-table.md) con una cadena de texto calificadora y un GUID de identificador de categoría. Los componentes con funcionalidad paralela que se han agrupado de esta manera se conocen como componentes calificados. Vea [Componentes calificados.](qualified-components.md) Esto proporciona al instalador un método para el direccionamiento indirecto de un solo nivel al hacer referencia a componentes. Consulte [Uso de componentes calificados.](using-qualified-components.md)

La tabla PublishComponent tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Componentid | [GUID](guid.md)             | Y   | N        |
| Calificador:   | [Texto](text.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| AppData     | [Texto](text.md)             | N   | Y        |
| Característica\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

GUID de [cadena](guid.md) que representa la categoría de componentes que se agrupan. Tenga en cuenta que el título de esta columna es engañoso. Este es el GUID de la categoría de componentes calificados y no es el mismo GUID que aparece en la columna ComponentId de la [tabla Component](component-table.md). Aquí hace referencia a un servidor que proporciona la funcionalidad de un componente a clientes externos en lugar del propio componente.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Calificador
</dt> <dd>

Cadena de texto que califica el valor de la columna ComponentId. Un calificador se usa para distinguir varias formas del mismo componente, como un componente que se implementa en varios idiomas. Estas son las cadenas de texto del calificador [**devueltas por MsiEnumComponentQualifiers.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la columna uno de la [tabla Component](component-table.md). Este identificador hace referencia al registro del componente calificado en la tabla Component.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>Appdata
</dt> <dd>

Texto localizable opcional que describe el componente completo de este registro. La aplicación analiza normalmente la cadena y se puede mostrar al usuario. Debe describir el componente completo. Se puede recuperar con [**MsiEnumComponentQualifiers.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa en la columna uno de la [tabla Característica](feature-table.md). Esta es la característica que usa este componente completo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta [la acción PublishComponents](publishcomponents-action.md) o [la acción UnpublishComponents.](unpublishcomponents-action.md)

Tenga en cuenta que el nombre de esta tabla es engañoso. Esta tabla no es necesaria para crear anuncios. Consulte la columna Atributos de la tabla [Componentes y](component-table.md) la [tabla Características](feature-table.md) para obtener información sobre cómo establecer el estado de instalación de los componentes que se anunciarán.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



