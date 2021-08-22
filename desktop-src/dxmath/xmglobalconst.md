---
description: Declara un objeto como una constante pick-any para evitar recargas redundantes de ese objeto si se usa (y declara) en varios lugares de la biblioteca DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Macro XMGLOBALCONST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be72254865aed46de86955c2a27a4d73351311c5aa63a44a6e218be7a3915d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118005"
---
# <a name="xmglobalconst-macro"></a>Macro XMGLOBALCONST

Declara un objeto como una constante *pick-any* para evitar recargas redundantes de ese objeto si se usa (y declara) en varios lugares de la biblioteca DirectXMath.

## <a name="syntax"></a>Sintaxis

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Comentarios

El uso de XMGLOBALCONST permite especificar constantes globales. Esto ayuda a reducir el tamaño del segmento de datos de una aplicación, evitar la creación y destrucción de objetos redundantes y reducir las operaciones de carga y almacenamiento.

## <a name="requirements"></a>Requisitos

**Encabezado:** Declarado en DirectXMath.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Macros de biblioteca de DirectXMath](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Constantes globales en la biblioteca DirectXMath](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
