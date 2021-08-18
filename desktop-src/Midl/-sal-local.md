---
title: Modificador /sal_local
description: El modificador local /sal hace que MIDL también genere anotaciones SAL para parámetros de \_ métodos de interfaz marcados como \local\. El modificador /sal también debe estar presente.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local switch MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666401cca482846fc2e6a9d5851a4da9d2d362279c9bc1496ab672a94ac9b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014093"
---
# <a name="sal_local-switch"></a>Modificador local /sal \_

El **modificador \_ local /sal** hace que MIDL también genere anotaciones SAL para los parámetros de los métodos de interfaz marcados [**\[ como locales. \]**](local.md) El [**modificador /sal**](-sal.md) también debe estar presente.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Modifica el comportamiento del modificador [**/sal**](-sal.md) para proporcionar también anotaciones en los parámetros de los métodos de interfaz marcados con el [**\[ atributo local. \]**](local.md) Use el [**\[ atributo \] anotación**](annotate.md)para invalidar la anotación generada por MIDL con una cadena de anotación diferente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[Anotar\]**](annotate.md)
</dt> </dl>

 

 




