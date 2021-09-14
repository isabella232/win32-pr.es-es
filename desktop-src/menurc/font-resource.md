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
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252399"
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

 

 




