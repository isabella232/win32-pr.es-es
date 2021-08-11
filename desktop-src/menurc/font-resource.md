---
title: Recurso FONT
description: Define un archivo que contiene una fuente.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menús de recursos FONT y otros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf08abd68d5d99640435d355609d5647c71116f9fa29c137ba67a311d41f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235277"
---
# <a name="font-resource"></a>Recurso FONT

Define un archivo que contiene una fuente.

``` syntax
nameID FONT filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Valor entero único de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo que contiene el recurso. El nombre debe ser un nombre de archivo válido; debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual. La ruta de acceso debe ser una cadena entre comillas.

</dd> </dl>

Algunos atributos también se admiten para la compatibilidad con versiones anteriores. Para obtener más información, vea [Atributos de recursos comunes](common-resource-attributes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define un único recurso de fuente:

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




