---
title: modificador/Win64
description: El modificador/Win64 indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 64 bits. Tenga en cuenta que este modificador está obsoleto.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /Win64 modificador MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358026"
---
# <a name="win64-switch"></a>modificador/Win64

El modificador **/Win64** indica al compilador de MIDL que genere archivos de código auxiliar, o un archivo de biblioteca de tipos, para un entorno de 64 bits.

> [!Note]  
> Este modificador está obsoleto. En su lugar, use el modificador [**/ia64**](-ia64.md) o [**/AMD64**](-amd64.md) . El modificador **/Win64** es equivalente al modificador **/ia64** .

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El modificador **/Win64** es equivalente a establecer el modificador [**/env**](-env.md) en Win64.

> [!Note]  
> No es posible usar MIDL.exe para generar un TLB de 64 bits en Windows 2000.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/ENV**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




