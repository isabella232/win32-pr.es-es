---
title: notificar atributo
description: El atributo \ Notify \ indica al compilador de MIDL que genere una llamada a un procedimiento \ Notify \ en el lado servidor de la aplicación.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notificar al atributo MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532596"
---
# <a name="notify-attribute"></a>notificar atributo

El atributo **\[ Notify \]** indica al compilador de MIDL que genere una llamada a un procedimiento **\[ Notify \]** en el lado del servidor de la aplicación.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*procedimiento: nombre* 
</dt> <dd>

Nombre del procedimiento remoto con el que se asociará el procedimiento de notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El procedimiento **\[ Notify \]** llamado como resultado del atributo **\[ Notify \]** está asociado a un procedimiento remoto determinado en el servidor. Es similar en concepto a una función de devolución de llamada. El código auxiliar llama al procedimiento **\[ Notify \]** una vez que se han calculado las referencias de todos los argumentos de salida del procedimiento remoto al que está asociado, y se libera cualquier memoria asociada a los parámetros. Se llama a la rutina **\[ Notify \]** si se produce un error en una llamada antes de que se ejecute la rutina de servidor. Por ejemplo, si se produce un error en un servidor durante la desserialización debido a la recepción de datos incorrectos del cliente, \[ \] se llama a la rutina Notify.

El atributo **\[ Notify \]** es útil para desarrollar aplicaciones que adquieran recursos en procedimientos remotos. Estos recursos se liberan después en el procedimiento **\[ Notify \]** después de que se calculen las referencias de los parámetros de salida del procedimiento remoto.

El nombre del procedimiento de **\[ notificación \]** es el nombre del procedimiento remoto con el sufijo de **\_ notificaciones**. El procedimiento **\_ Notify** no requiere ningún parámetro y no devuelve un resultado. También se genera un prototipo de este procedimiento en el archivo de encabezado. Por ejemplo, si el archivo IDL contiene lo siguiente:

``` syntax
MyProcedure([in] short S);
```

Especifique lo siguiente en ACF para MIDL a fin de generar la llamada a **\_ Notify** :

``` syntax
[notify] MyProcedure();
```

El compilador MIDL generará código auxiliar de servidor que contiene la siguiente llamada al procedimiento **\_ Notify** :

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

 

 




