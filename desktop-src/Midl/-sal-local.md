---
title: modificador/sal_local
description: El \_ conmutador local/sal dirige a MIDL para que también genere anotaciones sal para los parámetros de los métodos de interfaz marcados como \ local \. El modificador/sal también debe estar presente.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local modificador MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676291"
---
# <a name="sal_local-switch"></a>\_conmutador local de/sal

El **conmutador \_ local/sal** dirige a MIDL para que también genere anotaciones sal para los parámetros de los métodos de interfaz marcados como [**\[ locales \]**](local.md). El modificador [**/sal**](-sal.md) también debe estar presente.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Modifica el comportamiento del modificador [**/sal**](-sal.md) para proporcionar también anotaciones en los parámetros de los métodos de interfaz marcados con el atributo [**\[ local \]**](local.md) . Utilice el atributo [**\[ Anotate \]**](annotate.md)para invalidar la anotación generada por MIDL con una cadena de anotación diferente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[anotar\]**](annotate.md)
</dt> </dl>

 

 




