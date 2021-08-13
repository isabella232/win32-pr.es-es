---
title: Modificador /tlb
description: El modificador /tlb especifica un nombre de archivo para la biblioteca de tipos generada por el compilador midl.
ms.assetid: 7d5d9f92-ed1a-46bc-beb1-4be70d0a4813
keywords:
- /tlb switch MIDL
topic_type:
- apiref
api_name:
- /tlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081723648788ec51fa65a4770deb336f665804a9527dc223000826870dbe1ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643755"
---
# <a name="tlb-switch"></a>Modificador /tlb

El **modificador /tlb** especifica un nombre de archivo para la biblioteca de tipos generada por el compilador midl.

``` syntax
midl /tlb filename
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*filename* 
</dt> <dd>

Especifica el nombre del archivo de biblioteca de tipos de salida (TLB). De forma predeterminada, si no se usa el modificador **/tlb,** el archivo TLB tiene el mismo nombre que el archivo IDL, con la extensión . Tlb.

</dd> </dl>

## <a name="examples"></a>Ejemplos

**midl /tlb newname.tlb**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/notlb**](-notlb.md)
</dt> </dl>

 

 




