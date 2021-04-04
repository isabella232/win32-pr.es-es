---
title: modificador/Server
description: El modificador/Server indica al compilador de MIDL que genere archivos de origen de C del lado servidor para una interfaz RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- modificador de/Server (MIDL)
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076766"
---
# <a name="server-switch"></a>modificador/Server

El modificador **/Server** indica al compilador de MIDL que genere archivos de origen de C del lado servidor para una interfaz RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>código auxiliar * * * *


</dt> <dd>

Genera los archivos del lado servidor.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>ninguno * * * *


</dt> <dd>

No genera archivos del lado servidor.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando no se especifica el modificador **/Server** , el compilador MIDL genera el archivo de código auxiliar del servidor. Este modificador no afecta a las interfaces OLE.

La opción **None** no hace que se generen archivos.

El modificador **/Server** tiene prioridad sobre el modificador **/sstub**

## <a name="examples"></a>Ejemplos

**MIDL/Server None**

**código auxiliar de MIDL/Server**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




