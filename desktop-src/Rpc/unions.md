---
title: palabra clave union (RPC)
description: Las uniones requieren palabras clave MIDL especiales para admitir su uso con llamada a procedimiento remoto (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071387"
---
# <a name="union-keyword-rpc"></a>palabra clave union (RPC)

Algunas características del lenguaje C, como las uniones, requieren palabras clave MIDL especiales para admitir su uso en llamadas a procedimientos remotos. Una unión en el lenguaje C es una variable que contiene objetos de diferentes tipos y tamaños. Normalmente, el desarrollador crea una variable para realizar un seguimiento de los tipos almacenados en la unión. Para funcionar correctamente en un entorno distribuido, la variable que indica el tipo de unión o discriminador *también* debe estar disponible para el equipo remoto. MIDL proporciona el \[ [**tipo de modificador \_ y**](/windows/desktop/Midl/switch-type) \] switch \[ [**\_ es**](/windows/desktop/Midl/switch-is) \] palabras clave para identificar el tipo y el nombre discriminante.

MIDL requiere que el discriminador se transmita con la unión de una de estas dos maneras:

-   La unión y el discriminador deben proporcionarse como parámetros.
-   La unión y el discriminador deben empaquetarse en una estructura .

MIDL proporciona dos tipos fundamentales de uniones discriminadas: [**unión nocapsulada \_**](/windows/desktop/Midl/nonencapsulated-unions) y [**unión \_ encapsulada**](/windows/desktop/Midl/encapsulated-unions). El discriminador de una unión nocapsulada es otro parámetro si la unión es un parámetro. Es otro campo si la unión es un campo de una estructura. La definición de una unión encapsulada se convierte en una definición de estructura cuyo primer campo es el discriminador y cuyo segundo y último campo son la unión. En el ejemplo siguiente se muestra cómo proporcionar la unión y discriminador como parámetros:

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

La unión del ejemplo anterior puede contener un valor único: **short**, **float** o **char**. La definición de tipo para la unión incluye el atributo de tipo **de modificador \_** MIDL que especifica el tipo del discriminante. Aquí, \[ switch \_ type(short) \] especifica que el discriminador es de tipo **short**. El modificador debe ser un tipo entero.

Si la unión es miembro de una estructura, el discriminador debe ser miembro de la misma estructura. Si la unión es un parámetro, el discriminador debe ser otro parámetro. El prototipo de la **función UnionParamProc** en el ejemplo anterior muestra el *discriminante sUtype* como el último parámetro de la llamada. (El discriminador puede aparecer en cualquier posición de la llamada). El tipo del parámetro especificado en el **\[ atributo switch \_ is \]** debe coincidir con el tipo especificado en el atributo **\[ switch \_ type. \]**

En el ejemplo siguiente se muestra el uso de una sola estructura que empaqueta el discriminador con la unión :

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

El compilador MIDL rpc de Microsoft permite declaraciones de unión fuera de [**las construcciones typedef.**](/windows/desktop/Midl/typedef) Esta característica es una extensión de DCE IDL. Para obtener más información, vea [**union**](/windows/desktop/Midl/union).

 

 