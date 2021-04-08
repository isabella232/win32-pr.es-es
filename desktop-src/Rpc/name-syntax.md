---
title: Sintaxis de nombre
description: Llamada a procedimiento remoto (RPC) y sintaxis de nombre.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994411"
---
# <a name="name-syntax"></a>Sintaxis de nombre

Microsoft RPC acepta nombres que se ajustan a la siguiente sintaxis:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Especifica un identificador que puede contener cualquier carácter excepto el carácter de barra diagonal (/) delimitador.

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>dominio de
</dt> <dd>

Especifica el nombre del dominio.

</dd> </dl>

Parámetro que selecciona el tipo de sintaxis de nombre y la cadena que especifica el nombre que se proporciona a muchas de las funciones RPC de la interfaz del servicio de nombres (NSI).

Microsoft RPC solo admite un tipo de sintaxis de nombre, tal y como se especifica en el \_ DCE de sintaxis de RPC C NS de constantes \_ \_ \_ . Esta constante se define en el archivo de encabezado RPCNSI. H.

La sintaxis de nombre especificada por \_ el \_ \_ DCE de sintaxis de RPC C NS \_ es una extensión de la \_ Sintaxis de nombre de servicio de directorio de celdas (CDs) de OSF DCE. La capacidad de especificar un nombre de dominio representa una extensión de esa sintaxis. No hay ningún límite absoluto en el número de nombres que se pueden separar con caracteres de barra diagonal, siempre y cuando la cadena global tenga menos de 256 caracteres.

Las barras diagonales le permiten especificar una estructura lógica para el nombre, pero no se corresponden con una estructura lógica en los propios objetos.

 

 




