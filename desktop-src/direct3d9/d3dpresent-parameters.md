---
description: Describe los parámetros de presentación.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS estructura (D3D9Types. h)
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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362611"
---
# <a name="d3dpresent_parameters-structure"></a>\_Estructura de los parámetros D3DPRESENT

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



## <a name="members"></a>Miembros

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de los búferes de reserva de la nueva cadena de intercambio, en píxeles. Si **windowed** es **false** (la presentación está en pantalla completa), este valor debe ser igual al ancho de uno de los modos de presentación enumerados que se encuentran en [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Si **windowed** es **true** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área cliente de **HDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **null**).

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de los búferes de reserva de la nueva cadena de intercambio, en píxeles. Si **windowed** es **false** (la presentación está en pantalla completa), este valor debe ser igual al alto de uno de los modos de presentación enumerados que se encuentran en [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Si **windowed** es **true** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área cliente de **HDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **null**).

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

El formato del búfer de reserva. Para obtener más información acerca de los formatos, vea [D3DFORMAT](d3dformat.md). Este valor debe ser uno de los formatos de representación-destino tal y como lo valida [**CheckDeviceType**](/windows/desktop/api). Puede usar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) para obtener el formato actual.

De hecho, \_ se puede especificar D3DFMT Unknown para **BackBufferFormat** mientras está en modo de ventana. Esto indica al tiempo de ejecución que use el formato de modo de presentación actual y elimina la necesidad de llamar a [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

En el caso de las aplicaciones en ventanas, el formato del búfer de reserva ya no necesita coincidir con el formato de modo de presentación, ya que el hardware ahora puede realizar la conversión de colores (si el hardware admite la conversión de colores). El conjunto de posibles formatos de búfer de reserva está restringido, pero el tiempo de ejecución permitirá que se presente cualquier formato de búfer de reserva válido a cualquier formato de escritorio. (Existe el requisito adicional de que el dispositivo funcione en el escritorio; normalmente, los dispositivos no funcionan en los modos de 8 bits por píxel).

Las aplicaciones de pantalla completa no pueden realizar la conversión de color.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Este valor puede estar comprendido entre 0 y [D3DPRESENT \_ \_ búferes \_ ](d3dpresent-back-buffers.md) de reserva Max (o [D3DPRESENT de \_ \_ búferes de reserva \_ Max \_ ex](d3dpresent-back-buffers.md) al usar Direct3D 9Ex). Los valores 0 se tratan como 1. Si no se puede crear el número de búferes de reserva, el tiempo de ejecución producirá un error en la llamada al método y rellenará este valor con el número de búferes de reserva que se pueden crear. Como resultado, una aplicación puede llamar al método dos veces con la misma \_ estructura de parámetros D3DPRESENT y esperar que funcione la segunda vez.

El método genera un error si no se puede crear un búfer de reserva. El valor de **BackBufferCount** influye en el conjunto de efectos de intercambio permitidos. En concreto, cualquier \_ efecto de intercambio de copia de D3DSWAPEFFECT requiere que haya exactamente un búfer de reserva.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md)**

</dd> <dd>

Miembro del tipo enumerado de [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) . El valor debe ser D3DMULTISAMPLE \_ None, a menos que **SwapEffect** se haya establecido en D3DSWAPEFFECT \_ discard. El muestreo múltiple solo se admite si el efecto de intercambio es D3DSWAPEFFECT \_ discard.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nivel de calidad. El intervalo válido está comprendido entre cero y uno menos que el nivel devuelto por pQualityLevels usado por [**CheckDeviceMultiSampleType**](/windows/desktop/api). Al pasar un valor mayor, se devuelve el error D3DERR \_ INVALIDCALL. Los valores emparejados de destinos de representación o de superficies de estarcido de profundidad y [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) deben coincidir.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DSWAPEFFECT**](./d3dswapeffect.md) . El tiempo de ejecución garantizará la semántica implícita relacionada con el comportamiento de intercambio de búfer; por lo tanto, si **windowed** es **true** y **SwapEffect** se establece en D3DSWAPEFFECT \_ Flip, el tiempo de ejecución creará un búfer de reserva adicional y copiará el que se convierta en el búfer frontal en el momento de la presentación.

La \_ copia de D3DSWAPEFFECT requiere que **BackBufferCount** se establezca en 1.

D3DSWAPEFFECT \_ discard se aplicará en el tiempo de ejecución de depuración rellenando cualquier búfer con ruido una vez presentado.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D9 y Direct3D9Ex<br/> En Direct3D9Ex, \_ se agrega D3DSWAPEFFECT FLIPEX para designar cuando una aplicación está adoptando el modo flip. Es decir, Whan el marco de una aplicación se pasa en el modo de la ventana (en lugar de copiarse) al Administrador de ventanas de escritorio (DWM) para la composición. El modo Flip proporciona un ancho de banda de memoria más eficaz y permite a una aplicación aprovechar las estadísticas de presentación en pantalla completa. No cambia el comportamiento de la pantalla completa. El comportamiento del modo de volteo está disponible a partir de Windows 7.<br/> |



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Tipo: **[ **hWnd**](../winprog/windows-data-types.md)**

</dd> <dd>

La ventana dispositivo determina la ubicación y el tamaño del búfer de reserva en la pantalla. Direct3D lo usa cuando el contenido del búfer de reserva se copia en el búfer frontal durante su [**presencia**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

-   En el caso de una aplicación de pantalla completa, se trata de un identificador de la ventana superior (que es la ventana de enfoque).

    En el caso de las aplicaciones que usan varios dispositivos de pantalla completa (por ejemplo, un sistema de varios monitores), exactamente un dispositivo puede usar la ventana de enfoque como ventana del dispositivo. Todos los demás dispositivos deben tener ventanas de dispositivo únicas.

-   En el caso de una aplicación de modo de ventana, este identificador será la ventana de destino predeterminada para [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Si este identificador es **null**, se tomará la ventana de foco.

Tenga en cuenta que el tiempo de ejecución no realiza ningún intento para reflejar los cambios de usuario en el tamaño de la ventana. El búfer de reserva no se restablece implícitamente cuando se restablece esta ventana. Sin embargo, el método [**actual**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) realiza un seguimiento automático de los cambios de posición de la ventana.

</dd> <dt>

**Ventanas**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** si la aplicación se ejecuta en la ventana; **False** si la aplicación se ejecuta en pantalla completa.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Si este valor es **true**, Direct3D administrará los búferes de profundidad de la aplicación. El dispositivo creará un búfer de estarcido de profundidad cuando se cree. El búfer de estarcido de profundidad se establecerá automáticamente como el destino de representación del dispositivo. Cuando se restablece el dispositivo, el búfer de estarcido de profundidad se destruye y se vuelve a crear automáticamente con el nuevo tamaño.

Si EnableAutoDepthStencil es **true**, AutoDepthStencilFormat debe ser un formato de estarcido de profundidad válido.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) . El formato de la superficie de estarcido de profundidad automática que creará el dispositivo. Este miembro se omite a menos que **EnableAutoDepthStencil** sea **true**.

</dd> <dt>

**Marcas**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Una de las constantes de [D3DPRESENTFLAG](d3dpresentflag.md) .

</dd> <dt>

**RefreshRateInHz de pantalla completa \_**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocidad a la que el adaptador de pantalla actualiza la pantalla. El valor depende del modo en el que se ejecuta la aplicación:

-   En el modo de ventana, la frecuencia de actualización debe ser 0.
-   En el modo de pantalla completa, la frecuencia de actualización es una de las frecuencias de actualización devueltas por [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

La velocidad máxima a la que se pueden presentar los búferes de reserva de la cadena de intercambio en el búfer frontal. Para obtener una explicación detallada de los modos y los intervalos que se admiten, vea [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 
