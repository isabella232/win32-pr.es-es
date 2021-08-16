---
title: Asas
description: Hasta dos partes en la descripción de cadena de formato de los identificadores de dirección de un procedimiento.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb31dcf075b7b07b65d2a976a37386e164d8cadc11903a33c22172c433a3a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929542"
---
# <a name="handles"></a>Asas

Hasta dos partes en la descripción de cadena de formato de los identificadores de dirección de un procedimiento. La primera parte es el tipo de identificador<1> de la descripción de un procedimiento, que se \_ usa para indicar identificadores implícitos. Esta parte siempre está presente. La segunda parte es una descripción de parámetro de cualquier identificador explícito en el procedimiento. Ambos se explican en las secciones siguientes, junto con una explicación de la compatibilidad adicional del compilador MIDL de la estructura del descriptor de código auxiliar para los problemas de identificador de enlace.

## <a name="implicit-handles"></a>Identificadores implícitos

Si un procedimiento usa un identificador implícito para el enlace, el tipo de identificador<un campo> de la descripción del procedimiento contiene uno de los tres valores distintos de \_ cero válidos. La compatibilidad del compilador MIDL con identificadores implícitos se encuentra en el campo IMPLICIT \_ HANDLE INFO de la estructura Descriptor de código \_ auxiliar:

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

Si el procedimiento usa un identificador automático, el **miembro pAutoHandle** contiene la dirección de la variable de identificador automático definida por el código auxiliar.

Si el procedimiento usa un identificador primitivo implícito, el **miembro pPrimitiveHandle** contiene la dirección de la variable de identificador primitivo definida por el código auxiliar.

Por último, si el procedimiento usa un identificador genérico implícito, el **miembro pGenericBindingInfo** contiene la dirección del puntero a la estructura **GENERIC BINDING \_ \_ INFO** correspondiente. La estructura de datos **MIDL \_ STUB \_ DESC** contiene un puntero a una colección de estructuras **GENERIC BINDING \_ \_ PAIR.** La entrada en la posición cero de  esta  colección está reservada para las rutinas de enlace y desenlazadas correspondientes al identificador de enlace genérico al que hace referencia **pGenericBindingInfo** en **IMPLICIT \_ HANDLE \_ INFO**. El tipo de identificador de enlace implícito se indica en la cadena de formato.

## <a name="explicit-handles"></a>Identificadores explícitos

Hay tres posibles tipos de identificador explícitos: contexto, genérico y primitivo. En el caso de un identificador explícito (o un identificador de contexto de solo salida, que se controla de la misma manera), la información del identificador de enlace aparece como uno de los parámetros \[  \] del procedimiento. Las tres descripciones posibles son las siguientes.

Primitivo

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

La marca<1> indica si un puntero pasa el identificador.

El desplazamiento<2> proporciona el desplazamiento desde el principio de la pila hasta el identificador primitivo.

> [!Note]  
> Una descripción de identificador primitivo en la cadena de formato de tipo se reduce a una única FC \_ IGNORE.

 

Genérico

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

La marca y el tamaño<1> la marca superior nibble y el tamaño \_ \_ inferior. La marca indica si un puntero pasa el identificador. El campo tamaño proporciona el tamaño del tipo de identificador genérico definido por el usuario. Este tamaño se limita a 1, 2 o 4 bytes en sistemas de 32 bits y 1, 2, 4 u 8 bytes en sistemas de 64 bits.

El campo<2> proporciona el desplazamiento desde el principio de la pila del puntero hasta los datos del tamaño especificado.

El índice de par de rutinas de enlace<el campo 1> proporciona el índice en el \_ \_ campo \_ aGenericBindingRoutinePairs   del descriptor de código auxiliar para enlazar y desenlace punteros de función rutinaria para el identificador genérico.

> [!Note]  
> Una descripción de identificador genérico en el formato de tipo es solo la descripción del tipo de datos relacionado.

 

Contexto

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Las marcas<1> indican cómo se pasa el identificador y qué tipo es. Las marcas válidas se muestran en la tabla siguiente.



| Hex | Marca                                   |
|-----|----------------------------------------|
| 80  | HANDLE \_ PARAM \_ ES A TRAVÉS \_ DE \_ PTR            |
| 40  | HANDLE \_ PARAM \_ ESTÁ \_ EN                  |
| 20  | HANDLE \_ PARAM \_ IS \_ OUT                 |
| 21  | HANDLE \_ PARAM \_ IS \_ RETURN              |
| 08  | IDENTIFICADOR DE \_ CONTEXTO ESTRICTO \_ DE BAND \_           |
| 04  | IDENTIFICADOR DE CONTEXTO DE BAND \_ \_ SIN \_ \_ SERIALIZACIÓN    |
| 02  | SERIALIZACIÓN \_ DEL IDENTIFICADOR DE CONTEXTO DE \_ \_ SERIALIZACIÓN        |
| 01  | EL IDENTIFICADOR DE CONTEXTO DE TAMPOCO \_ \_ PUEDE SER \_ \_ \_ NULL |



 

Las cuatro primeras marcas siempre han estado presentes, las cuatro últimas se agregaron en Windows 2000.

El desplazamiento<2> campo proporciona el desplazamiento desde el inicio de la pila hasta el identificador de contexto.

El índice de rutina de desenlace de contexto<1> proporciona un índice en el \_ \_ campo \_ **apfnRunRundownRoutines** del descriptor de código auxiliar para la rutina de desmontaje utilizada para este identificador de contexto. El compilador siempre genera un índice. En el caso de las rutinas que no tienen una rutina de desmontaje, se trata de un índice de una posición de tabla que contiene null.

Para los códigos auxiliares integrados **en –Oi2**, el parámetro num<1> proporciona el recuento ordinal, empezando por cero, especificando qué identificador de contexto se encuentra en el procedimiento \_ especificado.

Para las versiones anteriores del intérprete, el parámetro param num<1> proporciona el número de parámetro del identificador de contexto, empezando por cero, en \_ su procedimiento.

> [!Note]  
> Una descripción del identificador de contexto en la cadena de formato de tipo no tendrá el desplazamiento<2> en la descripción.

 

## <a name="the-new-oif-header"></a>Nuevo encabezado –Oif

Como se mencionó anteriormente, [**el encabezado –Oif**](/windows/desktop/Midl/-oi) se expande en el **encabezado –Oi.** Para mayor comodidad, aquí se muestran todos los campos:

(El encabezado anterior)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(Las [**extensiones –Oif)**](/windows/desktop/Midl/-oi)

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

El tamaño de búfer de cliente constante<2> proporciona el tamaño del búfer de serialización que el compilador podría haber calculado \_ \_ \_ previamente. Puede ser solo un tamaño parcial, ya que la marca ClientMustSize desencadena el tamaño.

El tamaño de búfer de servidor constante<2> proporciona el tamaño del búfer de serialización según lo \_ \_ \_ precalutado por el compilador. Puede ser solo un tamaño parcial, ya que la marca ServerMustSize desencadena el tamaño.

Las MARCAS \_ DE OPT DEL INTÉRPRETE se definen en \_ Typetypes.h:

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   El bit ServerMustSize se establece si el servidor necesita realizar un paso de tamaño de búfer.
-   El bit ClientMustSize se establece si el cliente necesita realizar un paso de ajuste de tamaño de búfer.
-   El bit HasReturn se establece si el procedimiento tiene un valor devuelto.
-   El bit HasPipes se establece si el paquete de canalización debe usarse para admitir un argumento de canalización.
-   El bit HasAsyncUuid se establece si el procedimiento es un procedimiento DCOM asincrónico.
-   El bit HasExtensions indica que Windows 2000 y las extensiones posteriores.
-   El bit HasAsyncHandle indica un procedimiento RPC asincrónico.

El bit HasAsyncHandle se ha usado inicialmente para una implementación DCOM diferente de compatibilidad asincrónica y, por lo tanto, no se pudo usar para la compatibilidad asincrónica de estilo actual en DCOM. El bit HasAsyncUuid lo indica actualmente.

 

 