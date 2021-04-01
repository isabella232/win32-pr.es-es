---
title: Códigos de error de DirectComposition (Dcomp. h)
description: En esta sección se describen los códigos de error específicos de DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150690"
---
# <a name="directcomposition-error-codes"></a>Códigos de error de DirectComposition

Si se produce un error, Microsoft DirectComposition devuelve un código como un valor **HRESULT** . En esta sección se describen los códigos de error específicos de DirectComposition. Para obtener una lista de los códigos de error del modelo de objetos componentes (COM) generales, vea [códigos de error com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**ERROR de DCOMPOSITION \_ \_ acceso \_ denegado**
</dt> <dd> <dl> <dt>


</dt> <dt>



El identificador de ventana que se especificó en una llamada al método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) pertenece a un proceso diferente del que creó el objeto de dispositivo.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**
</dt> <dd> <dl> <dt>


</dt> <dt>



La superficie ya se estaba representando cuando la aplicación llamó al método [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)o [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) . Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa**
</dt> <dd> <dl> <dt>


</dt> <dt>



La aplicación llamó al método [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)o [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) para una superficie que no se está representando. Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**la \_ ventana de error DCOMPOSITION \_ \_ ya está \_ compuesta**
</dt> <dd> <dl> <dt>


</dt> <dt>



Se llamó al método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) con *hWnd* y los parámetros de *nivel superior* para los que ya existe un árbol visual.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Si una llamada a [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) era la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ correcto                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ correcto                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando** |



 

Si una llamada a [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) era la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ correcto                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ correcto                                             |



 

Si una llamada a [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) era la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_superficie de error DCOMPOSITION \_ \_ que se está \_ representando**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ correcto                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ correcto                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_superficie de error DCOMPOSITION \_ \_ que se va a \_ representar.** |



 

Si una llamada a [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) era la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ correcto                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **la \_ superficie de error DCOMPOSITION \_ \_ no \_ se \_ representa.** |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Dcomp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DirectComposition](reference.md)
</dt> </dl>

 

