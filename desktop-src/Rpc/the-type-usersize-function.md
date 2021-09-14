---
title: La type_UserSize función
description: La función \_ UserSize de tipo es una función auxiliar para los atributos \wire \_ marshal\ y \_ \user marshal\.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f997d12e11f643eb2faf9990454a8508d15636
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244424"
---
# <a name="the-type_usersize-function"></a>El tipo \_ UserSize (Función)

La **&lt; función &gt; \_ UserSize de** tipo es una función auxiliar para los atributos wire marshal \[ [ \_ y](/windows/desktop/Midl/wire-marshal) \] user \[ [ \_ marshal.](/windows/desktop/Midl/user-marshal) \] Los códigos auxiliares llaman a esta función para cambiar el tamaño del búfer de datos RPC para el objeto de datos de usuario antes de serializar los datos en el lado cliente o servidor. La función se define como:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

El &lt; tipo en el nombre de la función significa &gt; userm-type, **\[ \_ \]** **\[ \_ \]** tal como se especifica en la definición de tipo de serialización de usuario o de referencias de conexión. Este tipo puede no ser transmitible o incluso, cuando se usa con el atributo **\[ \_ de \]** serialización de usuario, desconocido para el compilador MIDL. El nombre del tipo de conexión (el nombre del tipo transmitido a través de la red) no se usa en el prototipo de función. Sin embargo, tenga en cuenta que el tipo de conexión define el diseño de los datos según lo especificado por OSF DCE. Todos los datos deben convertirse al formato de representación de datos de red (CONVERT).

El *parámetro pFlags* es un puntero a **un campo de marca larga** sin signo. La palabra superior de la marca contiene marcas de formato OMISIÓN definidas por OSF DCE para representaciones de punto flotante, orden de bytes y caracteres. La palabra inferior contiene una marca de contexto de serialización definida por el canal COM. El diseño exacto de las marcas dentro del campo se muestra en la tabla siguiente.



| Bits  | Marca                                  | Value                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Representación de punto flotante         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Orden de bytes enteros y de punto flotante | 0 = Big-endian 1 = Little-endian                                                          |
| 19-16 | Representación de caracteres              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Marca de contexto de serialización               | 0 = MSHCTX \_ LOCAL 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ INPROC |



 

La marca de contexto de serialización permite modificar el comportamiento de la rutina en función del contexto de la llamada RPC. Por ejemplo, si tiene un identificador **(long**) a un bloque de datos, podría enviar el identificador de una llamada en proceso, pero enviaría los datos reales de una llamada a otro equipo. La marca de contexto de serialización y sus valores se definen en los archivos Wtypes.h y Wtypes.idl del Kit de desarrollo de software de plataforma (SDK).

> [!Note]  
> Cuando el tipo de conexión está definido correctamente, no es necesario usar las marcas de formato JPEG, ya que el motor JPEG realiza las conversiones necesarias.

 

El *parámetro StartingSize* a es el desplazamiento del búfer actual. El tamaño inicial indica el desplazamiento del búfer para el objeto de usuario y puede o no estar alineado correctamente. La rutina debe tener en cuenta el relleno necesario.

El *parámetro pMyObj* es un puntero a un objeto de tipo de usuario.

El valor devuelto es la nueva posición de desplazamiento o búfer. La función debe devolver el tamaño acumulado, que es el tamaño inicial más el posible relleno más el tamaño de los datos.

La **&lt; función &gt; \_ UserSize de** tipo puede devolver una sobreestimación del tamaño necesario. El tamaño real del búfer enviado está definido por el tamaño de los datos, no por el tamaño de asignación del búfer.

No **&lt; se llama a la &gt; \_ función UserSize** de tipo si el tamaño de la conexión se puede calcular en tiempo de compilación. Tenga en cuenta que para la mayoría de las uniones, incluso si no hay punteros, el tamaño real de la representación de la conexión solo se puede determinar en tiempo de ejecución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reglas de serialización para la serialización \_ de usuarios y la serialización de \_ conexión](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[serialización \_ de usuario](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 
