---
title: Asas
description: Hasta dos partes de la descripción de la cadena de formato de una dirección de procedimiento que controla.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359284"
---
# <a name="handles"></a>Asas

Hasta dos partes de la descripción de la cadena de formato de una dirección de procedimiento que controla. La primera parte es el \_ tipo de identificador<1> campo de la descripción de un procedimiento, que se usa para indicar identificadores implícitos. Esta parte siempre está presente. La segunda parte es una descripción de parámetro de cualquier identificador explícito en el procedimiento. Ambos se explican en las secciones siguientes, junto con una explicación de la compatibilidad del compilador de MIDL adicional de la estructura de descriptores de código auxiliar para los problemas de identificador de enlace.

## <a name="implicit-handles"></a>Identificadores implícitos

Si un procedimiento usa un identificador implícito para el enlace, el \_ tipo de identificador<1> campo de la descripción del procedimiento contiene uno de los tres valores distintos de cero válidos. La compatibilidad del compilador de MIDL con los identificadores implícitos se encuentra en el \_ \_ campo información de identificador implícita de la estructura del descriptor de código auxiliar:

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

Si el procedimiento usa un identificador automático, el miembro **pAutoHandle** contiene la dirección de la variable de identificador automático definido por stub.

Si el procedimiento usa un identificador primitivo implícito, el miembro **pPrimitiveHandle** contiene la dirección de la variable de identificador primitivo definida por el código auxiliar.

Por último, si el procedimiento usa un identificador genérico implícito, el miembro **pGenericBindingInfo** contiene la dirección del puntero a la estructura **de \_ \_ información de enlace genérica** correspondiente. La descripción del **\_ código auxiliar \_ de MIDL** de la estructura de datos contiene un puntero a una colección de estructuras de **\_ \_ pares de enlace genéricos** . La entrada en la posición cero de esta colección está reservada para las rutinas de **enlace** y **desenlace** correspondientes al identificador de enlace genérico al que hace referencia **pGenericBindingInfo** en la **\_ \_ información de identificador implícita**. El tipo de identificador de enlace implícito se indica en la cadena de formato.

## <a name="explicit-handles"></a>Identificadores explícitos

Hay tres posibles tipos de identificador explícito: context, Generic y Primitive. En el caso de un identificador explícito (o un \[  \] identificador de contexto de solo salida, que se administra de la misma manera), la información del controlador de enlace aparece como uno de los parámetros del procedimiento. Las tres descripciones posibles son las siguientes.

Primitivo

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

La marca<1> indica si un puntero pasa el identificador.

El desplazamiento<2> proporciona el desplazamiento desde el principio de la pila hasta el identificador primitivo.

> [!Note]  
> Una descripción de identificador primitivo en la cadena de formato de tipo se reduce a un único \_ pase por alto de FC.

 

Genérico

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

La marca \_ y el \_ tamaño<1> tiene la marca superior y el tamaño de la parte inferior. La marca indica si el identificador se pasa mediante un puntero. El campo tamaño proporciona el tamaño del tipo de identificador genérico definido por el usuario. Este tamaño está limitado a 1, 2 o 4 bytes en sistemas de 32 bits y 1, 2, 4 u 8 bytes en sistemas de 64 bits.

El campo desplazamiento<2> proporciona el desplazamiento desde el principio de la pila del puntero a los datos del tamaño especificado.

El \_ \_ \_ campo de índice de rutina de enlace<1> proporciona el índice en el campo AGenericBindingRoutinePairs del descriptor de código auxiliar para los punteros de función de rutina de **enlace** y **desenlace** para el identificador genérico.

> [!Note]  
> Una descripción de identificador genérico en el formato de tipo es la descripción del tipo de datos relacionado.

 

Context

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Las marcas<1> indican cómo se pasa el identificador y qué tipo es. En la tabla siguiente se muestran marcas válidas.



| Hex | Marca                                   |
|-----|----------------------------------------|
| 80  | el \_ parámetro de identificador \_ es \_ mediante \_ ptr            |
| 40  | el \_ parámetro \_ de identificador está \_ en                  |
| 20  | el \_ parámetro de identificador \_ está \_ fuera                 |
| 21  | el \_ parámetro de identificador \_ es \_ devuelto              |
| 08  | identificador de contexto de NDR \_ STRICT \_ \_           |
| 04  | \_identificador de contexto NDR \_ \_ sin \_ serialización    |
| 02  | \_ \_ serializar identificador de contexto de NDR \_        |
| 01  | el \_ identificador de contexto de NDR \_ \_ no puede \_ ser \_ nulo |



 

Las primeras cuatro marcas siempre están presentes, las cuatro últimas se agregaron en Windows 2000.

El campo desplazamiento<2> proporciona el desplazamiento desde el inicio de la pila hasta el identificador de contexto.

El \_ Índice de \_ rutina de informe detallado de contexto \_<1> proporciona un índice en el campo **apfnNdrRundownRoutines** del descriptor de código auxiliar de la rutina de detención utilizada para este identificador de contexto. El compilador siempre genera un índice. En el caso de las rutinas que no tienen una rutina de informe detallado, se trata de un índice de una posición de tabla que contiene null.

En el caso de los códigos auxiliares integrados **: Oi2**, el parámetro \_ num<1> proporciona el recuento ordinal, empezando por cero y especificando el identificador de contexto que se encuentra en el procedimiento especificado.

En el caso de las versiones anteriores del intérprete, param \_ num<1> proporciona el número de parámetro del identificador de contexto, empezando por cero, en el procedimiento.

> [!Note]  
> Una descripción de identificador de contexto en la cadena de formato de tipo no tendrá el desplazamiento<2> en la descripción.

 

## <a name="the-new-oif-header"></a>Nuevo encabezado – interfaces

Como se mencionó anteriormente, el encabezado [**–**](/windows/desktop/Midl/-oi) activations se expande en el encabezado **– OI** . Para mayor comodidad, aquí se muestran todos los campos:

(El encabezado anterior)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(Extensiones de [**-interfaces**](/windows/desktop/Midl/-oi) )

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

El \_ \_ \_ tamaño de búfer de cliente constante<2> proporciona el tamaño del búfer de serialización que podría haber sido calculado previamente por el compilador. Esto puede ser solo un tamaño parcial, ya que la marca ClientMustSize desencadena el tamaño.

El \_ \_ \_ tamaño de búfer de servidor constante<2> proporciona el tamaño del búfer de serialización calculado por el compilador. Esto puede ser solo un tamaño parcial, ya que la marca ServerMustSize desencadena el tamaño.

Las \_ marcas opt del intérprete \_ se definen en Ndrtypes. h:

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

-   El bit ServerMustSize se establece si el servidor necesita realizar un paso de tamaño del búfer.
-   El bit ClientMustSize se establece si el cliente necesita realizar un paso de tamaño del búfer.
-   El bit HasReturn se establece si el procedimiento tiene un valor devuelto.
-   El bit HasPipes se establece si el paquete de canalización debe usarse para admitir un argumento de canalización.
-   El bit HasAsyncUuid se establece si el procedimiento es un procedimiento DCOM asincrónico.
-   El bit HasExtensions indica que se usan las extensiones de Windows 2000 y versiones posteriores.
-   El bit HasAsyncHandle indica un procedimiento RPC asincrónico.

El bit HasAsyncHandle se ha usado inicialmente para una implementación DCOM diferente de compatibilidad asincrónica y, por tanto, no se pudo usar para la compatibilidad asincrónica de estilo actual en DCOM. El bit HasAsyncUuid indica actualmente esto.

 

 