---
title: Códigos de retorno de DirectDraw (Ddraw.h)
description: 'Códigos de retorno de DirectDraw: los errores se representan mediante valores negativos y no se pueden combinar.'
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e937ad9cc32a7837303d535b73b176c7e16f2d0ab0033bf625f629d2d5f7bc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504357"
---
# <a name="directdraw-return-codes"></a>Códigos de retorno de DirectDraw

Los errores se representan mediante valores negativos y no se pueden combinar. En esta tabla se enumeran los valores que pueden devolver todos los métodos de las funciones [DirectDraw Interfaces](directdraw-interfaces.md) y [DirectDraw](directdraw-functions.md). Para obtener una lista de los códigos de error que puede devolver cada método o función, vea la descripción del método o la función.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**
</dt> <dd> <dl> <dt>



La solicitud se completó correctamente.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ YA INICIALIZADO**
</dt> <dd> <dl> <dt>



El objeto ya se ha inicializado.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**
</dt> <dd> <dl> <dt>



Un objeto DirectDrawClipper se adjunta a una superficie de origen que se ha pasado a una llamada al método [**IDirectDrawSurface7::BltFast.**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast)


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**
</dt> <dd> <dl> <dt>



Una superficie no se puede adjuntar a otra superficie solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**
</dt> <dd> <dl> <dt>



Una superficie no se puede desasociar de otra superficie solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**
</dt> <dd> <dl> <dt>



Windows puede crear más contextos de dispositivo (DC) o un controlador de dominio ha solicitado una superficie indizada por paleta cuando la superficie no tenía ninguna paleta y el modo de presentación no estaba indexado por la paleta (en este caso, DirectDraw no puede seleccionar una paleta adecuada en el controlador de dominio).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**
</dt> <dd> <dl> <dt>



Las superficies principal y 3D, o las superficies que se crean implícitamente, no se pueden duplicar.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**
</dt> <dd> <dl> <dt>



Se rechaza el acceso a esta superficie porque se intentó bloquear la superficie principal sin compatibilidad con la Interfaz de control de pantalla (DCI).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**
</dt> <dd> <dl> <dt>



Error al intentar bloquear la página de una superficie. El bloqueo de página no funciona en una superficie de memoria para mostrar o en una superficie principal emulada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**
</dt> <dd> <dl> <dt>



Error al intentar desbloquear una superficie en la página. El desbloqueo de páginas no funciona en una superficie de memoria para mostrar o en una superficie principal emulada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**
</dt> <dd> <dl> <dt>



Se intentó establecer una lista de clips para un objeto DirectDrawClipper que ya está supervisando un identificador de ventana.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**
</dt> <dd> <dl> <dt>



No se especifica ninguna clave de color de origen para esta operación.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**
</dt> <dd> <dl> <dt>



Actualmente no hay soporte técnico disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**
</dt> <dd> <dl> <dt>



Novedad de DirectX 7.0. La superficie requiere la marca COMPLEX de DDSCAPS. \_


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**
</dt> <dd> <dl> <dt>



Ya se ha devuelto un contexto de dispositivo (DC) para esta superficie. Solo se puede recuperar un controlador de dominio para cada superficie.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNSURFACE**
</dt> <dd> <dl> <dt>



Las superficies creadas por un dispositivo DirectDraw no se pueden usar directamente en otro dispositivo DirectDraw.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**
</dt> <dd> <dl> <dt>



Ya se ha creado un objeto DirectDraw que representa este controlador para este proceso.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR \_ EXCEPTION**
</dt> <dd> <dl> <dt>



Se encontró una excepción al realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**
</dt> <dd> <dl> <dt>



Se intentó establecer el nivel de cooperación cuando ya estaba establecido en exclusivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ EXPIRÓ**
</dt> <dd> <dl> <dt>



Los datos han expirado y, por tanto, ya no son válidos.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ GENÉRICO**
</dt> <dd> <dl> <dt>



Hay una condición de error indefinido.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**
</dt> <dd> <dl> <dt>



El alto del rectángulo proporcionado no es un múltiplo de la alineación necesaria.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWJUNREADYSET**
</dt> <dd> <dl> <dt>



Ya se ha establecido el identificador de ventana de nivel cooperativo de DirectDraw. No se puede restablecer mientras el proceso tiene superficies o paletas creadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**
</dt> <dd> <dl> <dt>



DirectDraw no puede restaurar el estado porque el identificador de ventana de nivel cooperativo de DirectDraw se ha subclasificado.


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**
</dt> <dd> <dl> <dt>



La superficie no se puede restaurar porque es una superficie creada implícitamente.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**
</dt> <dd> <dl> <dt>



La solicitud de creación de la superficie principal no coincide con la superficie principal existente.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**INVALIDCAPS de DDERR \_**
</dt> <dd> <dl> <dt>



Uno o varios de los bits de funcionalidad pasados a la función de devolución de llamada son incorrectos.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**
</dt> <dd> <dl> <dt>



DirectDraw no admite la lista de clips proporcionada.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**
</dt> <dd> <dl> <dt>



El identificador único global (GUID) pasado a la [**función DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) no es un identificador de controlador directDraw válido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INVALIDMODE**
</dt> <dd> <dl> <dt>



DirectDraw no admite el modo solicitado.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INVALIDOBJECT**
</dt> <dd> <dl> <dt>



DirectDraw recibió un puntero que era un objeto DirectDraw no válido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**INVALIDPARAMS de DDERR \_**
</dt> <dd> <dl> <dt>



Uno o varios de los parámetros pasados al método son incorrectos.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**
</dt> <dd> <dl> <dt>



El formato de píxel no era válido según lo especificado.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**INVALIDPOSITION de DDERR \_**
</dt> <dd> <dl> <dt>



La posición de la superposición en el destino ya no es válida.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**
</dt> <dd> <dl> <dt>



El rectángulo proporcionado no era válido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**
</dt> <dd> <dl> <dt>



La secuencia especificada contiene datos no válidos.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**
</dt> <dd> <dl> <dt>



La superficie era del tipo incorrecto.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**
</dt> <dd> <dl> <dt>



Una o varias superficies están bloqueadas, lo que provoca el error de la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**
</dt> <dd> <dl> <dt>



Hay más datos disponibles de los que puede contener el tamaño de búfer especificado.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NEWMODE**
</dt> <dd> <dl> <dt>



Novedad de DirectX 7.0. Cuando se llama a [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) con la marca DDSMT ISTESTREQUIRED, podría devolver este valor para indicar que algunas o todas las resoluciones pueden y deben \_ probarse. [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) devuelve este valor para indicar que la prueba ha cambiado a un nuevo modo de presentación.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**
</dt> <dd> <dl> <dt>



No hay hardware 3D ni emulación presente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de aceleración alfa presente o disponible, lo que provoca el error de la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**
</dt> <dd> <dl> <dt>



No hay ningún bloque de bits que transfiera hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOCLIPLIST**
</dt> <dd> <dl> <dt>



No hay ninguna lista de clips disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**
</dt> <dd> <dl> <dt>



No hay ningún objeto DirectDrawClipper asociado al objeto de superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de conversión de colores presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**
</dt> <dd> <dl> <dt>



La superficie no tiene actualmente una clave de color.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**
</dt> <dd> <dl> <dt>



No hay compatibilidad de hardware con la clave de color de destino.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**
</dt> <dd> <dl> <dt>



Se llamó a una función create sin el [**método IDirectDraw7::SetCooperativeLevel.**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel)


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**
</dt> <dd> <dl> <dt>



No se ha creado ningún contexto de dispositivo (DC) para esta superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de operación de trama (ROP) de DirectDraw disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**
</dt> <dd> <dl> <dt>



No es posible crear objetos DirectDraw solo de hardware; el controlador no admite ningún hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**
</dt> <dd> <dl> <dt>



La compatibilidad con DirectDraw no es posible con el controlador de pantalla actual.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**
</dt> <dd> <dl> <dt>



Novedad de DirectX 7.0. Las pruebas no pueden continuar porque el controlador del adaptador de pantalla no enumera las tasas de actualización.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOEMULATION**
</dt> <dd> <dl> <dt>



La emulación de software no está disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOEXCLUSIVEMODE**
</dt> <dd> <dl> <dt>



La operación requiere que la aplicación tenga el modo exclusivo, pero la aplicación no tiene el modo exclusivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**
</dt> <dd> <dl> <dt>



No se admite la volteo de superficies visibles.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**
</dt> <dd> <dl> <dt>



Se intentó crear o establecer una ventana de dispositivo sin establecer primero la ventana de foco.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**
</dt> <dd> <dl> <dt>



No hay GDI presente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOHWND**
</dt> <dd> <dl> <dt>



Clipper notificación requiere un identificador de ventana o no se ha establecido previamente ningún identificador de ventana como identificador de ventana de nivel cooperativo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de asignación de textura compatible con mipmap presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de creación de reflejo presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**
</dt> <dd> <dl> <dt>



Novedad de DirectX 7.0. Las pruebas no pueden continuar porque el monitor no tiene datos EDID asociados.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**
</dt> <dd> <dl> <dt>



Se intentó asignar memoria de vídeo no local desde un dispositivo que no admite memoria de vídeo no local.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**
</dt> <dd> <dl> <dt>



El dispositivo no admite superficies optimizadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**
</dt> <dd> <dl> <dt>



Se llama al método [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) en una superposición en la que no se ha llamado al método [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) para establecer como destino.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware superpuesto presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**
</dt> <dd> <dl> <dt>



No hay ningún objeto de paleta asociado a esta superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**
</dt> <dd> <dl> <dt>



No hay compatibilidad con hardware para paletas de 16 o 256 colores.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de operación de trama adecuado presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**
</dt> <dd> <dl> <dt>



No hay ningún hardware de rotación presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**
</dt> <dd> <dl> <dt>



No hay ningún hardware estéreo presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**
</dt> <dd> <dl> <dt>



No hay compatibilidad de hardware para la extensión.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**
</dt> <dd> <dl> <dt>



No hay hardware presente que admita superficies estéreo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



El objeto DirectDrawSurface no usa una paleta de colores de 4 bits y la operación solicitada requiere una paleta de colores de 4 bits.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



El objeto DirectDrawSurface no usa una paleta de índices de color de 4 bits y la operación solicitada requiere una paleta de índices de color de 4 bits.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



El objeto DirectDrawSurface no usa una paleta de colores de 8 bits y la operación solicitada requiere una paleta de colores de 8 bits.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**
</dt> <dd> <dl> <dt>



Se llama a un componente de superposición para una superficie no superpuesta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**
</dt> <dd> <dl> <dt>



La operación no se puede llevar a cabo porque no hay ningún hardware de asignación de texturas presente o disponible.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR \_ NOTFLIPPABLE**
</dt> <dd> <dl> <dt>



Se intentó voltear una superficie que no se puede voltear.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR \_ NOTFOUND**
</dt> <dd> <dl> <dt>



No se encontró el elemento solicitado.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR \_ NOTINITIALIZED**
</dt> <dd> <dl> <dt>



Se intentó llamar a un método de interfaz de un objeto DirectDraw creado por [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) antes de inicializar el objeto.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR \_ NO CARGADO**
</dt> <dd> <dl> <dt>



La superficie es una superficie optimizada, pero aún no se le ha asignado memoria.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR \_ NOTLOCKED**
</dt> <dd> <dl> <dt>



Se intentó desbloquear una superficie que no estaba bloqueada.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**
</dt> <dd> <dl> <dt>



Se intentó desbloquear una superficie sin bloqueos de página pendientes.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**
</dt> <dd> <dl> <dt>



La superficie que se usa no es una superficie basada en paleta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**
</dt> <dd> <dl> <dt>



No hay compatibilidad de hardware para las operaciones sincronizadas verticales en blanco.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**
</dt> <dd> <dl> <dt>



La operación para crear un búfer z en la memoria para mostrar o para realizar una transferencia de bloque de bits (bitblt), mediante un búfer z no se puede llevar a cabo porque no hay compatibilidad de hardware con los búferes z.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**
</dt> <dd> <dl> <dt>



Las superficies superpuestas no se pueden superponer en capas z, en función del orden z porque el hardware no admite la ordenación z de las superposiciones.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**OUTOFCAPS de DDERR \_**
</dt> <dd> <dl> <dt>



Ya se ha asignado el hardware necesario para la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw no tiene suficiente memoria para realizar la operación.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw no tiene suficiente memoria de presentación para realizar la operación.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**
</dt> <dd> <dl> <dt>



Los rectángulos de origen y destino están en la misma superficie y se superponen entre sí.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR \_ OVERLAYCANTCLIP**
</dt> <dd> <dl> <dt>



El hardware no admite superposiciones recortadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**
</dt> <dd> <dl> <dt>



Se intentó tener más de una clave de color activa en una superposición.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR \_ OVERLAYNOTVISIBLE**
</dt> <dd> <dl> <dt>



Se llamó al método [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) en una superposición oculta.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**PALETA DE \_ DDERRBUSY**
</dt> <dd> <dl> <dt>



Se rechaza el acceso a esta paleta porque otro subproceso bloquea la paleta.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**
</dt> <dd> <dl> <dt>



Este proceso ya ha creado una superficie principal.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**REGIÓN DE \_ DDERRTOOSMALL**
</dt> <dd> <dl> <dt>



La región que se pasa [**al método IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) es demasiado pequeña.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**
</dt> <dd> <dl> <dt>



Se intentó adjuntar una superficie a otra superficie a la que ya está asociada.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**
</dt> <dd> <dl> <dt>



Se intentó convertir una superficie en una dependencia de otra superficie de la que ya depende.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**
</dt> <dd> <dl> <dt>



Se rechaza el acceso a la superficie porque otro subproceso bloquea la superficie.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**
</dt> <dd> <dl> <dt>



Se rechaza el acceso a la superficie porque la superficie está oculta.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**
</dt> <dd> <dl> <dt>



Se rechaza el acceso a la superficie porque la memoria de la superficie ha desaparecido. Llame al [**método IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) en esta superficie para restaurar la memoria asociada a él.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**
</dt> <dd> <dl> <dt>



La superficie solicitada no está adjunta.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**
</dt> <dd> <dl> <dt>



Novedad de DirectX 7.0. Cuando lo devuelve el método [**IDirectDraw7::StartModeTest,**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) este valor significa que no se puede iniciar ninguna prueba porque todas las resoluciones elegidas para las pruebas ya tienen información de frecuencia de actualización en el Registro. Cuando [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)lo devuelve, el valor significa que DirectDraw ha completado una prueba de frecuencia de actualización.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIIGHT**
</dt> <dd> <dl> <dt>



El alto solicitado por DirectDraw es demasiado grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**
</dt> <dd> <dl> <dt>



El tamaño solicitado por DirectDraw es demasiado grande. Sin embargo, el alto y el ancho individuales son tamaños válidos.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**
</dt> <dd> <dl> <dt>



El ancho solicitado por DirectDraw es demasiado grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ NO COMPATIBLE**
</dt> <dd> <dl> <dt>



La operación no es compatible.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**
</dt> <dd> <dl> <dt>



DirectDraw no admite el formato de píxel solicitado.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**
</dt> <dd> <dl> <dt>



DirectDraw no admite la máscara de bits en el formato de píxel solicitado.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ UNSUPPORTEDMODE**
</dt> <dd> <dl> <dt>



La pantalla está actualmente en un modo no admitido.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**
</dt> <dd> <dl> <dt>



Hay un espacio en blanco vertical en curso.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**VÍDEO DE \_ DDERRNOTACTIVE**
</dt> <dd> <dl> <dt>



El puerto de vídeo no está activo.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTFUNDDRAWING**
</dt> <dd> <dl> <dt>



La operación bitblt anterior que transfiere información hacia o desde esta superficie está incompleta.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ WRONGMODE**
</dt> <dd> <dl> <dt>



Esta superficie no se puede restaurar porque se creó en un modo diferente.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**
</dt> <dd> <dl> <dt>



El rectángulo proporcionado no estaba alineado horizontalmente en un límite necesario.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

