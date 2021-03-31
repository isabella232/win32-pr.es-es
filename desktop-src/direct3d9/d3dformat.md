---
description: Define los distintos tipos de formatos de superficie.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821167"
---
# <a name="d3dformat"></a>D3DFORMAT

Define los distintos tipos de formatos de superficie.

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a>Observaciones

Hay varios tipos de formatos:

-   [Formato de búfer o de pantalla](#backbuffer-or-display-formats)
-   [Formatos de búfer](#buffer-formats)
-   [DXTn formatos de textura comprimidos](#dxtn-compressed-texture-formats)
-   [Formatos de punto flotante](#floating-point-formats)
-   [Formatos FOURCC](#fourcc-formats)
-   [Formatos IEEE](#ieee-formats)
-   [Formatos mixtos](#mixed-formats)
-   [Formatos con signo](#signed-formats)
-   [Formatos sin signo](#unsigned-formats)
-   [Otros](#other)

Todos los formatos se muestran de izquierda a derecha, el bit más significativo al bit menos significativo. Por ejemplo, el **D3DFORMAT \_ ARGB** se ordena desde el canal de bits más significativo a (alfa) hasta el canal de bits menos significativo B (azul). Al atravesar los datos de la superficie, los datos se almacenan en la memoria desde el bit menos significativo hasta el bit más significativo, lo que significa que el orden de los canales en la memoria se encuentra entre el bit menos significativo (azul) y el bit más significativo (alfa).

El valor predeterminado para los formatos que contienen canales sin definir (G16R16, A8, etc.) es 1. La única excepción es el formato A8, que se inicializa en 000 para los tres canales de color.

El orden de los bits es del byte más significativo primero, por lo que D3DFMT \_ A8L8 indica que el byte alto de este formato de 2 bytes es alfa. **D3DFMT \_ D16** indica un valor entero de 16 bits y una superficie bloqueada por la aplicación.

Se han elegido formatos de píxel para habilitar la expresión de formatos de extensión definidos por el fabricante de hardware, así como para incluir el método FOURCC bien establecido. El conjunto de formatos comprendido por el tiempo de ejecución de Direct3D se define mediante D3DFORMAT.

Tenga en cuenta que los formatos que proporcionan los proveedores de hardware independientes (IHV) y muchos códigos FOURCC no aparecen en la lista. Los formatos de esta enumeración son únicos en que los autoriza el tiempo de ejecución, lo que significa que el rasterizador de referencia funcionará en todos estos tipos. Los formatos proporcionados por IHV serán compatibles con los IHV individuales en cada tarjeta.

### <a name="backbuffer-or-display-formats"></a>Formato de búfer o de pantalla

Estos formatos son los únicos formatos válidos para un búfer de reserva o una pantalla.



| Formato      | Búfer de reserva | Pantalla                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (solo en modo de pantalla completa) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Formatos de búfer

Los búferes de profundidad, estarcido, vértice y índice tienen formatos únicos.



| Marcas de búfer               | Value | Formato                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ bloqueable**  | 70    | profundidad de bits de búfer z de 16 bits.                                                                                                                    |
| **D3DFMT \_ D32**            | 71    | profundidad de bits de búfer z de 32 bits.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | profundidad de bits de búfer z de 16 bits donde se reservan 15 bits para el canal de profundidad y 1 bit se reserva para el canal de estarcido.                     |
| **D3DFMT \_ D24S8**          | 75    | profundidad de bits de búfer z de 32 bits con 24 bits para el canal de profundidad y 8 bits para el canal de estarcido.                                             |
| **D3DFMT \_ D24X8**          | 77    | profundidad de bits de búfer z de 32 bits con 24 bits para el canal de profundidad.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | profundidad de bits de búfer z de 32 bits con 24 bits para el canal de profundidad y 4 bits para el canal de estarcido.                                             |
| **D3DFMT \_ D32F \_ bloqueable** | 82    | Formato bloqueable en el que el valor de profundidad se representa como un número de punto flotante estándar IEEE.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Formato no bloqueable que contiene 24 bits de profundidad (en formato de punto flotante de 24 bits-20e4) y 8 bits de estarcido.                        |
| **D3DFMT \_ D32 \_ bloqueable**  | 84    | Un búfer de profundidad de bits de 32 con bloqueos. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/>  |
| **D3DFMT \_ S8 \_ bloqueable**   | 85    | Búfer de estarcido de 8 bits que se bloquea. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/> |
| **D3DFMT \_ D16**            | 80    | profundidad de bits de búfer z de 16 bits.                                                                                                                    |
| **D3DFMT \_ VERTEXDATA**     | 100   | Describe una superficie de búfer de vértices.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | profundidad de bits de búfer de índice de 16 bits.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | profundidad de bits de búfer de índice de 32 bits.                                                                                                                |



 

Todos los formatos de la galería de símbolos de profundidad, excepto D3DFMT \_ D16, \_ no indican ninguna ordenación de bits determinada por píxel y el controlador puede consumir más del número indicado de canal de bits por profundidad (pero no canal de estarcido).

### <a name="dxtn-compressed-texture-formats"></a>DXTn formatos de textura comprimidos

Estas marcas se utilizan para las texturas comprimidas:



| DXTn marcas de textura comprimidas | Value                          | Formato                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | MAKEFOURCC (' D ', ' X ', ' T ', ' 1 ') | Formato de textura de compresión DXT1 |
| **D3DFMT \_ DXT2**              | MAKEFOURCC (' D ', ' X ', ' T ', ' 2 ') | Formato de textura de compresión DXT2 |
| **D3DFMT \_ DXT3**              | MAKEFOURCC (' D ', ' X ', ' T ', ' 3 ') | Formato de textura de compresión DXT3 |
| **D3DFMT \_ DXT4**              | MAKEFOURCC (' D ', ' X ', ' T ', ' 4 ') | Formato de textura de compresión DXT4 |
| **D3DFMT \_ DXT5**              | MAKEFOURCC (' D ', ' X ', ' T ', ' 5 ') | Formato de textura de compresión DXT5 |



 

El tiempo de ejecución no permitirá que una aplicación cree una superficie con un formato DXTn a menos que las dimensiones de la superficie sean múltiplos de 4. Esto se aplica a las superficies sin formato, los destinos de representación, las texturas 2D, las texturas de cubo y las texturas de volumen.

### <a name="floating-point-formats"></a>Formatos de Floating-Point

Estas marcas se usan para los formatos de superficie de punto flotante. Estos formatos de 16 bits por canal también se conocen como formatos s10e5.



| Marcas de punto flotante      | Value | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | formato Float de 16 bits con 16 bits para el canal rojo.                                   |
| **D3DFMT \_ G16R16F**       | 112   | formato Float de 32 bits con 16 bits para el canal rojo y 16 bits para el canal verde. |
| **D3DFMT \_ A16B16G16R16F** | 113   | formato Float de 64 bits con 16 bits para cada canal (alfa, azul, verde, rojo).        |



 

### <a name="fourcc-formats"></a>Formatos FOURCC

Los datos en formato FOURCC son datos comprimidos.

### <a name="makefourcc"></a>MAKEFOURCC

A continuación se muestra una macro para generar códigos de cuatro caracteres:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Estos son los formatos FOURCC definidos:



| Marcas FOURCC              | Value                          | Formato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTI2 \_ ARGB8** | MAKEFOURCC (' M ', ' E ', ' T ', ' 1 ')    | Textura de múltiples elementos (no comprimida)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC (' G ', ' R ', ' G ', ' B ') | Formato RGB empaquetado de 16 bits análogo a YUY2 (Y0U0, Y1V0, Y2U2, etc.). Requiere un par de píxeles para representar correctamente el valor de color. El primer píxel del par contiene 8 bits de color verde (en los 8 bits superiores) y 8 bits de rojo (en los 8 bits inferiores). El segundo píxel contiene 8 bits de verde (en los 8 bits superiores) y 8 bits de azul (en los 8 bits inferiores). Juntos, los dos píxeles comparten los componentes rojo y azul, mientras que cada uno tiene un componente verde único (G0R0, G1B0, G2R2, etc.). La muestra de textura no normaliza los colores al buscar en un sombreador de píxeles; permanecen en el intervalo de 0,0 f a 255.0 f. Esto se aplica a todos los modelos de sombreador de píxeles programables. Para el sombreador de píxeles de función fija, el hardware debe normalizarse en el intervalo 0. f a 1. f y tratarlo esencialmente como textura YUY2. El hardware que expone este formato debe tener el miembro PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) establecido en un valor capaz de controlar ese intervalo. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC (' R ', ' G ', ' B ', ' G ') | Formato RGB empaquetado de 16 bits análogo a UYVY (U0Y0, V0Y1, U2Y2, etc.). Requiere un par de píxeles para representar correctamente el valor de color. El primer píxel del par contiene 8 bits de color verde (en los 8 bits inferiores) y 8 bits de rojo (en los 8 bits superiores). El segundo píxel contiene 8 bits de color verde (en los 8 bits inferiores) y 8 bits de azul (en los 8 bits superiores). Juntos, los dos píxeles comparten los componentes rojo y azul, mientras que cada uno tiene un componente verde único (R0G0, B0G1, R2G2, etc.). La muestra de textura no normaliza los colores al buscar en un sombreador de píxeles; permanecen en el intervalo de 0,0 f a 255.0 f. Esto se aplica a todos los modelos de sombreador de píxeles programables. Para el sombreador de píxeles de función fija, el hardware debe normalizarse en el intervalo 0. f a 1. f y tratarlo esencialmente como textura YUY2. El hardware que expone este formato debe tener el miembro PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) establecido en un valor capaz de controlar ese intervalo.     |
| **D3DFMT \_ UYVY**          | MAKEFOURCC (' U ', ' Y ', ' V ', ' Y ') | Formato UYVY (compatibilidad con PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ YUY2**          | MAKEFOURCC (' Y ', ' U ', ' Y ', ' 2 ') | Formato YUY2 (compatibilidad con PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>Formatos IEEE

Estas marcas se usan para los formatos de superficie de punto flotante. Estos formatos de 32 bits por canal también se conocen como formatos s23e8.



| Marcas de punto flotante      | Value | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | formato Float de 32 bits con 32 bits para el canal rojo.                                   |
| **D3DFMT \_ G32R32F**       | 115   | formato Float de 64 bits con 32 bits para el canal rojo y 32 bits para el canal verde. |
| **D3DFMT \_ A32B32G32R32F** | 116   | formato Float de 128 bits con 32 bits para cada canal (alfa, azul, verde, rojo).       |



 

### <a name="mixed-formats"></a>Formatos mixtos

Los datos en formatos mixtos pueden contener una combinación de datos sin firmar y datos firmados.



| Marcas de formato mixtas      | Value | Formato                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | formato de mapa de rugosidad de 16 bits con luminancia usando 6 bits para luminancia y 5 bits cada uno para v y usted. |
| **D3DFMT \_ X8L8V8U8**    | 62    | formato de mapa de rugosidad de 32 bits con luminancia usando 8 bits para cada canal.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | formato de mapa de rugosidad de 32 bits con 2 bits para Alpha y 10 bits cada uno para w, v y usted.                |



 

### <a name="signed-formats"></a>Formatos con signo

Los datos en un formato con signo pueden ser positivos y negativos. Los formatos con signo usan combinaciones de los datos (U), (V), (W) y (Q).



| Marcas de formato con signo      | Value | Formato                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | formato de mapa de rugosidad de 16 bits con 8 bits para cada uno de los datos de usuario y v.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | formato de mapa de rugosidad de 32 bits con 8 bits para cada canal.                                                     |
| **D3DFMT \_ V16U16**       | 64    | formato de mapa de rugosidad de 32 bits con 16 bits para cada canal.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | formato de mapa de rugosidad de 64 bits con 16 bits para cada componente.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | formato de compresión normal de 16 bits. La muestra de textura calcula el canal de C desde: C = sqrt (1-U ²-V ²). |



 

### <a name="unsigned-formats"></a>Formatos sin signo

Los datos en un formato sin signo deben ser positivos. Los formatos sin signo usan combinaciones de los datos (R) Ed, (G) reen, (B) lue, (A) LPHA, (L) uminance y (P) Alette. Los datos de la paleta también se conocen como datos indizados de color, ya que los datos se utilizan para indizar una paleta de colores.



| Marcas de formato sin signo             | Value | Formato                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | formato de píxel RGB de 24 bits con 8 bits por canal.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | formato de píxel ARGB de 32 bits con alfa, con 8 bits por canal.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | formato de píxel RGB de 32 bits, donde se reservan 8 bits para cada color.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | formato de píxel RGB de 16 bits con 5 bits para rojo, 6 bits para verde y 5 bits para azul.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | formato de píxel de 16 bits en el que se reservan 5 bits para cada color.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | formato de píxel de 16 bits en el que se reservan 5 bits para cada color y 1 bit se reserva para alpha.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | formato de píxel ARGB de 16 bits con 4 bits para cada canal.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | formato de textura RGB de 8 bits que usa 3 bits para rojo, 3 bits para verde y 2 bits para azul.                                                                                     |
| **D3DFMT \_ A8**                    | 28    | solo alfa de 8 bits.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | formato de textura ARGB de 16 bits con 8 bits para alfa, 3 bits cada uno para rojo y verde, y 2 bits para azul.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | formato de píxel RGB de 16 bits con 4 bits para cada color.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | formato de píxel de 32 bits con 10 bits para cada color y 2 bits para alpha.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | formato de píxel ARGB de 32 bits con alfa, con 8 bits por canal.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | formato de píxel RGB de 32 bits, donde se reservan 8 bits para cada color.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | formato de píxel de 32 bits con 16 bits cada uno para verde y rojo.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | formato de píxel de 32 bits con 10 bits cada uno para rojo, verde y azul, y 2 bits para alfa.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | formato de píxel de 64 bits con 16 bits para cada componente.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | color de 8 bits indizado con 8 bits de alfa.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | color de 8 bits indexado.                                                                                                                                                      |
| **D3DFMT \_ L8**                    | 50    | solo luminancia de 8 bits.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | solo luminancia de 16 bits.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16 bits con 8 bits para cada alfa y luminancia.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8 bits con 4 bits cada uno para alfa y luminancia.                                                                                                                          |
| **D3DFMT \_ a1**                    | 118   | monocromo de 1 bit. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR \_** | 119   | 2,8: punto fijo sesgado. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/>                                      |
| **D3DFMT \_ BINARYBUFFER**          | 199   | Formato binario que indica que los datos no tienen ningún tipo inherente. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/> |



 

### <a name="other"></a>Otros

Esta marca se utiliza para los formatos no definidos.



| Otras marcas         | Value | Formato                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ desconocido** | 0     | El formato de la superficie es desconocido |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




