---
title: notify_flag atributo
description: El atributo \notify \_ flag\ proporciona una notificación que identifica si se llama a una rutina de servidor.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag atributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9fb7479667fb9757924dcba765c34138cf01c1ad6645ce7bfdc525be393e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066884"
---
# <a name="notify_flag-attribute"></a>atributo de marca notify \_

El **\[ atributo notify \_ flag \]** proporciona una notificación que identifica si se llama a una rutina de servidor.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*procedure-name* 
</dt> <dd>

Nombre del procedimiento remoto al que está asociado el procedimiento \_ de marca de notificación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **\[ atributo de \_ marca \]** notify es similar en uso al **\[ atributo notify. \]**

El **\[ nombre del procedimiento \_ de \]** marca de notificación es el nombre del procedimiento remoto con el sufijo **\_ de la marca \_ de notificación**. El **\_ procedimiento de \_ marca** de notificación no requiere ningún parámetro y no devuelve un resultado. También se genera un prototipo de este procedimiento en el archivo de encabezado. Por ejemplo, si el archivo IDL contiene lo siguiente:

``` syntax
MyProcedure([in] short S);
```

Especifique lo siguiente en ACF for MIDL para generar la llamada **\_ a la marca \_ de** notificación:

``` syntax
[notify_flag] MyProcedure();
```

El compilador MIDL generará código auxiliar de servidor que contiene la siguiente llamada al procedimiento **\_ de marca \_ de** notificación:

``` syntax
MyProcedure_notify_flag();
```

El archivo de encabezado contendrá un prototipo:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag** es **TRUE si** se llama a la rutina del servidor.

## <a name="examples"></a>Ejemplos

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Notificar**](notify.md)
</dt> </dl>

 

 




