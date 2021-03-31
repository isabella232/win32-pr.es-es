---
description: Los componentes calificados son un método de direccionamiento indirecto y se pueden usar para agrupar componentes con funcionalidad paralela en categorías.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Uso de componentes calificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154366"
---
# <a name="using-qualified-components"></a>Uso de componentes calificados

Los componentes calificados son un método de direccionamiento indirecto y se pueden usar para agrupar componentes con funcionalidad paralela en categorías.

Para devolver la ruta de acceso completa e instalar un [componente completo](qualified-components.md), llame a [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Para enumerar todos los calificadores de componente cualificados y las cadenas descriptivas, llame a [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

**Para agrupar los componentes en una categoría de componente calificado**

1.  Debe haber un registro en la [tabla de componentes](component-table.md) para cada componente incluido en la nueva categoría de componentes calificados. Cree los campos en la tabla de componentes de la misma forma que para los componentes normales. Tenga en cuenta que cada componente calificado debe tener un GUID de identificador de componente único escrito en la columna ComponentId de la tabla de componentes.
2.  Generar una cadena de texto de calificador para cada componente calificado. El calificador debe ser una cadena de texto única que se pueda generar fácilmente al buscar un componente calificado. Por ejemplo, si los componentes de la categoría se califican por idioma, el identificador numérico de la configuración regional (LCID) es una cadena de calificador razonable.
3.  Agregue un registro en la [tabla PublishComponent](publishcomponent-table.md) para cada componente calificado. Especifique los identificadores de componente completo de la columna componente de la tabla componente en la \_ columna componente de la tabla PublishComponent. Escriba las cadenas de calificador de cada componente calificado en la columna calificador. Escriba una cadena traducida que se mostrará al usuario y que describa el componente calificado en la columna AppData opcional. Se debe colocar una cadena explicativa en el campo AppData, como "Diccionario francés", en lugar de solo el LCID numérico. Escriba el nombre de la característica que usa este componente en la columna de la característica \_ . El identificador de característica de este campo también debe aparecer en la columna característica de la [tabla de características](feature-table.md).
4.  Genere un GUID de categoría para esta categoría de componentes calificados. Debe ser un [GUID](guid.md)válido. Si utiliza una utilidad como GUIDGEN para generar el GUID, asegúrese de que contiene solo letras mayúsculas. Para cada componente calificado en esta categoría, escriba el GUID de la categoría en el campo ComponentId de la [tabla PublishComponent](publishcomponent-table.md).

En el ejemplo siguiente se muestra cómo se crea la categoría de "plantillas de FAX" de los componentes calificados en las tablas componente, característica y PublishComponent.

[Tabla PublishComponent](publishcomponent-table.md)



| ComponentId                  | Qualifier | AppData             | Característica\_   | Componente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID de categoría de plantilla de FAX} | 3082      | Plantilla de Inglés de EE. UU. | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Plantilla en Japonés   | FAXTemplate | FAXTemplateJPN |
|                              | 1054      | Plantilla tailandesa       | FAXTemplate | FAXTemplateTHA |
|                              | 1031      | Plantilla alemana     | FAXTemplate | FAXTemplateDEU |



 

[Tabla de componentes](component-table.md) (tabla parcial)



| Componente      | ComponentId                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*Plantilla de fax (Inglés de EE. UU.) GUID del componente*} |
| FAXTemplateJPN | {*GUID del componente de plantilla de fax (japonés)*}   |
| FAXTemplateTHA | {*GUID del componente de plantilla de fax (tailandés)*}       |
| FAXTemplateDEU | {*GUID del componente de plantilla de fax (alemán)*}     |



 

[Tabla de características](feature-table.md) (tabla parcial)



| Característica     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



