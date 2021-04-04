---
title: notify_flag atributo)
description: El atributo \ Notify \_ Flag \ proporciona una notificación que identifica si se llama a una rutina de servidor.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag el atributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076574"
---
# <a name="notify_flag-attribute"></a>atributo de marca de notificación \_

El atributo **\[ Notify \_ Flag \]** proporciona una notificación que identifica si se llama a una rutina de servidor.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*procedimiento: nombre* 
</dt> <dd>

Nombre del procedimiento remoto con el que \_ está asociado el procedimiento de marca de notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ Notify \_ Flag \]** es similar en el uso del atributo **\[ Notify \]** .

El nombre del procedimiento de **\[ \_ marca \] de notificación** es el nombre del procedimiento remoto con el sufijo de la **\_ \_ marca de notificación**. El procedimiento **\_ Notify \_ Flag** no requiere ningún parámetro y no devuelve un resultado. También se genera un prototipo de este procedimiento en el archivo de encabezado. Por ejemplo, si el archivo IDL contiene lo siguiente:

``` syntax
MyProcedure([in] short S);
```

Especifique lo siguiente en ACF para MIDL a fin de generar la llamada a la **\_ \_ marca de notificación** :

``` syntax
[notify_flag] MyProcedure();
```

El compilador MIDL generará código auxiliar de servidor que contiene la siguiente llamada al procedimiento de **\_ \_ marca de notificación** :

``` syntax
MyProcedure_notify_flag();
```

El archivo de encabezado contendrá un prototipo:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag** es **true** si se llama a la rutina de servidor.

## <a name="examples"></a>Ejemplos

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**notificar a**](notify.md)
</dt> </dl>

 

 




