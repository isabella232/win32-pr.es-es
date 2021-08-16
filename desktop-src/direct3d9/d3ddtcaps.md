---
description: Constantes que describen los tipos de datos de vértice admitidos por un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ea92ee6fce4536747383c2180331af277eff22cd941dc57c2e0cec5612b4a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119415"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Constantes que describen los tipos de datos de vértice admitidos por un dispositivo.



| \#Definir              | Valor       | Descripción                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | Byte 4D sin signo.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Byte 4D sin signo normalizado. Cada uno de los cuatro bytes se normaliza dividiendo a 255,0.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | 4D normalizado corto sin signo, expandido a (primer byte/65535.0, segundo byte/65535.0, tercer byte/65535.0, cuarto byte/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | Formato 3D sin signo 10 10 10 expandido a (valor, valor, valor, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | Formato 10 10 10 con firma 3D normalizado y expandido a (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | Números de punto flotante 2D de 16 bits.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | Números de punto flotante 4D de 16 bits.                                                                                             |



 

El miembro DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|  Requisito                        | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



