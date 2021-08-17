---
title: Métodos opcionales
description: Métodos opcionales
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64f4b22693c77295d3a21cfb59055f9a232d08bb1426d995f710bbf24073d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130047"
---
# <a name="optional-methods"></a>Métodos opcionales

Un componente OLE puede implementar una interfaz sin implementar toda la semántica de todos los métodos de la interfaz, devolviendo E \_ NOTIMPL o S \_ OK según corresponda. En la tabla siguiente se describen los métodos que un contenedor de control ActiveX no es necesario implementar (es decir, el contenedor de controles puede devolver E \_ NOTIMPL).

En la tabla siguiente se describen los métodos opcionales; Tenga en cuenta que el método debe seguir existiendo, pero simplemente puede devolver E NOTIMPL en \_ lugar de implementar semántica real. Tenga en cuenta que cualquier método de una interfaz obligatoria que no se muestra a continuación debe considerarse obligatorio y no puede devolver E \_ NOTIMPL.

## <a name="ioleclientsite"></a>IOleClientSite



| Método                                                     | Comentarios                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Necesario para que la persistencia se pueda admite correctamente.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Solo es necesario si el contenedor admite la vinculación a controles dentro de su propio formulario o documento.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Método                                                                     | Comentarios                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Opcionales<br/>                                      |
| [**Pergamino**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Puede devolver S \_ FALSE sin ninguna acción.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Puede devolver S \_ OK sin ninguna acción.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | La desactivación es obligatoria; Deshacer es opcional. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Método                                                                          | Comentarios                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Necesario para los contenedores que admiten controles extendidos.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Necesario para los contenedores que desean incluir sus propias páginas de propiedades para controlar las propiedades de control extendidas además de las proporcionadas por un control .<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Puede devolver S \_ FALSE sin ninguna acción.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Opcionales<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (propiedades ambiente)



| Método                      | Comentarios                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Necesario para contenedores que admiten propiedades ambientales no estándar.<br/> |
| GetTypeInfo<br/>      | Necesario para contenedores que admiten propiedades ambientales no estándar.<br/> |
| GetIDsOfNames<br/>    | Necesario para contenedores que admiten propiedades ambientales no estándar.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (receptor de eventos)



| Método                      | Comentarios                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a esto.<br/> |
| GetTypeInfo<br/>      | El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a esto.<br/> |
| GetIDsOfNames<br/>    | El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a esto.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Método                                                                           | Comentarios                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Necesario para contenedores con interfaz de usuario de barra de herramientas (que es opcional)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Necesario para contenedores con interfaz de usuario de barra de herramientas (que es opcional)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Necesario para contenedores con interfaz de usuario de barra de herramientas (que es opcional)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Necesario para contenedores con interfaz de usuario de menú (que es opcional)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Necesario para contenedores con interfaz de usuario de menú (que es opcional)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Necesario para contenedores con interfaz de usuario de menú (que es opcional)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Solo es necesario para contenedores que tienen una línea de estado<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Opcionales<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Opcionales<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Método                                                                    | Comentarios                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Solo si se admite la vinculación a controles u otras inserciones en el contenedor, ya que esto es necesario para el enlace de moniker.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | En cuanto a ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Devuelve todos los ActiveX a través de un enumerador con [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), pero no necesariamente todos los objetos (porque no hay ninguna garantía de que todos los objetos son controles ActiveX; algunos pueden ser controles Windows normales).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

