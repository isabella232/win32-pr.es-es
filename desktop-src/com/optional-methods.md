---
title: Métodos opcionales
description: Métodos opcionales
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149644"
---
# <a name="optional-methods"></a>Métodos opcionales

Un componente OLE puede implementar una interfaz sin implementar toda la semántica de cada método en la interfaz, en lugar de devolver E \_ NOTIMPL o S \_ correctos según corresponda. En la tabla siguiente se describen los métodos que no es necesario que implemente un contenedor de controles ActiveX (es decir, el contenedor de control puede devolver E \_ NOTIMPL).

En la tabla siguiente se describen los métodos opcionales; Tenga en cuenta que el método todavía debe existir, pero simplemente puede devolver E \_ NOTIMPL en lugar de implementar semántica real. Tenga en cuenta que los métodos de una interfaz obligatoria que no se enumeran a continuación deben considerarse obligatorios y no pueden devolver E \_ NOTIMPL.

## <a name="ioleclientsite"></a>IOleClientSite



| Método                                                     | Comentarios                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Necesario para que la persistencia se admita correctamente.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Solo es necesario si el contenedor admite la vinculación a controles dentro de su propio formulario o documento.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Método                                                                     | Comentarios                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Opcionales<br/>                                      |
| [**Scroll**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Puede devolver S \_ false sin ninguna acción.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Puede devolver S \_ OK sin ninguna acción.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | La desactivación es obligatoria; Undo es opcional. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Método                                                                          | Comentarios                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Necesario para los contenedores que admiten controles extendidos.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Necesario para los contenedores que desean incluir sus propias páginas de propiedades para controlar las propiedades de control extendidas además de las proporcionadas por un control.<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Puede devolver S \_ false sin ninguna acción.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Opcionales<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (propiedades de ambiente)



| Método                      | Comentarios                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Necesario para los contenedores que admiten propiedades de ambiente no estándar.<br/> |
| GetTypeInfo<br/>      | Necesario para los contenedores que admiten propiedades de ambiente no estándar.<br/> |
| GetIDsOfNames<br/>    | Necesario para los contenedores que admiten propiedades de ambiente no estándar.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (receptor de eventos)



| Método                      | Comentarios                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a.<br/> |
| GetTypeInfo<br/>      | El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a.<br/> |
| GetIDsOfNames<br/>    | El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Método                                                                           | Comentarios                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Necesario para contenedores con la interfaz de usuario de la barra de herramientas (que es opcional)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Necesario para contenedores con la interfaz de usuario de la barra de herramientas (que es opcional)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Necesario para contenedores con la interfaz de usuario de la barra de herramientas (que es opcional)<br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Necesario para contenedores con la interfaz de usuario de menú (que es opcional)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Necesario para contenedores con la interfaz de usuario de menú (que es opcional)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Necesario para contenedores con la interfaz de usuario de menú (que es opcional)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Solo es necesario para los contenedores que tienen una línea de estado<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Opcionales<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Opcionales<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Método                                                                    | Comentarios                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Solo si se admite la vinculación a controles u otras inserciones en el contenedor, ya que esto es necesario para el enlace de moniker.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Como para ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Devuelve todos los controles ActiveX a través de un enumerador con [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), pero no necesariamente todos los objetos (porque no hay ninguna garantía de que todos los objetos sean controles ActiveX; algunos pueden ser controles normales de Windows).<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

