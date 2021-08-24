---
title: Modificador /server
description: El modificador /server dirige al compilador MIDL para generar archivos de código fuente de C del lado servidor para una interfaz RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf634e9ce91e937ff1e43b9059d12181dc723695139001ec368109d6fdf4a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067475"
---
# <a name="server-switch"></a>Modificador /server

El **modificador /server** dirige al compilador MIDL para generar archivos de código fuente C del lado servidor para una interfaz RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub***


</dt> <dd>

Genera los archivos del lado servidor.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none**


</dt> <dd>

No genera archivos del lado servidor.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando no se especifica el modificador **/server,** el compilador MIDL genera el archivo de código auxiliar del servidor. Este modificador no afecta a las interfaces OLE.

La **opción none** hace que no se genere ningún archivo.

El **modificador /server** tiene prioridad sobre **el modificador /sstub.**

## <a name="examples"></a>Ejemplos

**midl /server none**

**midl /server stub**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




