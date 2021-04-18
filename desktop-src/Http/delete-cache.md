---
title: delete cache
description: Vacía la memoria caché de la dirección URL completa o elimina las entradas según la dirección URL especificada.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- eliminar caché HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "105685666"
---
# <a name="delete-cache"></a>delete cache

Vacía la memoria caché de la dirección URL completa o elimina las entradas según la dirección URL especificada.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[URL = \] * * * cadena*
</dt> <dd>

Obligatorio. Especifica la dirección URL completa.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[Recursive = \] {sí \| no}**
</dt> <dd>

En caso afirmativo, quita todas las entradas de la dirección URL especificada.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**eliminar la dirección URL de caché = https://www.contoso.com:80/myresource/ recursivo = sí**

 

 




