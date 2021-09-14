---
description: Describe los parámetros de presentación.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f113b3df247765b958dfe47bb04fafb6c9a13bbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970975"
---
# <a name="d3dpresent_parameters-structure"></a>D3DPRESENT \_ PARAMETERS (estructura)

Describe los parámetros de presentación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a>Members

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de los búferes de reserva de la nueva cadena de intercambio, en píxeles. Si **Windowed** es **FALSE** (la presentación es de pantalla completa), este valor debe ser igual al ancho de uno de los modos de presentación enumerados que se encuentran a través [**de EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Si **Windowed** es **TRUE** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área cliente de **hDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **NULL).**

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de los búferes de reserva de la nueva cadena de intercambio, en píxeles. Si **Windowed** es **FALSE** (la presentación es de pantalla completa), este valor debe ser igual al alto de uno de los modos de presentación enumerados que se encuentran a través de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Si **Windowed** es **TRUE** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área cliente de **hDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **NULL).**

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato de búfer de reserva. Para obtener más información sobre los formatos, [vea D3DFORMAT](d3dformat.md). Este valor debe ser uno de los formatos de destino de representación validados [**por CheckDeviceType.**](/windows/desktop/api) Puede usar [**GetDisplayMode para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) obtener el formato actual.

De hecho, D3DFMT \_ UNKNOWN se puede especificar para **BackBufferFormat** en modo de ventana. Esto indica al tiempo de ejecución que use el formato de modo de presentación actual y elimina la necesidad de llamar a [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

En el caso de las aplicaciones con ventanas, el formato de búfer de reserva ya no necesita coincidir con el formato de modo de presentación, ya que el hardware puede realizar la conversión de color (si el hardware admite la conversión de colores). El conjunto de posibles formatos de búfer de reserva está restringido, pero el tiempo de ejecución permitirá que cualquier formato de búfer de reserva válido se presente a cualquier formato de escritorio. (Existe el requisito adicional de que el dispositivo sea operable en el escritorio; los dispositivos normalmente no funcionan en modos de 8 bits por píxel).

Las aplicaciones de pantalla completa no pueden realizar la conversión de colores.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Este valor puede estar entre 0 y [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (o [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) cuando se usa Direct3D 9Ex). Los valores de 0 se tratan como 1. Si no se puede crear el número de búferes de reserva, el tiempo de ejecución producirá un error en la llamada al método y rellenará este valor con el número de búferes de reserva que se podrían crear. Como resultado, una aplicación puede llamar al método dos veces con la misma estructura D3DPRESENT PARAMETERS y esperar que funcione \_ la segunda vez.

Se produce un error en el método si no se puede crear un búfer de reserva. El valor de **BackBufferCount influye** en qué conjunto de efectos de intercambio se permiten. En concreto, cualquier efecto de intercambio COPY de D3DSWAPEFFECT \_ requiere que haya exactamente un búfer de reserva.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**

</dd> <dd>

Miembro del [**tipo enumerado D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md) El valor debe ser D3DMULTISAMPLE NONE a menos que SwapEffect se haya establecido \_ en D3DSWAPEFFECT  \_ DISCARD. Solo se admite la multimuestreo si el efecto de intercambio es D3DSWAPEFFECT \_ DISCARD.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nivel de calidad. El intervalo válido está entre cero y uno menos que el nivel devuelto por pQualityLevels usado por [**CheckDeviceMultiSampleType.**](/windows/desktop/api) Al pasar un valor mayor, se devuelve el error D3DERR \_ INVALIDCALL. Los valores emparejados de destinos de representación o de superficies de galería de símbolos de profundidad y [**D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md) deben coincidir.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Miembro del [**tipo enumerado D3DSWAPEFFECT.**](./d3dswapeffect.md) El tiempo de ejecución garantizará la semántica implícita relativa al comportamiento de intercambio de búfer; Por lo tanto, si **Windowed** es **TRUE** y **SwapEffect** se establece en D3DSWAPEFFECT FLIP, el tiempo de ejecución creará un búfer de reserva adicional y copiará lo que se convierta en el búfer front-time en el momento de la \_ presentación.

D3DSWAPEFFECT \_ COPY requiere que **BackBufferCount** se establezca en 1.

D3DSWAPEFFECT DISCARD se aplicará en el tiempo de ejecución de depuración rellenando cualquier búfer con \_ ruido después de que se presente.

Diferencias entre Direct3D9 y Direct3D9Ex:

- En Direct3D9Ex, D3DSWAPEFFECT FLIPEX se agrega para designar cuándo una aplicación \_ adopta el modo de volteo. Es decir, el marco de una aplicación se pasa en modo de ventana (en lugar de copiarse) al Administrador de ventanas de escritorio(DWM) para la composición. El modo de volteo proporciona un ancho de banda de memoria más eficaz y permite que una aplicación aproveche las estadísticas de pantalla completa presentes. No cambia el comportamiento de pantalla completa. El comportamiento del modo de volteo está disponible a partir Windows 7.



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

La ventana del dispositivo determina la ubicación y el tamaño del búfer de reserva en la pantalla. Direct3D lo usa cuando el contenido del búfer de reserva se copia en el búfer front-buffer durante [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

-   Para una aplicación de pantalla completa, se trata de un identificador de la ventana superior (que es la ventana de foco).

    En el caso de las aplicaciones que usan varios dispositivos de pantalla completa (por ejemplo, un sistema multimonitor), exactamente un dispositivo puede usar la ventana de foco como ventana del dispositivo. Todos los demás dispositivos deben tener ventanas de dispositivo únicas.

-   Para una aplicación en modo de ventana, este identificador será la ventana de destino predeterminada para [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Si este identificador es **NULL,** se toma la ventana de foco.

Tenga en cuenta que el tiempo de ejecución no intenta reflejar los cambios del usuario en el tamaño de la ventana. El búfer de reserva no se restablece implícitamente cuando se restablece esta ventana. Sin embargo, [**el método Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) realiza un seguimiento automático de los cambios de posición de la ventana.

</dd> <dt>

**Ventana**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE** si la aplicación se ejecuta en ventanas; **FALSE** si la aplicación se ejecuta a pantalla completa.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Si este valor es **TRUE,** Direct3D administrará los búferes de profundidad para la aplicación. El dispositivo creará un búfer de galería de símbolos de profundidad cuando se cree. El búfer de galería de símbolos de profundidad se establecerá automáticamente como destino de representación del dispositivo. Cuando se restablece el dispositivo, el búfer de galería de símbolos de profundidad se destruirá automáticamente y se volverá a crear con el nuevo tamaño.

Si EnableAutoDepthStencil es **TRUE,** AutoDepthStencilFormat debe ser un formato válido de galería de símbolos de profundidad.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del [tipo enumerado D3DFORMAT.](d3dformat.md) Formato de la superficie de galería de símbolos de profundidad automática que creará el dispositivo. Este miembro se omite a menos **que EnableAutoDepthStencil** sea **TRUE.**

</dd> <dt>

**Marcas**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Una de las [constantes D3DPRESENTFLAG.](d3dpresentflag.md)

</dd> <dt>

**FullScreen \_ RefreshRateInHz**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocidad a la que el adaptador de pantalla actualiza la pantalla. El valor depende del modo en el que se ejecuta la aplicación:

-   Para el modo de ventana, la frecuencia de actualización debe ser 0.
-   Para el modo de pantalla completa, la frecuencia de actualización es una de las tasas de actualización devueltas por [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocidad máxima a la que se pueden presentar los búferes de reserva de la cadena de intercambio al búfer front-buffer. Para obtener una explicación detallada de los modos y los intervalos admitidos, vea [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
