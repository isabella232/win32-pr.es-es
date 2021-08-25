---
description: Los estados de la fase de textura definen operaciones de textura de varias mezclas.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumeración D3DTEXTURESTAGESTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4879009f603a6943302f0595f37176ec5edf8e1a1d3212efedb66c923d775104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894155"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>D3DTEXTURESTAGESTATETYPE (enumeración)

Los estados de la fase de textura definen operaciones de textura de varias mezclas. Algunos estados del muestreador establecen el procesamiento de vértices y otros, el procesamiento de píxeles. Los estados de la fase de textura se pueden guardar y restaurar mediante bloques de estado (vea State Blocks Save and Restore State (Direct3D 9) [Bloques de estado guardar y restaurar estado [(Direct3D 9)]).](state-blocks-save-and-restore-state.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**COLOROP de D3DTSS \_**
</dt> <dd>

El estado de la fase de textura es una operación de combinación de colores de textura identificada por un miembro del tipo enumerado [**D3DTEXTUREOP.**](./d3dtextureop.md) El valor predeterminado de la primera fase de textura (fase 0) es D3DTOPMODULTE; para todas las demás fases, el valor predeterminado \_ es D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

El estado de la fase de textura es el primer argumento de color de la fase, identificado por uno de [los D3DTA](d3dta.md). El argumento predeterminado es TEXTURA D3DTA. \_

Especifique D3DTA \_ TEMP para seleccionar un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP está presente. El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

El estado de la fase de textura es el segundo argumento de color de la fase, identificado por [D3DTA.](d3dta.md) El argumento predeterminado es D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para seleccionar un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP está presente. El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0)

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

El estado de la fase de textura es una operación de mezcla alfa de textura identificada por un miembro del tipo enumerado [**D3DTEXTUREOP.**](./d3dtextureop.md) El valor predeterminado de la primera fase de textura (fase 0) es D3DTOP SELECTARG1 y, para todas las demás fases, el valor predeterminado \_ es D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

El estado de la fase de textura es el primer argumento alfa para la fase, identificado por [D3DTA.](d3dta.md) El argumento predeterminado es TEXTURA D3DTA. \_ Si no se establece ninguna textura para esta fase, el argumento predeterminado es D3DTA \_ DIFUSO. Especifique D3DTA \_ TEMP para seleccionar un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP está presente. El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

El estado de la fase de textura es el segundo argumento alfa para la fase, identificado por [D3DTA.](d3dta.md) El argumento predeterminado es D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para seleccionar un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP está presente. El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

El estado de la fase de textura es un valor de punto flotante para el coeficiente \[ \] \[ 0 0 \] en una matriz de asignación de protuberancias. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

El estado de la fase de textura es un valor de punto flotante para el coeficiente \[ \] \[ 0 1 \] en una matriz de asignación de protuberancias. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

El estado de la fase de textura es un valor de punto flotante para el coeficiente \[ \] \[ 1 0 \] en una matriz de asignación de protuberancias. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

El estado de la fase de textura es un valor de punto flotante para \[ el coeficiente \] \[ 1 1 \] en una matriz de asignación de protuberancias. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

Índice del conjunto de coordenadas de textura que se va a usar con esta fase de textura. Puede especificar hasta ocho conjuntos de coordenadas de textura por vértice. Si un vértice no incluye un conjunto de coordenadas de textura en el índice especificado, el sistema tiene como valor predeterminado las coordenadas you y v (0,0).

Al representar con sombreadores de vértices, el índice de coordenadas de textura de cada fase debe establecerse en su valor predeterminado. El índice predeterminado de cada fase es igual al índice de fase. Establezca este estado en el índice de base cero del conjunto de coordenadas para cada vértice que use esta fase de textura.

Además, las aplicaciones pueden incluir, como or lógico con el índice que se establece, una de las constantes para solicitar que Direct3D genere automáticamente las coordenadas de textura de entrada para una transformación de textura. Para obtener una lista de todas las constantes, vea [D3DTSS \_ TCI](d3dtss-tci.md).

A excepción de D3DTSS \_ TCI PASSTHRU, que se resuelve en cero, si alguno de los siguientes valores se incluye con el índice que se establece, el sistema usa el índice estrictamente para determinar el modo de ajuste de \_ textura. Estas marcas son más útiles al realizar la asignación de entorno.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

Valor de escala de punto flotante para la luminosidad del mapa de protuberancia. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**BUMPENVLOFFSET de D3DTSS \_**
</dt> <dd>

Valor de desplazamiento de punto flotante para la luminosidad del mapa de protuberancia. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**TEXTURA DE \_ D3DTSSTRANSFORMFLAGS**
</dt> <dd>

Miembro del tipo [**enumerado D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) que controla la transformación de las coordenadas de textura para esta fase de textura. El valor predeterminado es D3DTTFF \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Configuración para el tercer operando de color para las operaciones triadicas (multiplicar, agregar e interpolar linealmente), identificado por [D3DTA](d3dta.md). Esta configuración se admite si las funcionalidades de dispositivo LERP D3DTEXOPCAPS MULTIPLYADD o \_ D3DTEXOPCAPS \_ están presentes. El argumento predeterminado es D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para seleccionar un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP está presente. El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Configuración para el operando selector de canal alfa para operaciones triadicas (multiplicar, agregar e interpolar linealmente), identificado por [D3DTA](d3dta.md). Esta configuración se admite si las funcionalidades de dispositivo LERP D3DTEXOPCAPS MULTIPLYADD o \_ D3DTEXOPCAPS \_ están presentes. El argumento predeterminado es D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para seleccionar un color de registro temporal para lectura o escritura. Se admite D3DTA TEMP si la funcionalidad del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP está presente. El argumento predeterminado es (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

Establecer para seleccionar el registro de destino para el resultado de esta fase, identificado por [D3DTA](d3dta.md). Este valor se puede establecer en D3DTA CURRENT (el valor predeterminado) o en \_ D3DTA TEMP, que es un único registro temporal que se puede leer en fases posteriores como argumento de \_ entrada. El color final pasado al blender y al búfer de fotogramas de blender se toma de D3DTA CURRENT, por lo que el último estado activo de la fase de textura debe establecerse para escribir \_ en current. Esta configuración se admite si la funcionalidad del dispositivo D3DPMISCCAPS \_ TSSARGTEMP está presente.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ CONSTANTE**
</dt> <dd>

Color constante por fase. Para ver si un dispositivo admite un color constante por fase, vea la constante D3DPMISCCAPS \_ PERSTAGECONSTANT en [D3DPMISCCAPS](d3dpmisccaps.md). D3DTSS \_ CONSTANT se usa en D3DTA \_ CONSTANT. Consulte [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de este tipo enumerado se usan con los métodos [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) e [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para recuperar y establecer valores de estado de textura.

El intervalo válido de valores para D3DTSS \_ BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 y D3DTSS BUMPENVMAT11 es mayor o igual que -8,0 y menor que \_ 8,0. Este intervalo, expresado en notación matemática es (-8.0,8.0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
