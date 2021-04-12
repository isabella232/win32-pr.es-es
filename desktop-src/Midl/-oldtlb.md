---
title: modificador/oldtlb
description: El modificador/oldtlb indica al compilador de MIDL que genere una biblioteca de tipos de formato antiguo.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb modificador MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420599"
---
# <a name="oldtlb-switch"></a>modificador/oldtlb

El modificador **/oldtlb** indica al compilador de MIDL que genere una biblioteca de tipos de formato antiguo.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El modificador **/oldtlb** invalida el valor predeterminado y dirige el compilador MIDL para generar bibliotecas de tipos de formato antiguo incluso en las versiones actuales de Windows mediante [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) en lugar de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).

## <a name="examples"></a>Ejemplos

**MIDL/oldtlb nombrearchivo. idl**

**/oldtlb myoldodl. ODL de MIDL**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 