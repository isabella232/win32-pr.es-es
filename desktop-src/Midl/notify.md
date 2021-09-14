---
title: atributo notify
description: El atributo \notify\ indica al compilador midL que genere una llamada a un procedimiento \notify\ en el lado servidor de la aplicación.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notify attribute MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159440"
---
# <a name="notify-attribute"></a>atributo notify

El **\[ atributo notify \]** indica al compilador MIDL que genere una llamada a un procedimiento **\[ de \]** notificación en el lado servidor de la aplicación.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*procedure-name* 
</dt> <dd>

Nombre del procedimiento remoto al que se asociará el procedimiento de notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ procedimiento de \]** notificación llamado como resultado del atributo **\[ notify \]** está asociado a un procedimiento remoto determinado en el servidor. Es similar en concepto a una función de devolución de llamada. El código **\[ \]** auxiliar llama al procedimiento de notificación después de que se hayan serializado todos los argumentos de salida del procedimiento remoto al que está asociado y se libera cualquier memoria asociada a los parámetros. Se **\[ llama a la \]** rutina notify si se produce un error en una llamada antes de que se ejecute la rutina de servidor. Por ejemplo, si se produce un error en un servidor durante la desmarque debido a la recepción de datos no recibidos del cliente, se llama a \[ \] la rutina de notificación.

El **\[ atributo notify \]** es útil para desarrollar aplicaciones que adquieren recursos en procedimientos remotos. A continuación, estos recursos se liberan en el procedimiento **\[ de \]** notificación una vez que se serializan por completo los parámetros de salida del procedimiento remoto.

El **\[ nombre \]** del procedimiento de notificación es el nombre del procedimiento remoto con el sufijo **\_ notify**. El **\_ procedimiento de** notificación no requiere ningún parámetro y no devuelve un resultado. También se genera un prototipo de este procedimiento en el archivo de encabezado. Por ejemplo, si el archivo IDL contiene lo siguiente:

``` syntax
MyProcedure([in] short S);
```

Especifique lo siguiente en ACF for MIDL para generar la **\_ llamada de** notificación:

``` syntax
[notify] MyProcedure();
```

El compilador MIDL generará código auxiliar de servidor que contiene la siguiente llamada al **\_ procedimiento de** notificación:

``` syntax
MyProcedure_notify();
```

El archivo de encabezado contendrá un prototipo:

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>Ejemplos

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> </dl>

 

 




