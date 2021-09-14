---
description: La tabla Extensión contiene información sobre los servidores de extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del Registro.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabla de extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158422"
---
# <a name="extension-table"></a>Tabla de extensiones

La tabla Extensión contiene información sobre los servidores de extensiones de nombre de archivo que se deben generar como parte del anuncio del producto. Cada fila genera un conjunto de claves y valores del Registro.

La tabla Extension contiene las columnas que se muestran en la tabla siguiente.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Extensión   | [Texto](text.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| Progid\_    | [Texto](text.md)             | N   | Y        |
| MIME\_      | [Texto](text.md)             | N   | Y        |
| Característica\_   | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extensión
</dt> <dd>

Extensión asociada a la fila de tabla. La extensión puede tener hasta 255 caracteres. Escriba la extensión en este campo sin el período anterior.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa de la primera columna de la [tabla Component.](component-table.md) Esta columna hace referencia al componente que controla la instalación de la extensión.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>Progid\_
</dt> <dd>

Identificador de programa asociado a esta extensión. Se trata de una clave externa en la [tabla ProgId.](progid-table.md)

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>MIME\_
</dt> <dd>

Tipo de contenido que se va a escribir para la columna Extensión.

Clave externa de la primera columna de la [tabla MIME.](mime-table.md)

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Característica](feature-table.md) que especifica la característica que proporciona el servidor de extensiones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a la tabla Extension cuando se ejecuta [la acción RegisterExtensionInfo](registerextensioninfo-action.md) o la acción [UnRegisterExtensionInfo.](unregisterextensioninfo-action.md)

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

 

 



