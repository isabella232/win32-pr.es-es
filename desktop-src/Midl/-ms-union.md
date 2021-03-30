---
title: modificador/ms_union
description: El \_ modificador de/MS Union controla la alineación del NDR de las uniones no encapsuladas. Nota Este atributo se proporciona por compatibilidad con versiones anteriores.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union modificador MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904176"
---
# <a name="ms_union-switch"></a>\_conmutador de Unión/MS

El modificador de **/MS \_ Union** controla la alineación del NDR de las uniones no encapsuladas.

> [!Note]  
> Este atributo se proporciona por compatibilidad con versiones anteriores. No se recomienda su uso en una nueva interfaz.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El compilador MIDL refleja el comportamiento del compilador de de OSF-DCE IDL para las uniones no encapsuladas. Sin embargo, dado que las versiones anteriores del compilador de MIDL no lo hacían, el modificador **/MS \_ Union** proporciona compatibilidad con las interfaces creadas en versiones anteriores del compilador de MIDL.

La \_ característica MS Union se puede usar como un modificador de la línea de comandos (**/MS \_ Union**), un atributo de interfaz IDL o como un atributo de tipo IDL.

## <a name="examples"></a>Ejemplos

**archivo de \_ Unión MIDL/ms. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




