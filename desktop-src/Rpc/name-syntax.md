---
title: Sintaxis de nombre
description: Llamada a procedimiento remoto (RPC) y sintaxis de nombre.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f63c86e6fe9283855e886014787fe36361bfbcdea3bc53e4078bbb43d193293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927824"
---
# <a name="name-syntax"></a>Sintaxis de nombre

Rpc de Microsoft acepta nombres que se ajustan a la sintaxis siguiente:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Especifica un identificador que puede contener cualquier carácter excepto el carácter de barra diagonal delimitadora (/).

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>Nombrededominio
</dt> <dd>

Especifica el nombre del dominio.

</dd> </dl>

Un parámetro que selecciona el tipo de sintaxis de nombre y la cadena que especifica el nombre se proporcionan a muchas de las funciones RPC de la interfaz de servicio de nombres (NSI).

Rpc de Microsoft solo admite un tipo de sintaxis de nombre, tal y como especifica la constante RPC \_ C \_ NS \_ SYNTAX \_ DCE. Esta constante se define en el archivo de encabezado RPCNSI.H.

La sintaxis de nombre especificada por RPC C NS SYNTAX DCE es una extensión de la sintaxis de nombre Servicio de directorio de celdas \_ \_ \_ \_ \_ DCE (CDS) de OSF. La capacidad de especificar un nombre de dominio representa una extensión a esa sintaxis. No hay ningún límite absoluto en el número de nombres que se pueden separar por caracteres de barra diagonal, siempre que la cadena general tenga menos de 256 caracteres.

Las barras diagonales permiten especificar una estructura lógica en el nombre, pero no corresponden a una estructura lógica en los propios objetos.

 

 




