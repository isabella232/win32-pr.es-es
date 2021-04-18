---
description: Los Estados de muestra definen operaciones de muestreo de textura como el direccionamiento de textura y el filtrado de textura.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumeración D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717690"
---
# <a name="d3dsamplerstatetype-enumeration"></a>Enumeración D3DSAMPLERSTATETYPE

Los Estados de muestra definen operaciones de muestreo de textura como el direccionamiento de textura y el filtrado de textura. Algunos Estados muestreador establecen el procesamiento de vértices y algún procesamiento de píxeles de configuración. Los Estados de muestra se pueden guardar y restaurar mediante stateblocks (vea el [Estado de guardado y restauración de los bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ ADDRESSU**
</dt> <dd>

Modo de dirección de textura para la coordenada u. El valor predeterminado es D3DTADDRESS \_ Wrap. Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**
</dt> <dd>

Modo de dirección de textura para la coordenada v. El valor predeterminado es D3DTADDRESS \_ Wrap. Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**
</dt> <dd>

Modo de dirección de textura para la coordenada w. El valor predeterminado es D3DTADDRESS \_ Wrap. Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**
</dt> <dd>

Color del borde o escriba [**D3DCOLOR**](d3dcolor.md). El color predeterminado es 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**
</dt> <dd>

Filtro de ampliación de tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). El valor predeterminado es D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**
</dt> <dd>

Filtro de minificación de tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). El valor predeterminado es D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**
</dt> <dd>

Filtro de mipmap que se va a utilizar durante minificación. Vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). El valor predeterminado es D3DTEXF \_ None.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**
</dt> <dd>

Sesgo de nivel de detalle del mipmap. El valor predeterminado es cero.

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**
</dt> <dd>

Índice de nivel de detalle del mapa más grande que se va a usar. Los valores van de 0 a (n-1), donde 0 es el mayor. El valor predeterminado es cero.

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**
</dt> <dd>

DWORD máximo anisotropía. Los valores van de 1 al valor que se especifica en el miembro **MaxAnisotropy** de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . El valor predeterminado es 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**
</dt> <dd>

Valor de corrección gamma. El valor predeterminado es 0, lo que significa que gamma es 1,0 y no se requiere ninguna corrección. De lo contrario, este valor significa que la muestra debe suponer un valor de gamma de 2,2 en el contenido y convertirla en lineal (gamma 1,0) antes de presentarla al sombreador de píxeles.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**
</dt> <dd>

Cuando se asigna una textura de múltiples elementos a la muestra, indica el índice de elemento que se va a usar. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**
</dt> <dd>

Desplazamiento de vértice en el mapa de desplazamiento premuestreado. Se trata de una constante usada por del teselador, su valor predeterminado es 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
