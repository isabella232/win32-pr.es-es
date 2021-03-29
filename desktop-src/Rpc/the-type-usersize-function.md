---
title: La función type_UserSize
description: La función de tipo de usuario \_ es una función auxiliar para los atributos \ WIRE \_ Marshal \ y \ User \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793665"
---
# <a name="the-type_usersize-function"></a>La función de tipo de \_ usuario

La **<type> \_ función de usuario es** una función auxiliar para los atributos de serialización de \[ [ \_ conexión](/windows/desktop/Midl/wire-marshal) \] y de cálculo de \[ [ \_ referencias de usuarios](/windows/desktop/Midl/user-marshal) \] . El código auxiliar llama a esta función para ajustar el tamaño del búfer de datos RPC para el objeto de datos del usuario antes de que se calculen las referencias de los datos en el cliente o el servidor. La función se define como:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<type>En el nombre de la función se entiende el tipo userm, tal y como se especifica en la definición de tipo de cálculo de referencias de **\[ \_ \] conexión** o de **\[ usuario \_ \]** . Este tipo puede ser no transmitible o incluso cuando se usa con el atributo de **\[ \_ cálculo de referencias \] del usuario** , desconocido para el compilador de MIDL. El nombre del tipo de conexión (el nombre del tipo transmitido a través de la red) no se utiliza en el prototipo de función. Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de los datos tal y como se especifica en OSF DCE. Todos los datos se deben convertir al formato de representación de datos de red (NDR).

El parámetro *pFlags* es un puntero a un campo de marca **larga sin signo** . La palabra superior de la marca contiene marcas de formato NDR, tal y como se define en OSF DCE para el punto flotante, el orden de bytes y las representaciones de caracteres. La palabra inferior contiene una marca de contexto de cálculo de referencias tal como la define el canal COM. En la tabla siguiente se muestra el diseño exacto de las marcas dentro del campo.



| Bits  | Marca                                  | Value                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Representación de punto flotante         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Orden de bytes entero y de punto flotante | 0 = Big-Endian 1 = Little-endian                                                          |
| 19-16 | Representación de caracteres              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Marca de contexto de cálculo de referencias               | 0 = MSHCTX \_ local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ Inproc |



 

La marca de contexto de serialización permite modificar el comportamiento de la rutina en función del contexto de la llamada RPC. Por ejemplo, si tiene un identificador (**Long**) a un bloque de datos, podría enviar el identificador de una llamada en proceso, pero enviaría los datos reales para una llamada a otro equipo. La marca de contexto de cálculo de referencias y sus valores se definen en los archivos Wtypes. h y Wtypes. idl en el kit de desarrollo de software (SDK) de la plataforma.

> [!Note]  
> Cuando el tipo de conexión se define correctamente, no es necesario utilizar las marcas de formato NDR, ya que el motor NDR realiza las conversiones necesarias.

 

El parámetro *StartingSize* es el desplazamiento del búfer actual. El tamaño inicial indica el desplazamiento del búfer para el objeto de usuario y puede o no estar alineado correctamente. La rutina debe tener en cuenta el relleno que sea necesario.

El parámetro *pMyObj* es un puntero a un objeto de tipo de usuario.

El valor devuelto es el nuevo desplazamiento o la posición del búfer. La función debe devolver el tamaño acumulado, que es el tamaño inicial más el posible relleno más el tamaño de los datos.

La función de **<type> \_ usuario** puede devolver un valor sobrestimado del tamaño necesario. El tamaño real del búfer enviado lo define el tamaño de los datos, no el tamaño de asignación del búfer.

No se llama a la función de **<type> \_ usuario** si el tamaño de la conexión se puede calcular en tiempo de compilación. Tenga en cuenta que para la mayoría de las uniones, incluso si no hay punteros, el tamaño real de la representación de la conexión solo se puede determinar en tiempo de ejecución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Serialización de reglas para serialización de usuario \_ y \_ serialización de conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[\_serialización de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[\_serialización de cable](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 