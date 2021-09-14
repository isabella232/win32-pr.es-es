---
description: Las definiciones siguientes se deben usar al leer y escribir directamente el encabezado binario.
ms.assetid: 19c36f94-8088-417d-867d-3a02912087dc
title: Encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfaa589382812cfd752d47cc8b95cda0139385b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060637"
---
# <a name="header"></a>Encabezado

Las definiciones siguientes se deben usar al leer y escribir directamente el encabezado binario.

> [!Note]  
> Los flujos de datos comprimidos no se admiten actualmente y, por tanto, no se detallan aquí.

 


```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación binaria](binary-encoding.md)
</dt> </dl>

 

 



