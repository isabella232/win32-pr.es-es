---
description: Define la clase de memoria que contiene los búferes de un recurso.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumeración D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649417"
---
# <a name="d3dpool-enumeration"></a>Enumeración D3DPOOL

Define la clase de memoria que contiene los búferes de un recurso.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**\_Valor predeterminado de D3DPOOL**
</dt> <dd>

Los recursos se colocan en el bloque de memoria más adecuado para el conjunto de usos solicitado para el recurso especificado. Suele ser la memoria de vídeo, incluida la memoria de vídeo local y la memoria AGP. El \_ grupo predeterminado D3DPOOL es independiente de D3DPOOL \_ Managed y D3DPOOL \_ SYSTEMMEM, y especifica que el recurso se coloca en la memoria preferida para el acceso al dispositivo. Tenga en cuenta que el \_ valor predeterminado de D3DPOOL nunca indica que D3DPOOL \_ administrado o D3DPOOL \_ SYSTEMMEM debe elegirse como el tipo de bloque de memoria para este recurso. Las texturas colocadas en el \_ grupo predeterminado D3DPOOL no se pueden bloquear a menos que sean texturas dinámicas o son formatos de controlador privados, FourCC. Para acceder a las texturas de unlockable, debe usar funciones como [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api)y [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api). \_La administración de D3DPOOL es probablemente una opción mejor que D3DPOOL \_ predeterminada para la mayoría de las aplicaciones. Tenga en cuenta que algunas texturas creadas en formatos de píxeles de propietario del controlador, desconocidos para el tiempo de ejecución de Direct3D, se pueden bloquear. Tenga en cuenta también que, a diferencia de las texturas, los búferes de intercambio de cadena, los destinos de representación, los búferes de vértices y los búferes de índice se pueden bloquear. Cuando se pierde un dispositivo, los recursos creados con D3DPOOL \_ default se deben liberar antes de llamar a [**IDirect3DDevice9:: RESET**](/windows/desktop/api). Para obtener más información, vea [dispositivos perdidos (Direct3D 9)](lost-devices.md).

Al crear recursos con el \_ valor predeterminado de D3DPOOL, si ya se ha confirmado la memoria de la tarjeta de vídeo, los recursos administrados se expulsarán para liberar suficiente memoria para satisfacer la solicitud.

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**Administrado por D3DPOOL \_**
</dt> <dd>

Los recursos se copian automáticamente en la memoria accesible para el dispositivo según sea necesario. Los recursos administrados están respaldados por la memoria del sistema y no es necesario volver a crearlos cuando se pierde un dispositivo. Consulte [Administración de recursos (Direct3D 9)](managing-resources.md) para obtener más información. Se pueden bloquear los recursos administrados. Solo se modifica directamente la copia de la memoria del sistema. Direct3D copia los cambios en la memoria accesible desde el controlador según sea necesario.



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> D3DPOOL \_ Managed es válido con [**IDirect3DDevice9**](/windows/desktop/api); sin embargo, no es válido con [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**
</dt> <dd>

Los recursos se colocan en memoria que normalmente no es accesible para el dispositivo Direct3D. Esta asignación de memoria consume RAM del sistema pero no reduce la memoria RAM paginable. No es necesario volver a crear estos recursos cuando se pierde un dispositivo. Los recursos de este grupo se pueden bloquear y se pueden usar como origen de una operación [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api) o [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) en un recurso de memoria creado con D3DPOOL \_ default.

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ Scratch**
</dt> <dd>

Los recursos se colocan en la RAM del sistema y no es necesario volver a crearlos cuando se pierde un dispositivo. Estos recursos no están limitados por el tamaño del dispositivo o las restricciones de formato. Por este motivo, no se puede tener acceso a estos recursos mediante el dispositivo Direct3D ni establecerse como texturas o destinos de representación. Sin embargo, estos recursos siempre se pueden crear, bloquear y copiar.

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todos los tipos de grupo son válidos con todos los recursos, incluidos: búferes de vértices, búferes de índice, texturas y superficies.

En las tablas siguientes se indican las restricciones en los tipos de grupo para destinos de representación, galerías de símbolos de profundidad y usos dinámicos y de mipmap. Una x indica una combinación compatible; la falta de una x indica una incompatibilidad.



| grupo               | D3DUSAGE \_ RENDERTARGET | D3DUSAGE \_ DEPTHSTENCIL |
|--------------------|------------------------|------------------------|
| \_Valor predeterminado de D3DPOOL   | x                      | x                      |
| Administrado por D3DPOOL \_   |                        |                        |
| D3DPOOL \_ Scratch   |                        |                        |
| D3DPOOL \_ SYSTEMMEM |                        |                        |



 



| grupo               | D3DUSAGE \_ dinámico | D3DUSAGE \_ AUTOGENMIPMAP |
|--------------------|-------------------|-------------------------|
| \_Valor predeterminado de D3DPOOL   | x                 | x                       |
| Administrado por D3DPOOL \_   |                   | x                       |
| D3DPOOL \_ Scratch   |                   |                         |
| D3DPOOL \_ SYSTEMMEM | x                 |                         |



 

Para obtener más información sobre los tipos de uso, vea [**D3DUSAGE**](d3dusage.md).

Los grupos no se pueden mezclar para los distintos objetos contenidos en un recurso (niveles MIP en un mipmap) y, cuando se elige un grupo, no se puede cambiar.

Las aplicaciones deben usar D3DPOOL \_ administradas para la mayoría de los recursos estáticos, ya que esto evita que la aplicación tenga que tratar con los dispositivos perdidos. (El tiempo de ejecución restaura los recursos administrados). Esto es especialmente útil para los sistemas de arquitectura de memoria unificada (UMA). Otros recursos dinámicos no son una buena coincidencia para D3DPOOL \_ administrado. De hecho, los búferes de índice y los búferes de vértices no se pueden crear con D3DPOOL \_ administrados junto con D3DUSAGE \_ Dynamic.

En el caso de las texturas dinámicas, a veces es conveniente usar un par de texturas de memoria de vídeo y de memoria del sistema, asignando la memoria de vídeo mediante D3DPOOL \_ default y la memoria del sistema mediante D3DPOOL \_ SYSTEMMEM. Puede bloquear y modificar los bits de la textura de memoria del sistema mediante un método de bloqueo. Después, puede actualizar la textura de memoria de vídeo mediante [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DUSAGE**](d3dusage.md)
</dt> <dt>

[**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md)
</dt> <dt>

[**D3DSURFACE \_ DESC**](d3dsurface-desc.md)
</dt> <dt>

[**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md)
</dt> <dt>

[**D3DVOLUME \_ DESC**](d3dvolume-desc.md)
</dt> </dl>

 

 
