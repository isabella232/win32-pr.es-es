---
description: La tabla Property contiene los nombres de propiedad y los valores de todas las propiedades definidas en la instalación. Las propiedades con valores NULL no están presentes en la tabla.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Tabla de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a7f72d1ee8cbbf05e39754ba1d06700f7b5d5f2e03c0a7ef3cb9b03b7d00f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145358"
---
# <a name="property-table"></a>Tabla de propiedades

La tabla Property contiene los nombres de propiedad y los valores de todas las propiedades definidas en la instalación. Las propiedades con valores NULL no están presentes en la tabla.

La tabla Property tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Value    | [Texto](text.md)             | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Nombre de una propiedad. Vea [Propiedades](properties.md).

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de cadena localizable para la propiedad . Nunca puede ser Null o una cadena vacía.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta que no se puede usar la tabla Property para establecer una propiedad en el valor de otra propiedad. El instalador no hace nada en la cadena de texto especificada en la columna Valor antes de establecer la propiedad en la columna Propiedad . Si se especifica FirstProperty en la columna Property y SecondProperty en la columna Value, el valor de FirstProperty se establece en la cadena de texto " SecondProperty " y no en el valor de la \[ \] propiedad \[ \] SecondProperty. Esto es necesario para evitar la creación de referencias circulares en la tabla Property. En su lugar, puede establecer una propiedad en otra mediante un [tipo de acción personalizada 51](custom-action-type-51.md).

Tenga en cuenta que [**la propiedad AdminProperties**](adminproperties.md) se puede usar para invalidar los valores de la tabla Property durante [una instalación administrativa.](administrative-installation.md)

No use propiedades para contraseñas u otra información que deba permanecer segura. El instalador puede escribir el valor de una propiedad creada en la tabla Property o creada en tiempo de ejecución en un registro o en el registro del sistema.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE05](ice05.md)  
[ICE06](ice06.md)  
[ICE16](ice16.md)  
[ICE24](ice24.md)  
[ICE31](ice31.md)  
[ICE34](ice34.md)  
[ICE36](ice36.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE52](ice52.md)  
[ICE61](ice61.md)  
[ICE73](ice73.md)  
[ICE74](ice74.md)  
[ICE80](ice80.md)  
[ICE87](ice87.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



