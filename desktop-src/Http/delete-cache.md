---
title: delete cache
description: Vacía toda la caché de direcciones URL o elimina las entradas según la dirección URL especificada.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- delete cache HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c41f2147f0101f312a7fa76796032ec8c821fcea9c08cf89bb3174ddace43d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870565"
---
# <a name="delete-cache"></a>delete cache

Vacía toda la caché de direcciones URL o elimina las entradas según la dirección URL especificada.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[ url= \]**_cadena_
</dt> <dd>

Obligatorio. Especifica la dirección URL completa.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive= \] {yes \| no}**
</dt> <dd>

En caso afirmativo, quita todas las entradas de la dirección URL especificada.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**delete cache url= https://www.contoso.com:80/myresource/ recursive=yes**

 

 




