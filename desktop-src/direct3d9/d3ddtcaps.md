---
description: Constantes que describen los tipos de datos de vértices admitidos por un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696114"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Constantes que describen los tipos de datos de vértices admitidos por un dispositivo.



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| \#define              | Value       | Descripción                                                                                                                   |
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | 4D sin signo.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Byte sin signo normalizado y 4D. Cada uno de los cuatro bytes se normaliza dividiendo en 255,0.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normalizado, 2D con signo corto, expandido a (primer byte/32767.0, segundo byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalizado, 4D con signo corto, expandido a (primer byte/32767.0, segundo byte/32767.0, tercer byte/32767.0, cuarto byte/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalizado, 2D sin signo corto, expandido a (primer byte/65535.0, segundo byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | 4D normalizado sin signo, expandido a (primer byte/65535.0, segundo byte/65535.0, tercer byte/65535.0, cuarto byte/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | formato 3D sin signo 10 10 10 expandido a (valor, valor, valor, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | formato 3D con signo 10 10 10 normalizado y expandido a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | números de punto flotante de 16 bits 2D.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | 4D números de punto flotante de 16 bits.                                                                                             |



 

El miembro DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



