---
description: La tabla de extensión contiene información sobre los servidores de extensión de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del registro.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabla de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652529"
---
# <a name="extension-table"></a>Tabla de extensión

La tabla de extensión contiene información sobre los servidores de extensión de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del registro.

La tabla de extensión contiene las columnas que se muestran en la tabla siguiente.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Extensión   | [Texto](text.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| Programa\_    | [Texto](text.md)             | N   | Y        |
| Mine\_      | [Texto](text.md)             | N   | Y        |
| Característica\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension
</dt> <dd>

La extensión asociada a la fila de la tabla. La extensión puede tener una longitud de hasta 255 caracteres. Escriba la extensión en este campo sin el punto anterior.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Una clave externa a la primera columna de la tabla de [componentes](component-table.md) . Esta columna hace referencia al componente que controla la instalación de la extensión.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>Programa\_
</dt> <dd>

IDENTIFICADOR de programa asociado a esta extensión. Se trata de una clave externa en la tabla [ProgID](progid-table.md) .

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>Mine\_
</dt> <dd>

El tipo de contenido que se va a escribir para la columna de extensión.

Una clave externa a la primera columna de la tabla [MIME](mime-table.md) .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_
</dt> <dd>

Una clave externa en la primera columna de la tabla de [características](feature-table.md) que especifica la característica que proporciona el servidor de extensión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a la tabla de extensión cuando se ejecuta la acción [RegisterExtensionInfo](registerextensioninfo-action.md) o la acción [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



