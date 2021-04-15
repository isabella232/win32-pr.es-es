---
description: Declara un objeto para que sea una constante de selección, para evitar recargas redundantes de ese objeto si se usa (y se declara) en varios lugares de la biblioteca de DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST (macro)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715569"
---
# <a name="xmglobalconst-macro"></a>XMGLOBALCONST (macro)

Declara un objeto para que sea una constante *de selección* , para evitar recargas redundantes de ese objeto si se usa (y se declara) en varios lugares de la biblioteca de DirectXMath.

## <a name="syntax"></a>Sintaxis

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Observaciones

El uso de XMGLOBALCONST permite la especificación de constantes globales. Esto ayuda a reducir el tamaño del segmento de datos de una aplicación, evitar la creación y destrucción de objetos redundantes, y reducir las operaciones de carga y almacenamiento.

## <a name="requirements"></a>Requisitos

**Encabezado:** Declarado en DirectXMath. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Macros de biblioteca de DirectXMath](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Constantes globales en la biblioteca de DirectXMath](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[modificado](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
