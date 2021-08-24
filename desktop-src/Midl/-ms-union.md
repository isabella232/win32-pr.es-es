---
title: Modificador /ms_union
description: 'El modificador de unión /ms controla la alineación de MUTACIÓN de las uniones \_ no superadas. Nota: Este atributo se proporciona para la compatibilidad con versiones anteriores.'
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union switch MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b8e2f4b86929954ad67c845cf546d46f5950698fce7c21d721613af3611a066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811395"
---
# <a name="ms_union-switch"></a>Modificador de unión /ms \_

El **modificador \_ de unión /ms** controla la alineación de MUTACIÓN de las uniones no superadas.

> [!Note]  
> Este atributo se proporciona por compatibilidad con versiones anteriores. No se recomienda su uso en una nueva interfaz.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

El compilador MIDL refleja el comportamiento del compilador IDL de OSF-DCE para las uniones no superadas. Sin embargo, dado que las versiones anteriores del compilador MIDL no lo hacían, el modificador de unión **/ms \_** proporciona compatibilidad con interfaces creadas en versiones anteriores del compilador MIDL.

La característica de unión ms se puede usar como un modificador de línea de comandos \_ (**/ms \_ union),** un atributo de interfaz IDL o como un atributo de tipo IDL.

## <a name="examples"></a>Ejemplos

**midl /ms \_ union file.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




