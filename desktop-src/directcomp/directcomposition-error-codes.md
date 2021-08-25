---
title: Códigos de error de DirectComposition (Dcomp.h)
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
ms.openlocfilehash: 7d86ab61574af84e0b4b51223c69b181697dc0ebbdd7995c1bff112e286cc3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891985"
---
# <a name="directcomposition-error-codes"></a>Códigos de error de DirectComposition

Si se produce un error, Microsoft DirectComposition devuelve un código como **un valor HRESULT.** En esta sección se describen los códigos de error específicos de DirectComposition. Para obtener una lista de códigos de error generales del Modelo de objetos componentes (COM), vea [Códigos de error COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION \_ ERROR \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>


</dt> <dt>



El identificador de ventana que se especificó en una llamada al método [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) pertenece a un proceso diferente del que creó el objeto de dispositivo.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA**
</dt> <dd> <dl> <dt>


</dt> <dt>



La superficie ya se estaba representando cuando la aplicación llamó al método [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)o [**IDCompositionSurface::ResumeDraw.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**NO SE REPRESENTA LA SUPERFICIE DE ERROR DE \_ \_ \_ \_ \_ DCOMPOSITION**
</dt> <dd> <dl> <dt>


</dt> <dt>



La aplicación llamó al [**método IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)o [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) para una superficie que no se está representando. Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**VENTANA DE ERROR DE DCOMPOSITION \_ \_ YA \_ \_ COMPUESTA**
</dt> <dd> <dl> <dt>


</dt> <dt>



Se llamó al método [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) con los parámetros *hwnd* y *topmost* para los que ya existe un árbol visual.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Si una llamada a [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) era la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA** |



 

Si una llamada a [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) fue la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ OK                                             |



 

Si una llamada a [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) fue la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFICIE DE ERROR DE \_ DCOMPOSITION \_ QUE SE \_ \_ REPRESENTA.** |



 

Si una llamada a [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) fue la acción más reciente:



| Llamar a este método:                                    | Devuelve este valor:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **NO SE REPRESENTA LA SUPERFICIE DE ERROR DE \_ \_ \_ \_ \_ DCOMPOSITION.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **NO SE REPRESENTA LA SUPERFICIE DE ERROR DE \_ \_ \_ \_ \_ DCOMPOSITION.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **NO SE REPRESENTA LA SUPERFICIE DE ERROR DE \_ \_ \_ \_ \_ DCOMPOSITION.** |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Dcomp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DirectComposition](reference.md)
</dt> </dl>

 

