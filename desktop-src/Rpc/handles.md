---
title: Asas
description: Hasta dos partes en la descripción de cadena de formato de los identificadores de una dirección de procedimiento.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244695"
---
# <a name="handles"></a>Asas

Hasta dos partes en la descripción de cadena de formato de los identificadores de una dirección de procedimiento. La primera parte es el tipo de identificador<1> campo de la descripción de un procedimiento, que se usa \_ para indicar identificadores implícitos. Esta parte siempre está presente. La segunda parte es una descripción de parámetro de cualquier identificador explícito en el procedimiento. Ambos se explican en las secciones siguientes, junto con una explicación de la compatibilidad adicional del compilador MIDL de la estructura del descriptor de código auxiliar para los problemas de identificador de enlace.

## <a name="implicit-handles"></a>Identificadores implícitos

Si un procedimiento usa un identificador implícito para el enlace, el tipo de identificador<un campo> de la descripción del procedimiento contiene uno de los tres valores válidos distintos \_ de cero. La compatibilidad del compilador MIDL con identificadores implícitos se encuentra en el campo IMPLICIT \_ HANDLE INFO de la estructura Del descriptor de código \_ auxiliar:

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

Si el procedimiento usa un identificador automático, el **miembro pAutoHandle** contiene la dirección de la variable de controlador auto definida por el código auxiliar.

Si el procedimiento usa un identificador primitivo implícito, el **miembro pPrimitiveHandle** contiene la dirección de la variable de identificador defined–primitive del código auxiliar.

Por último, si el procedimiento usa un identificador genérico implícito, el **miembro pGenericBindingInfo** contiene la dirección del puntero a la estructura **GENERIC BINDING \_ \_ INFO** correspondiente. La estructura de datos **MIDL \_ STUB \_ DESC** contiene un puntero a una colección de estructuras **GENERIC BINDING \_ \_ PAIR.** La entrada en la posición cero de  esta  colección está reservada para las rutinas de enlace y desenlace correspondientes al identificador de enlace genérico al que hace referencia **pGenericBindingInfo** en **IMPLICIT \_ HANDLE \_ INFO**. El tipo de identificador de enlace implícito se indica en la cadena de formato.

## <a name="explicit-handles"></a>Identificadores explícitos

Hay tres tipos de identificadores explícitos posibles: contexto, genérico y primitivo. En el caso de un identificador explícito (o un identificador de contexto de solo salida, que se controla de la misma manera), la información del identificador de enlace aparece como uno de los parámetros \[  \] del procedimiento. Las tres descripciones posibles son las siguientes.

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

La marca y el tamaño<1> tiene la marca superior \_ \_ nibble y el tamaño inferior nibble. La marca indica si un puntero pasa el identificador. El campo tamaño proporciona el tamaño del tipo de identificador genérico definido por el usuario. Este tamaño se limita a 1, 2 o 4 bytes en sistemas de 32 bits y 1, 2, 4 u 8 bytes en sistemas de 64 bits.

El desplazamiento<2 campos> proporciona el desplazamiento desde el principio de la pila del puntero hasta los datos del tamaño especificado.

El índice de par de rutinas de enlace<un campo> proporciona el índice en el campo \_ \_ \_ aGenericBindingRoutinePairs   del descriptor de código auxiliar para enlazar y desenlace los punteros de función rutinaria para el identificador genérico.

> [!Note]  
> Una descripción de identificador genérico en el formato de tipo es solo la descripción del tipo de datos relacionado.

 

Context

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
| 08  | IDENTIFICADOR DE \_ CONTEXTO \_ ESTRICTO DE \_ BAND           |
| 04  | IDENTIFICADOR DE CONTEXTO DE BAND \_ \_ SIN \_ \_ SERIALIZACIÓN    |
| 02  | SERIALIZACIÓN \_ DEL IDENTIFICADOR DE CONTEXTO DE \_ \_ SERIALIZACIÓN        |
| 01  | EL IDENTIFICADOR DE CONTEXTO DE BAND \_ \_ NO PUEDE SER \_ \_ \_ NULL |



 

Las cuatro primeras marcas siempre han estado presentes, las cuatro últimas se agregaron en Windows 2000.

El desplazamiento<2> campo proporciona el desplazamiento desde el inicio de la pila hasta el identificador de contexto.

El índice de rutina de desmontaje de contexto<1> proporciona un índice en el campo \_ \_ \_ **apfnRunRundownRoutines** del descriptor de código auxiliar para la rutina de desmontaje utilizada para este identificador de contexto. El compilador siempre genera un índice. Para las rutinas que no tienen una rutina de desmontaje, se trata de un índice de una posición de tabla que contiene null.

Para los códigos auxiliares integrados **en –Oi2,** el parámetro num<1> proporciona el recuento ordinal, empezando por cero, especificando qué identificador de contexto se encuentra en el procedimiento \_ especificado.

Para las versiones anteriores del intérprete, el parámetro num<1> proporciona el número de parámetro del identificador de contexto, empezando en \_ cero, en su procedimiento.

> [!Note]  
> Una descripción del identificador de contexto en la cadena de formato de tipo no tendrá el desplazamiento<2> en la descripción.

 

## <a name="the-new-oif-header"></a>Nuevo encabezado –Oif

Como se mencionó anteriormente, [**el encabezado –Oif**](/windows/desktop/Midl/-oi) se expande en el **encabezado –Oi.** Para mayor comodidad, todos los campos se muestran aquí:

(Encabezado antiguo)

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

El tamaño de búfer de servidor constante<2> proporciona el tamaño del búfer de serialización tal como lo \_ \_ \_ precaltó el compilador. Puede ser solo un tamaño parcial, ya que la marca ServerMustSize desencadena el tamaño.

Las MARCAS \_ DE OPT DE INTERPRETER se definen en \_ Types.h:

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
-   El bit ClientMustSize se establece si el cliente necesita realizar un paso de tamaño de búfer.
-   El bit HasReturn se establece si el procedimiento tiene un valor devuelto.
-   El bit HasPipes se establece si el paquete de canalización debe usarse para admitir un argumento de canalización.
-   El bit HasAsyncUuid se establece si el procedimiento es un procedimiento DCOM asincrónico.
-   El bit HasExtensions indica que Windows 2000 y las extensiones posteriores.
-   El bit HasAsyncHandle indica un procedimiento RPC asincrónico.

El bit HasAsyncHandle se ha usado inicialmente para una implementación DCOM diferente de compatibilidad asincrónica y, por lo tanto, no se pudo usar para la compatibilidad asincrónica de estilo actual en DCOM. El bit HasAsyncUuid actualmente indica esto.

 

 