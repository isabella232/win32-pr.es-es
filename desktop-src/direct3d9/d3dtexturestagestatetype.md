---
description: Los Estados de la fase de textura definen las operaciones de textura de varios mezcladores.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumeración D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
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
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280285"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>Enumeración D3DTEXTURESTAGESTATETYPE

Los Estados de la fase de textura definen las operaciones de textura de varios mezcladores. Algunos Estados muestreador configuran el procesamiento de vértices y algunos establecen el procesamiento de píxeles. Los Estados de las fases de textura se pueden guardar y restaurar mediante stateblocks (vea el [Estado de guardado y restauración de los bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintaxis


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

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**
</dt> <dd>

El estado de la fase de textura es una operación de combinación de colores de textura identificada por un miembro del tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) . El valor predeterminado de la primera fase de textura (Stage 0) es D3DTOP \_ modular; para todas las demás fases, el valor predeterminado es D3DTOP \_ Disable.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

Texture: el estado de la fase es el primer argumento de color de la fase, identificado por uno de los [D3DTA](d3dta.md). El argumento predeterminado es D3DTA \_ Texture.

Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente. El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

Texture: el estado de la fase es el segundo argumento de color para la fase, identificado por [D3DTA](d3dta.md). El argumento predeterminado es D3DTA \_ Current. Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente. El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0)

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

El estado de la fase de textura es una operación de combinación alfa de textura identificada por un miembro del tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) . El valor predeterminado de la primera fase de textura (Stage 0) es D3DTOP \_ SELECTARG1 y, para todas las demás fases, el valor predeterminado es D3DTOP \_ Disable.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

Texture: el estado de la fase es el primer argumento alfa de la fase, identificado por [D3DTA](d3dta.md). El argumento predeterminado es D3DTA \_ Texture. Si no se establece ninguna textura para esta fase, el argumento predeterminado es D3DTA \_ difuso. Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente. El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

Texture: el estado de la fase es el segundo argumento alfa de la fase, identificado por [D3DTA](d3dta.md). El argumento predeterminado es D3DTA \_ Current. Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente. El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 0 0 en una matriz de asignación de rugosidad. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 0 1 en una matriz de asignación de rugosidad. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 1 0 en una matriz de asignación de rugosidad. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 1 1 en una matriz de asignación de rugosidad. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

Índice del conjunto de coordenadas de textura que se va a usar con esta fase de textura. Puede especificar hasta ocho conjuntos de coordenadas de textura por vértice. Si un vértice no incluye un conjunto de coordenadas de textura en el índice especificado, el sistema toma como valor predeterminado las coordenadas de la TI y la v (0,0).

Al representar mediante sombreadores de vértices, el índice de coordenadas de textura de cada fase debe establecerse en su valor predeterminado. El índice predeterminado de cada fase es igual al índice de fase. Establezca este estado en el índice de base cero del conjunto de coordenadas para cada vértice que use esta fase de textura.

Además, las aplicaciones pueden incluir, como Logical o con el índice que se está configurando, una de las constantes para solicitar que Direct3D genere automáticamente las coordenadas de textura de entrada para una transformación de textura. Para obtener una lista de todas las constantes, vea [D3DTSS \_ TCI](d3dtss-tci.md).

Con la excepción de D3DTSS \_ TCI \_ PASSTHRU, que se resuelve como cero, si alguno de los valores siguientes se incluye con el índice que se está configurando, el sistema usa el índice estrictamente para determinar el modo de ajuste de textura. Estas marcas son más útiles cuando se realiza la asignación de entorno.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

Valor de escala de punto flotante para la luminancia del mapa de rugosidad. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**
</dt> <dd>

Valor de desplazamiento de punto flotante para la luminancia del mapa de rugosidad. El valor predeterminado es 0.0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**
</dt> <dd>

Miembro del tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) que controla la transformación de coordenadas de textura para esta fase de textura. El valor predeterminado es D3DTTFF \_ Disable.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Configuración del operando de tercer color para las operaciones triadic (multiplicar, agregar y interpolar linealmente), identificada por [D3DTA](d3dta.md). Esta configuración es compatible Si \_ están presentes las capacidades del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ lerp. El argumento predeterminado es D3DTA \_ Current. Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente. El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Configuración del operando selector de canal alfa para las operaciones triadic (multiplicar, agregar y interpolar linealmente), identificada por [D3DTA](d3dta.md). Esta configuración es compatible Si \_ están presentes las capacidades del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ lerp. El argumento predeterminado es D3DTA \_ Current. Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura. D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente. El argumento predeterminado es (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

Configuración para seleccionar el registro de destino para el resultado de esta fase, identificado por [D3DTA](d3dta.md). Este valor se puede establecer en D3DTA \_ Current (el valor predeterminado) o en D3DTA \_ temp, que es un registro temporal único que se puede leer en fases posteriores como argumento de entrada. El color final que se pasa al mezclador de niebla y al búfer de fotogramas se toma del D3DTA \_ actual, por lo que el último estado activo de la fase de textura debe establecerse para escribir en el actual. Esta configuración es compatible Si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ constante)**
</dt> <dd>

Color constante por fase. Para ver si un dispositivo admite un color constante por fase, consulte la constante D3DPMISCCAPS \_ PERSTAGECONSTANT en [D3DPMISCCAPS](d3dpmisccaps.md). La constante \_ D3DTA usa la constante D3DTSS \_ . Vea [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de este tipo enumerado se usan con los métodos [**IDirect3DDevice9:: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) y [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para recuperar y establecer los valores de estado de textura.

El intervalo válido de valores para los \_ coeficientes de la matriz de D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 y D3DTSS \_ BUMPENVMAT11 es mayor o igual que-8,0 y menor que 8,0. Este intervalo, expresado en notación matemática, es (-8.0, 8.0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
