---
description: Los componentes calificados son un método de direccionamiento indirecto y se pueden usar para agrupar componentes con funcionalidad paralela en categorías.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Uso de componentes calificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254018"
---
# <a name="using-qualified-components"></a>Uso de componentes calificados

Los componentes calificados son un método de direccionamiento indirecto y se pueden usar para agrupar componentes con funcionalidad paralela en categorías.

Para devolver la ruta de acceso completa e instalar un [componente](qualified-components.md)completo, llame a [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).

Para enumerar todos los calificadores de componentes calificados y cadenas descriptivas, llame a [**MsiEnumComponentQualifiers.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)

**Para agrupar componentes en una categoría de componentes calificados**

1.  Debe haber un registro en la tabla [Component](component-table.md) para cada componente incluido en la nueva categoría de componentes calificados. Cree los campos de la tabla Componente de la misma manera que para los componentes normales. Tenga en cuenta que cada componente calificado debe tener un GUID de identificador de componente único especificado en la columna ComponentId de la tabla Component.
2.  Genere una cadena de texto calificador para cada componente calificado. El calificador debe ser una cadena de texto única que se pueda generar fácilmente al buscar un componente completo. Por ejemplo, si los componentes de la categoría están calificados por idioma, el identificador numérico de configuración regional (LCID) es una cadena de calificador razonable.
3.  Agregue un registro en la [tabla PublishComponent para](publishcomponent-table.md) cada componente calificado. Escriba los identificadores de componente calificado de la columna Componente de la tabla Componente en la columna \_ Componente de la tabla PublishComponent. Escriba las cadenas de calificador de cada componente calificado en la columna Calificador. Escriba una cadena localizada que se mostrará al usuario y describa el componente calificado en la columna AppData opcional. Se debe colocar una cadena explicativa en el campo AppData, como "Diccionario de francés", en lugar de simplemente el LCID numérico. Escriba el nombre de la característica que usa este componente en la columna \_ Característica. El identificador de característica de este campo también debe aparecer en la columna Característica de la [tabla Característica](feature-table.md).
4.  Genere un GUID de categoría para esta categoría de componentes calificados. Debe ser un [GUID válido.](guid.md) Si usa una utilidad como GUIDGEN para generar el GUID, asegúrese de que solo contiene letras mayúsculas. Para cada componente calificado de esta categoría, escriba el GUID de categoría en el campo ComponentId de la [tabla PublishComponent](publishcomponent-table.md).

En el ejemplo siguiente se muestra cómo se crea la categoría "Plantillas de FAX" de componentes completos en las tablas Component, Feature y PublishComponent.

[Tabla PublishComponent](publishcomponent-table.md)



| Componentid                  | Calificador: | AppData             | Característica\_   | Componente\_    |
|------------------------------|-----------|---------------------|-------------|----------------|
| {GUID de categoría de plantilla de FAX} | 3082      | Plantilla en inglés de EE. UU. | FAXTemplate | FAXTemplateENU |
|                              | 1041      | Plantilla japonesa   | FAXTemplate | FAXTemplateTEMPLATETEMPLATEN |
|                              | 1054      | Plantilla tailandesa       | FAXTemplate | FAXTemplateTEMPLATE |
|                              | 1031      | Plantilla alemana     | FAXTemplate | FAXTemplateDEU |



 

[Tabla de componentes](component-table.md) (tabla parcial)



| Componente      | Componentid                                  |
|----------------|----------------------------------------------|
| FAXTemplateENU | {*FAX Template (US English) component GUID*} |
| FAXTemplateTEMPLATETEMPLATEN | {*GUID de componente de plantilla de FAX (japonés)*}   |
| FAXTemplateTEMPLATE | {*GUID de componente de plantilla de FAX (tailandés)*}       |
| FAXTemplateDEU | {*GUID de componente de plantilla de FAX (alemán)*}     |



 

[Tabla de características](feature-table.md) (tabla parcial)



| Característica     |
|-------------|
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |
| FAXTemplate |



 

 

 



