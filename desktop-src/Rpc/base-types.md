---
title: Tipos base
description: Para evitar los problemas que los tipos de datos dependientes de la implementación pueden causar en distintas arquitecturas de equipo, MIDL define sus propios tipos de datos base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476615"
---
# <a name="base-types"></a>Tipos base

Para evitar los problemas que los tipos de datos dependientes de la implementación pueden causar en distintas arquitecturas de equipo, MIDL define sus propios tipos de datos base.



| Tipo base                         | Descripción                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Booleana**](/windows/desktop/Midl/boolean)       | Elemento de datos que puede tener el valor **TRUE** o **FALSE.**                                                                                                          |
| [**Byte**](/windows/desktop/Midl/byte)             | Se garantiza que un elemento de datos de 8 bits se transmite sin ningún cambio.                                                                                                 |
| [**Char**](/windows/desktop/Midl/char-idl)         | Elemento de datos de caracteres sin signo de 8 bits.                                                                                                                              |
| [**Doble**](/windows/desktop/Midl/double)         | Número de punto flotante de 64 bits.                                                                                                                                     |
| [**Flotador**](/windows/desktop/Midl/float)           | Número de punto flotante de 32 bits.                                                                                                                                     |
| [**handle \_ t**](/windows/desktop/Midl/handle-t)    | Identificador primitivo que se puede usar para el enlace RPC o la serialización de datos.                                                                                            |
| [**hyper**](/windows/desktop/Midl/hyper)           | Un entero de 64 bits que se [](/windows/desktop/Midl/unsigned) puede declarar como [**con**](/windows/desktop/Midl/signed) signo o sin signo también se puede **\_ denominar int64**.                  |
| [**int**](/windows/desktop/Midl/int)               | Entero de 32 bits que se puede declarar como **con signo** o **sin signo.**                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Palabra clave que especifica un tipo entero que tiene propiedades de 32 o 64 bits.                                                                              |
| [**Largo**](/windows/desktop/Midl/long)             | Modificador de **int** que indica un entero de 32 bits. Se puede declarar como **con signo** o **sin signo.**                                                       |
| [**Corto**](/windows/desktop/Midl/short)           | Entero de 16 bits que se puede declarar como **con** signo o **sin signo.**                                                                                         |
| [**Pequeño**](/windows/desktop/Midl/small)           | Modificador de **int** que indica un entero de 8 bits. Se puede declarar como **con signo** o **sin signo.**                                                       |
| [**wchar \_ t**](/windows/desktop/Midl/wchar-t)      | Tipo de caracteres anchos que se admite como una extensión de Microsoft para IDL. Por lo tanto, este tipo no está disponible si se compila mediante el [ / **modificador osf.**](/windows/desktop/Midl/-osf) |



 

El archivo de encabezado Rpc rpc proporciona definiciones para la mayoría de estos tipos de datos base. La palabra **clave int** se reconoce y se puede transmitir en plataformas de 32 bits. En las plataformas de 16 bits, el tipo de datos **int** requiere un modificador , como **short** **o long**, para especificar su longitud.

Aunque **\* \* el estándar** ANSI C reconoce void como un tipo de puntero genérico, MIDL restringe su uso. Cada puntero utilizado en una operación remota o de serialización debe apuntar a tipos base o tipos construidos a partir de tipos base. (Hay una excepción: los identificadores de contexto se definen como **tipos void.** Para obtener más información, vea [Identificadores de contexto).](context-handles.md)

 

 