---
description: Define la clase de memoria que contiene los búferes de un recurso.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumeración D3DPOOL (D3D9Types.h)
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
ms.openlocfilehash: 872a3fe7a59d19e2f84bb29112080dc72ea8aea53a1fe39d80bbeda51207ba3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911071"
---
# <a name="d3dpool-enumeration"></a>D3DPOOL (enumeración)

Define la clase de memoria que contiene los búferes de un recurso.

## <a name="syntax"></a>Syntax


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

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ PREDETERMINADO**
</dt> <dd>

Los recursos se colocan en el grupo de memoria más adecuado para el conjunto de usos solicitado para el recurso especificado. Normalmente se trata de memoria de vídeo, incluida la memoria de vídeo local y la memoria AGP. El grupo D3DPOOL DEFAULT es independiente de \_ D3DPOOL MANAGED y \_ D3DPOOL SYSTEMMEM, y especifica que el recurso se coloca en la memoria preferida para el acceso al \_ dispositivo. Tenga en cuenta que D3DPOOL DEFAULT nunca indica que \_ D3DPOOL MANAGED o \_ D3DPOOL SYSTEMMEM deben elegirse como tipo de grupo de memoria para \_ este recurso. Las texturas colocadas en el grupo D3DPOOL DEFAULT no se pueden bloquear a menos que sean texturas dinámicas o que sean formatos de controlador \_ privados, FOURCC y . Para acceder a texturas desbloqueables, debe usar funciones como [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api)e [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api). D3DPOOL \_ MANAGED es probablemente una mejor opción que D3DPOOL DEFAULT para la mayoría de las \_ aplicaciones. Tenga en cuenta que algunas texturas creadas en formatos de píxeles propietarios del controlador, desconocidos para el entorno de ejecución de Direct3D, se pueden bloquear. Tenga en cuenta también que, a diferencia de las texturas, los búferes de reserva de la cadena de intercambio, los destinos de representación, los búferes de vértices y los búferes de índice se pueden bloquear. Cuando se pierde un dispositivo, los recursos creados con D3DPOOL DEFAULT deben liberarse antes de llamar a \_ [**IDirect3DDevice9::Reset**](/windows/desktop/api). Para obtener más información, [vea Dispositivos perdidos (Direct3D 9).](lost-devices.md)

Al crear recursos con D3DPOOL DEFAULT, si ya se ha confirmado la memoria de la tarjeta de vídeo, los recursos administrados se expulsarán para liberar suficiente memoria para satisfacer \_ la solicitud.

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ ADMINISTRADO**
</dt> <dd>

Los recursos se copian automáticamente en la memoria accesible desde el dispositivo según sea necesario. Los recursos administrados están con el respaldo de la memoria del sistema y no es necesario volver a crear cuando se pierde un dispositivo. Consulte [Administración de recursos (Direct3D 9)](managing-resources.md) para obtener más información. Los recursos administrados se pueden bloquear. Solo se modifica directamente la copia de memoria del sistema. Direct3D copia los cambios en la memoria accesible para el controlador según sea necesario.



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> D3DPOOL \_ MANAGED es válido con [**IDirect3DDevice9;**](/windows/desktop/api)sin embargo, no es válido con [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**
</dt> <dd>

Los recursos se colocan en memoria que el dispositivo Direct3D no suele tener acceso. Esta asignación de memoria consume ram del sistema, pero no reduce la RAM paginable. No es necesario volver a crear estos recursos cuando se pierde un dispositivo. Los recursos de este grupo se pueden bloquear y se pueden usar como origen de una operación [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) o [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) en un recurso de memoria creado con D3DPOOL \_ DEFAULT.

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ SCRATCH**
</dt> <dd>

Los recursos se colocan en la RAM del sistema y no es necesario volver a crear cuando se pierde un dispositivo. Estos recursos no están enlazados por restricciones de formato o tamaño del dispositivo. Por este problema, el dispositivo Direct3D no puede acceder a estos recursos ni establecerse como texturas o destinos de representación. Sin embargo, estos recursos siempre se pueden crear, bloquear y copiar.

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Todos los tipos de grupo son válidos con todos los recursos, incluidos: búferes de vértices, búferes de índice, texturas y superficies.

Las tablas siguientes indican restricciones en los tipos de grupo para los destinos de representación, las galerías de símbolos de profundidad y los usos dinámicos y mipmap. Una x indica una combinación compatible; la falta de una x indica incompatibilidad.



| grupo               | D3DUSAGE \_ RENDERTARGET | D3DUSAGE \_ DEPTHSTENCIL |
|--------------------|------------------------|------------------------|
| D3DPOOL \_ PREDETERMINADO   | x                      | x                      |
| D3DPOOL \_ ADMINISTRADO   |                        |                        |
| D3DPOOL \_ SCRATCH   |                        |                        |
| D3DPOOL \_ SYSTEMMEM |                        |                        |



 



| grupo               | D3DUSAGE \_ DYNAMIC | D3DUSAGE \_ AUTOGENMIPMAP |
|--------------------|-------------------|-------------------------|
| D3DPOOL \_ PREDETERMINADO   | x                 | x                       |
| D3DPOOL \_ ADMINISTRADO   |                   | x                       |
| D3DPOOL \_ SCRATCH   |                   |                         |
| D3DPOOL \_ SYSTEMMEM | x                 |                         |



 

Para obtener más información sobre los tipos de uso, [**vea D3DUSAGE**](d3dusage.md).

Los grupos no se pueden mezclar para distintos objetos contenidos en un recurso (niveles de mip en un mapa mip) y, cuando se elige un grupo, no se puede cambiar.

Las aplicaciones deben usar D3DPOOL MANAGED para la mayoría de los recursos estáticos, ya que esto hace que la aplicación no tenga que tratar \_ con dispositivos perdidos. (El tiempo de ejecución restaura los recursos administrados). Esto es especialmente beneficioso para los sistemas de arquitectura de memoria unificada (UMA). Otros recursos dinámicos no son una buena coincidencia para D3DPOOL \_ MANAGED. De hecho, los búferes de índice y los búferes de vértice no se pueden crear mediante D3DPOOL \_ MANAGED junto con D3DUSAGE \_ DYNAMIC.

En el caso de las texturas dinámicas, a veces es conveniente usar un par de texturas de memoria de vídeo y memoria del sistema, asignando la memoria de vídeo mediante D3DPOOL DEFAULT y la memoria del sistema mediante \_ D3DPOOL \_ SYSTEMMEM. Puede bloquear y modificar los bits de la textura de memoria del sistema mediante un método de bloqueo. A continuación, puede actualizar la textura de memoria de vídeo [**mediante IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



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

 

 
