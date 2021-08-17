---
description: Describe el estado actual del clip.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Estructura D3DCLIPSTATUS9 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1820e0646d735a8e1f3817832172d11e83218bbe8748e639084c47b3f77ea5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123372"
---
# <a name="d3dclipstatus9-structure"></a>Estructura D3DCLIPSTATUS9

Describe el estado actual del clip.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ClipUnion**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Marcas de unión de recorte que describen el estado actual del clip. Este miembro puede ser una o varias de las marcas siguientes:



| Value                                                                                                                                                      | Significado                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ ALL**</dt> </dl>          | Combinación de todas las marcas de recorte.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ LEFT**</dt> </dl>       | Todos los vértices se recortan mediante el plano izquierdo del frustum de visualización.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ RIGHT**</dt> </dl>    | Todos los vértices se recortan mediante el plano derecho del frustum de visualización.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ TOP**</dt> </dl>          | Todos los vértices se recortan mediante el plano superior del frustum de visualización.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ BOTTOM**</dt> </dl> | Todos los vértices se recortan mediante el plano inferior del frustum de visualización.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ FRONT**</dt> </dl>    | Todos los vértices se recortan mediante el plano frontal del frustum de visualización.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ BACK**</dt> </dl>       | Todos los vértices se recortan mediante el plano posterior del frustum de visualización.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Planos de recorte definidos por la aplicación.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**PLANO D3DCS1 \_**</dt> </dl> | Planos de recorte definidos por la aplicación.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Planos de recorte definidos por la aplicación.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Planos de recorte definidos por la aplicación.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Planos de recorte definidos por la aplicación.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Planos de recorte definidos por la aplicación.<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Marcas de intersección de recorte que describen el estado actual del clip. Este miembro puede tomar las mismas marcas que ClipUnion.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando se habilita el recorte durante el procesamiento de vértices (por [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)u otras funciones de dibujo), Direct3D calcula un código de recorte para cada vértice. El código de recorte es una combinación de bits D3DCS. \_ \* Cuando un vértice está fuera de un plano de recorte determinado, el bit correspondiente se establece en el código de recorte. Direct3D mantiene el estado del clip mediante **D3DCLIPSTATUS9,** que tiene miembros ClipUnion y ClipIntersection. ClipUnion es un OR bit a bit de todos los códigos de recorte de vértices y ClipIntersection es un AND bit a bit de todos los códigos de recorte de vértices. Los valores iniciales son cero para ClipUnion y 0xFFFFFFFF para ClipIntersection. Cuando D3DRS \_ CLIPPING se establece en **FALSE,** ClipUnion y ClipIntersection se establecen en cero. Direct3D actualiza el estado del clip durante las llamadas de dibujo. Para calcular el estado del clip para un objeto determinado, establezca ClipUnion y ClipIntersection en su valor inicial y continúe dibujando.

[**DrawRectPatch**](/windows/desktop/api) y [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) no actualizan el estado del clip porque no hay emulación de software para ellos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
