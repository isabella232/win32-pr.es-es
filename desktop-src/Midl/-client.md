---
title: Modificador /client
description: El modificador /client dirige al compilador MIDL para generar archivos de código fuente de C del lado cliente para una interfaz RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client switch MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159770"
---
# <a name="client-switch"></a>Modificador /client

El **modificador /client** dirige al compilador MIDL para generar archivos de código fuente de C del lado cliente para una interfaz RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub**


</dt> <dd>

Genera los archivos del lado cliente.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none**


</dt> <dd>

No genera ningún archivo del lado cliente.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando no se especifica el modificador **/client,** el compilador midl genera el archivo de código auxiliar de cliente. Este modificador no afecta a las interfaces OLE.

El **modificador /client** tiene prioridad sobre [**el modificador /cstub.**](-cstub.md)

## <a name="examples"></a>Ejemplos

**midl /client none filename.idl**

**midl /client stub filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/server**](-server.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




