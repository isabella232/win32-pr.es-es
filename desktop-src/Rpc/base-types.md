---
title: Tipos base
description: Para evitar los problemas que pueden causar los tipos de datos dependientes de la implementación en distintas arquitecturas de equipo, MIDL define sus propios tipos de datos base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359343"
---
# <a name="base-types"></a>Tipos base

Para evitar los problemas que pueden causar los tipos de datos dependientes de la implementación en distintas arquitecturas de equipo, MIDL define sus propios tipos de datos base.



| Tipo base                         | Descripción                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**boolean**](/windows/desktop/Midl/boolean)       | Elemento de datos que puede tener el valor **true** o **false**.                                                                                                          |
| [**bytes**](/windows/desktop/Midl/byte)             | Un elemento de datos de 8 bits garantizado que se va a transmitir sin ningún cambio.                                                                                                 |
| [**char**](/windows/desktop/Midl/char-idl)         | Un elemento de datos de caracteres sin signo de 8 bits.                                                                                                                              |
| [**double**](/windows/desktop/Midl/double)         | Número de punto flotante de 64 bits.                                                                                                                                     |
| [**flot**](/windows/desktop/Midl/float)           | Número de punto flotante de 32 bits.                                                                                                                                     |
| [**identificador \_ t**](/windows/desktop/Midl/handle-t)    | Identificador primitivo que se puede utilizar para el enlace RPC o la serialización de datos.                                                                                            |
| [**Thread**](/windows/desktop/Midl/hyper)           | También se puede hacer referencia a un entero de 64 bits que se puede declarar como [**con signo**](/windows/desktop/Midl/signed) o [**sin signo**](/windows/desktop/Midl/unsigned) como **\_ Int64**.                  |
| [**Inter**](/windows/desktop/Midl/int)               | Entero de 32 bits que se puede declarar como **con signo** o **sin signo**.                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Palabra clave que especifica un tipo entero que tiene propiedades de 32 bits o de 64 bits.                                                                              |
| [**tal**](/windows/desktop/Midl/long)             | Un modificador para **int** que indica un entero de 32 bits. Se puede declarar como **con signo** o **sin signo**.                                                       |
| [**short**](/windows/desktop/Midl/short)           | Entero de 16 bits que se puede declarar como **con signo** o **sin signo**.                                                                                         |
| [**pequeño**](/windows/desktop/Midl/small)           | Un modificador para **int** que indica un entero de 8 bits. Se puede declarar como **con signo** o **sin signo**.                                                       |
| [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)      | Tipo de caracteres anchos que se admite como extensión de Microsoft para IDL. Por lo tanto, este tipo no está disponible si se compila con el modificador [ / **OSF**](/windows/desktop/Midl/-osf) . |



 

El archivo de encabezado Rpcndr. h proporciona definiciones para la mayoría de estos tipos de datos base. La palabra clave **int** se reconoce y se transmite en plataformas de 32 bits. En las plataformas de 16 bits, el tipo de datos **int** requiere un modificador, como **Short** o **Long**, para especificar su longitud.

Aunque **void \* \*** se reconoce como un tipo de puntero genérico por el estándar ANSI C, MIDL restringe su uso. Cada puntero utilizado en una operación remota o de serialización debe apuntar a tipos base o tipos construidos a partir de tipos base. (Hay una excepción: los identificadores de contexto se definen como tipos **void** . Para obtener más información, vea [identificadores de contexto](context-handles.md)).

 

 