---
title: Modificador /win64
description: El modificador /win64 dirige al compilador MIDL a generar archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 64 bits. Nota Este modificador está obsoleto.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /win64 switch MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159694"
---
# <a name="win64-switch"></a>Modificador /win64

El **modificador /win64** dirige al compilador MIDL a generar archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 64 bits.

> [!Note]  
> Este modificador está obsoleto. Use el modificador [**/ia64**](-ia64.md) o [**/amd64**](-amd64.md) en su lugar. El **modificador /win64** es equivalente al **modificador /ia64.**

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El **modificador /win64** equivale a establecer el modificador [**/env**](-env.md) en win64.

> [!Note]  
> No es posible usar MIDL.exe para generar un tlb de 64 bits en Windows 2000.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




