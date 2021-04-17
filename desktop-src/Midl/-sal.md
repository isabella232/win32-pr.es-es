---
title: modificador/sal
description: El modificador/sal indica a MIDL que genere anotaciones SAL en los archivos de código auxiliar generados.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /sal modificador MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651334"
---
# <a name="sal-switch"></a>modificador/sal

El modificador **/sal** indica a MIDL que genere anotaciones sal en los archivos de código auxiliar generados.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

MIDL marcará los parámetros de puntero y matriz con anotaciones que reflejen la descripción del parámetro en el archivo IDL tal y como se aplica mediante RPC y el motor de serialización de NDR. MIDL no crea anotaciones para los parámetros de los métodos de interfaz marcados con el atributo [**\[ local \]**](local.md)a menos que [**/sal \_ local**](-sal-local.md) también esté presente en la línea de comandos. Para reemplazar la anotación generada por MIDL, utilice el atributo [**\[ Anotate \]**](annotate.md) .

Las anotaciones generadas por MIDL siempre tienen el prefijo \_ \_ RPC \_ y requieren el uso del encabezado **rpcsal. h** para traducir la anotación en anotaciones de sal estándar.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal \_ local**](-sal-local.md)
</dt> <dt>

[**\[anotar\]**](annotate.md)
</dt> </dl>

 

 




