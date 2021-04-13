---
title: /Client (modificador)
description: El modificador/Client indica al compilador de MIDL que genere archivos de origen de C del lado cliente para una interfaz RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- parámetro/Client del modificador MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358247"
---
# <a name="client-switch"></a>/Client (modificador)

El modificador **/Client** indica al compilador de MIDL que genere archivos de origen de C del lado cliente para una interfaz RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>código auxiliar * * * *


</dt> <dd>

Genera los archivos del lado cliente.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>ninguno * * * *


</dt> <dd>

No genera ningún archivo del lado cliente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando no se especifica el modificador **/Client** , el compilador MIDL genera el archivo de código auxiliar del cliente. Este modificador no afecta a las interfaces OLE.

El modificador **/Client** tiene prioridad sobre el modificador [**/cstub**](-cstub.md)

## <a name="examples"></a>Ejemplos

**MIDL/Client None nombreDeArchivo. idl**

**archivo de código auxiliar de MIDL. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Server**](-server.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




