---
title: Recurso HTML
description: Define un archivo HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menús de recursos HTML y otros recursos
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947feb790b5fbee628c846f88595b1ae25db4cfddedbbab223fd05513560d63e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687777"
---
# <a name="html-resource"></a>Recurso HTML

Define un archivo HTML.

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero de 16 bits sin signo que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Nombre del archivo HTML. Debe ser una ruta de acceso completa o relativa si el archivo no está en el directorio de trabajo actual. La ruta de acceso debe ser una cadena entre comillas.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define un recurso HTML:

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




