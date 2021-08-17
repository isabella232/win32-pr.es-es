---
description: Define los distintos tipos de formatos de superficie.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types.h)
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
ms.openlocfilehash: ec3f934d9d94bfcc1129414b652de770d205b6e190b9f901c6e4f35768f59217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732407"
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

## <a name="remarks"></a>Comentarios

Hay varios tipos de formatos:

-   [BackBuffer o formatos de presentación](#backbuffer-or-display-formats)
-   [Formatos de búfer](#buffer-formats)
-   [Formatos de textura comprimida dxtn](#dxtn-compressed-texture-formats)
-   [Formatos de punto flotante](#floating-point-formats)
-   [Formatos FOURCC](#fourcc-formats)
-   [Formatos IEEE](#ieee-formats)
-   [Formatos mixtos](#mixed-formats)
-   [Formatos firmados](#signed-formats)
-   [Formatos sin signo](#unsigned-formats)
-   [Otros](#other)

Todos los formatos se muestran de izquierda a derecha, bit más significativo a bit menos significativo. Por ejemplo, **D3DFORMAT \_ ARGB** se ordena desde el canal de bits A (alfa) más significativo hasta el canal de bits B (azul) menos significativo. Al recorrer los datos de la superficie, los datos se almacenan en memoria desde el bit menos significativo al bit más significativo, lo que significa que el orden del canal en la memoria va desde el bit menos significativo (azul) al bit más significativo (alfa).

El valor predeterminado para los formatos que contienen canales no definidos (G16R16, A8, entre otros) es 1. La única excepción es el formato A8, que se inicializa en 000 para los tres canales de color.

El orden de los bits es del byte más significativo primero, por lo que D3DFMT A8L8 indica que el byte alto de este formato de 2 bytes \_ es alfa. **D3DFMT \_ D16** indica un valor entero de 16 bits y una superficie que se puede bloquear por la aplicación.

Los formatos de píxel se han elegido para habilitar la expresión de formatos de extensión definidos por el proveedor de hardware, así como para incluir el método FOURCC bien establecido. D3DFORMAT define el conjunto de formatos que entiende el entorno de ejecución de Direct3D.

Tenga en cuenta que los formatos los proporcionan proveedores de hardware independientes (IHV) y muchos códigos FOURCC no aparecen en la lista. Los formatos de esta enumeración son únicos, ya que están autorizados por el tiempo de ejecución, lo que significa que el rasterizador de referencia funcionará en todos estos tipos. Los formatos proporcionados por IHV serán compatibles con los IHV individuales en cada tarjeta.

### <a name="backbuffer-or-display-formats"></a>BackBuffer o formatos de presentación

Estos formatos son los únicos válidos para un búfer de reserva o una presentación.



| Formato      | Búfer de reserva | Mostrar                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (solo en modo de pantalla completa) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Formatos de búfer

Los búferes de profundidad, galería de símbolos, vértices e índices tienen formatos únicos.



| Marcas de búfer               | Value | Formato                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ LOCKABLE**  | 70    | Profundidad de bits de búfer z de 16 bits.                                                                                                                    |
| **D3DFMT \_ D32**            | 71    | Profundidad de bits del búfer z de 32 bits.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | Profundidad de bits de búfer z de 16 bits donde 15 bits están reservados para el canal de profundidad y 1 bit está reservado para el canal de galería de símbolos.                     |
| **D3DFMT \_ D24S8**          | 75    | Profundidad de bits de búfer z de 32 bits con 24 bits para el canal de profundidad y 8 bits para el canal de galería de símbolos.                                             |
| **D3DFMT \_ D24X8**          | 77    | Profundidad de bits de búfer z de 32 bits con 24 bits para el canal de profundidad.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | Profundidad de bits de búfer z de 32 bits con 24 bits para el canal de profundidad y 4 bits para el canal de galería de símbolos.                                             |
| **D3DFMT \_ D32F \_ LOCKABLE** | 82    | Formato que se puede bloquear en el que el valor de profundidad se representa como un número de punto flotante IEEE estándar.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Formato no bloqueable que contiene 24 bits de profundidad (en un formato de punto flotante de 24 bits - 20e4) y 8 bits de galería de símbolos.                        |
| **D3DFMT \_ D32 \_ LOCKABLE**  | 84    | Búfer de profundidad de 32 bits que se puede bloquear. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/>  |
| **D3DFMT \_ S8 \_ LOCKABLE**   | 85    | Búfer de galería de símbolos de 8 bits que se puede bloquear. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/> |
| **D3DFMT \_ D16**            | 80    | Profundidad de bits de búfer z de 16 bits.                                                                                                                    |
| **D3DFMT \_ VERTEXDATA**     | 100   | Describe una superficie de búfer de vértices.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | Profundidad de bits del búfer de índice de 16 bits.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | Profundidad de bits del búfer de índice de 32 bits.                                                                                                                |



 

Todos los formatos de galería de símbolos de profundidad excepto D3DFMT D16 LOCKABLE indican que no hay ninguna ordenación de bits determinada por píxel y el controlador puede consumir más que el número indicado de bits por canal de profundidad (pero no canal de galería de \_ \_ símbolos).

### <a name="dxtn-compressed-texture-formats"></a>Formatos de textura comprimida dxtn

Estas marcas se usan para texturas comprimidas:



| Marcas de textura comprimida DXTn | Value                          | Formato                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | MAKEFOURCC('D', 'X', 'T', '1') | Formato de textura de compresión DXT1 |
| **D3DFMT \_ DXT2**              | MAKEFOURCC('D', 'X', 'T', '2') | Formato de textura de compresión DXT2 |
| **D3DFMT \_ DXT3**              | MAKEFOURCC('D', 'X', 'T', '3') | Formato de textura de compresión DXT3 |
| **D3DFMT \_ DXT4**              | MAKEFOURCC('D', 'X', 'T', '4') | Formato de textura de compresión DXT4 |
| **D3DFMT \_ DXT5**              | MAKEFOURCC('D', 'X', 'T', '5') | Formato de textura de compresión DXT5 |



 

El tiempo de ejecución no permitirá que una aplicación cree una superficie con un formato DXTn a menos que las dimensiones de la superficie sean múltiplo de 4. Esto se aplica a superficies sin formato de pantalla, destinos de representación, texturas 2D, texturas de cubo y texturas de volumen.

### <a name="floating-point-formats"></a>Floating-Point formatos

Estas marcas se usan para los formatos de superficie de punto flotante. Estos formatos de 16 bits por canal también se conocen como formatos s10e5.



| Marcas de punto flotante      | Value | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | Formato float de 16 bits con 16 bits para el canal rojo.                                   |
| **D3DFMT \_ G16R16F**       | 112   | Formato float de 32 bits con 16 bits para el canal rojo y 16 bits para el canal verde. |
| **D3DFMT \_ A16B16G16R16F** | 113   | Formato float de 64 bits con 16 bits para cada canal (alfa, azul, verde, rojo).        |



 

### <a name="fourcc-formats"></a>Formatos FOURCC

Los datos en formato FOURCC son datos comprimidos.

### <a name="makefourcc"></a>MAKEFOURCC

A continuación se ofrece una macro para generar códigos de cuatro caracteres:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Estos son los formatos FOURCC definidos:



| Marcas FOURCC              | Value                          | Formato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTI2 \_ ARGB8** | MAKEFOURCC('M', 'E', 'T','1')    | Textura multielemento (no comprimida)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC('G', 'R', 'G', 'B') | Un formato RGB empaquetado de 16 bits análogo a YUY2 (Y0U0, Y1V0, Y2U2, y así sucesivamente). Requiere un par de píxeles para representar correctamente el valor de color. El primer píxel del par contiene 8 bits de verde (en los 8 bits superiores) y 8 bits de rojo (en los 8 bits inferiores). El segundo píxel contiene 8 bits de verde (en los 8 bits superiores) y 8 bits de azul (en los 8 bits inferiores). Juntos, los dos píxeles comparten los componentes rojo y azul, mientras que cada uno tiene un componente verde único (G0R0, G1B0, G2R2, y así sucesivamente). El muestreador de textura no normaliza los colores al buscar en un sombreador de píxeles. permanecen en el intervalo de 0,0f a 255,0f. Esto es así para todos los modelos de sombreador de píxeles programables. Para el sombreador de píxeles de función fija, el hardware debe normalizarse al intervalo de 0.f a 1.f y tratarlo básicamente como la textura YUY2. El hardware que expone este formato debe tener el miembro PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) establecido en un valor capaz de controlar ese intervalo. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC('R', 'G', 'B', 'G') | Un formato RGB empaquetado de 16 bits análogo a UYVY (U0Y0, V0Y1, U2Y2, y así sucesivamente). Requiere un par de píxeles para representar correctamente el valor de color. El primer píxel del par contiene 8 bits de verde (en los 8 bits inferiores) y 8 bits de rojo (en los 8 bits superiores). El segundo píxel contiene 8 bits de verde (en los 8 bits inferiores) y 8 bits de azul (en los 8 bits superiores). Juntos, los dos píxeles comparten los componentes rojo y azul, mientras que cada uno tiene un componente verde único (R0G0, B0G1, R2G2, y así sucesivamente). El muestreador de textura no normaliza los colores al buscar en un sombreador de píxeles. permanecen en el intervalo de 0,0f a 255,0f. Esto es así para todos los modelos de sombreador de píxeles programables. Para el sombreador de píxeles de función fija, el hardware debe normalizarse al intervalo de 0.f a 1.f y tratarlo básicamente como la textura YUY2. El hardware que expone este formato debe tener el miembro PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) establecido en un valor capaz de controlar ese intervalo.     |
| **D3DFMT \_ UYVY**          | MAKEFOURCC('U', 'Y', 'V', 'Y') | Formato UYVY (cumplimiento de PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ YUY2**          | MAKEFOURCC('Y', 'U', 'Y', '2') | Formato YUY2 (cumplimiento de PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>Formatos IEEE

Estas marcas se usan para los formatos de superficie de punto flotante. Estos formatos de 32 bits por canal también se conocen como formatos s23e8.



| Marcas de punto flotante      | Value | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | Formato float de 32 bits con 32 bits para el canal rojo.                                   |
| **D3DFMT \_ G32R32F**       | 115   | Formato float de 64 bits con 32 bits para el canal rojo y 32 bits para el canal verde. |
| **D3DFMT \_ A32B32G32R32F** | 116   | Formato float de 128 bits con 32 bits para cada canal (alfa, azul, verde, rojo).       |



 

### <a name="mixed-formats"></a>Formatos mixtos

Los datos en formatos mixtos pueden contener una combinación de datos sin firmar y datos firmados.



| Marcas de formato mixto      | Value | Formato                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | Formato de mapa de protuberancia de 16 bits con luminosidad con 6 bits para la luminosidad y 5 bits para v y usted. |
| **D3DFMT \_ X8L8V8U8**    | 62    | Formato de mapa de protuberancia de 32 bits con luminosidad con 8 bits para cada canal.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | Formato de mapa de protuberancia de 32 bits con 2 bits para alfa y 10 bits cada uno para w, v y usted.                |



 

### <a name="signed-formats"></a>Formatos firmados

Los datos en un formato firmado pueden ser positivos y negativos. Los formatos firmados usan combinaciones de datos (U), (V), (W) y (Q).



| Marcas de formato con firma      | Value | Formato                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | Formato de mapa de protuberancia de 16 bits con 8 bits cada uno para los datos de usted y v.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | Formato de mapa de 32 bits con 8 bits para cada canal.                                                     |
| **D3DFMT \_ V16U16**       | 64    | Formato de mapa de 32 bits con 16 bits para cada canal.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | Formato de mapa de protuberancia de 64 bits con 16 bits para cada componente.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | Formato de compresión normal de 16 bits. El muestreador de textura calcula el canal de C a partir de: C = sqrt(1 - Untes - Vntes). |



 

### <a name="unsigned-formats"></a>Formatos sin signo

Los datos en formato sin signo deben ser positivos. Los formatos sin signo usan combinaciones de datos (R)ed, (G)reen, (B)lue, (A)lpha, (L)uminance y (P)alette. Los datos de la paleta también se conocen como datos indizados de color porque los datos se usan para indexar una paleta de colores.



| Marcas de formato sin signo             | Value | Formato                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | Formato de píxel RGB de 24 bits con 8 bits por canal.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | Formato de píxel ARGB de 32 bits con alfa, con 8 bits por canal.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | Formato de píxel RGB de 32 bits, donde se reservan 8 bits para cada color.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | Formato de píxel RGB de 16 bits con 5 bits para rojo, 6 bits para verde y 5 bits para azul.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | Formato de píxel de 16 bits, donde se reservan 5 bits para cada color.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | Formato de píxel de 16 bits, donde 5 bits están reservados para cada color y 1 bit está reservado para alfa.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | Formato de píxel ARGB de 16 bits con 4 bits para cada canal.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | Formato de textura RGB de 8 bits con 3 bits para rojo, 3 bits para verde y 2 bits para azul.                                                                                     |
| **D3DFMT \_ A8**                    | 28    | Solo alfa de 8 bits.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | Formato de textura ARGB de 16 bits con 8 bits para alfa, 3 bits para rojo y verde, y 2 bits para azul.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | Formato de píxel RGB de 16 bits con 4 bits para cada color.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | Formato de píxel de 32 bits con 10 bits para cada color y 2 bits para alfa.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | Formato de píxel ARGB de 32 bits con alfa, con 8 bits por canal.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | Formato de píxel RGB de 32 bits, donde se reservan 8 bits para cada color.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | Formato de píxel de 32 bits con 16 bits cada uno para verde y rojo.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | Formato de píxel de 32 bits con 10 bits cada uno para rojo, verde y azul, y 2 bits para alfa.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | Formato de píxeles de 64 bits con 16 bits para cada componente.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | Color de 8 bits indexado con 8 bits de alfa.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | Color de 8 bits indexado.                                                                                                                                                      |
| **D3DFMT \_ L8**                    | 50    | Solo luminosidad de 8 bits.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | Solo luminosidad de 16 bits.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16 bits con 8 bits cada uno para alfa y luminosidad.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8 bits con 4 bits cada uno para alfa y luminosidad.                                                                                                                          |
| **D3DFMT \_ A1**                    | 118   | Monocromo de 1 bit. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ \_ SESGO XR** | 119   | Punto fijo sesgado de 2,8. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/>                                      |
| **D3DFMT \_ BINARYBUFFER**          | 199   | Formato binario que indica que los datos no tienen ningún tipo inherente. **Diferencias entre Direct3D 9 y Direct3D 9Ex:** Esta marca solo está disponible en Direct3D 9Ex.<br/> |



 

### <a name="other"></a>Otros

Esta marca se usa para formatos no definidos.



| Otras marcas         | Value | Formato                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ UNKNOWN** | 0     | Se desconoce el formato de superficie |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




