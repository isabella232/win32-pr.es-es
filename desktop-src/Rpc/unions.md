---
title: palabra clave Union (RPC)
description: Las uniones requieren palabras clave MIDL especiales para admitir su uso con la llamada a procedimiento remoto (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359009"
---
# <a name="union-keyword-rpc"></a>palabra clave Union (RPC)

Algunas características del lenguaje C, como uniones, requieren palabras clave MIDL especiales para admitir su uso en llamadas a procedimientos remotos. Una Unión en el lenguaje C es una variable que contiene objetos de diferentes tipos y tamaños. Normalmente, el desarrollador crea una variable para realizar un seguimiento de los tipos almacenados en la Unión. Para que funcione correctamente en un entorno distribuido, la variable que indica el tipo de Unión, o *discriminante*, también debe estar disponible en el equipo remoto. MIDL proporciona el \[ [**\_ tipo de modificador**](/windows/desktop/Midl/switch-type) \] y el \[ [**modificador \_ son**](/windows/desktop/Midl/switch-is) \] palabras clave para identificar el tipo y el nombre de discriminante.

MIDL requiere que el discriminante se transmita con la Unión de una de estas dos maneras:

-   La Unión y discriminante se deben proporcionar como parámetros.
-   La Unión y discriminante se deben empaquetar en una estructura.

MIDL proporciona dos tipos fundamentales de uniones discriminadas: [**\_ Unión no encapsulada**](/windows/desktop/Midl/nonencapsulated-unions) y [**\_ Unión encapsulada**](/windows/desktop/Midl/encapsulated-unions). El discriminante de una Unión no encapsulada es otro parámetro si la Unión es un parámetro. Es otro campo si la Unión es un campo de una estructura. La definición de una Unión encapsulada se convierte en una definición de estructura cuyo primer campo es el discriminante y cuyo segundo y último campos son la Unión. En el ejemplo siguiente se muestra cómo proporcionar la Unión y discriminante como parámetros:

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

En el ejemplo anterior, la Unión puede contener un valor único: **Short**, **float** o **Char**. La definición de tipo para la Unión incluye el atributo de **\_ tipo de modificador** MIDL que especifica el tipo de discriminante. Aquí, \[ \_ el tipo de conmutador (short) \] especifica que discriminante es de tipo **Short**. El modificador debe ser un tipo entero.

Si la Unión es un miembro de una estructura, el discriminante debe ser un miembro de la misma estructura. Si la Unión es un parámetro, el discriminante debe ser otro parámetro. El prototipo de la función **UnionParamProc** en el ejemplo anterior muestra discriminante *sUtype* como el último parámetro de la llamada. (Discriminante puede aparecer en cualquier posición de la llamada). El tipo del parámetro especificado en el **\[ modificador \_ es \]** el atributo debe coincidir con el tipo especificado en el atributo de **\[ \_ \] tipo de conmutador** .

En el ejemplo siguiente se muestra el uso de una única estructura que empaqueta discriminante con la Unión:

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

El compilador de Microsoft RPC MIDL permite declaraciones Union fuera de las construcciones [**typedef**](/windows/desktop/Midl/typedef) . Esta característica es una extensión de DCE IDL. Para obtener más información, consulte [**Union**](/windows/desktop/Midl/union).

 

 