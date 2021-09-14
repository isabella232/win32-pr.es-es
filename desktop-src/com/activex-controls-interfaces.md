---
title: ActiveX Interfaces de controles
description: ActiveX Interfaces de controles
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264628"
---
# <a name="activex-controls-interfaces"></a>ActiveX Interfaces de controles

Además de otros mecanismos para comunicarse entre el control y su cliente, la tecnología de controles ActiveX especifica las interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) e [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) para la comunicación de control de cliente. También hay la interfaz [**ISimpleFrameSite para**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) contenedores de control simples.

Sin embargo, estas tres interfaces son específicas de los controles y no suelen ser útiles fuera del contexto de los controles. Estas interfaces se definen de la siguiente manera.

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

Algunos controles, como un cuadro de grupo, son simplemente un contenedor simple de otros controles. En tales casos, el control simple, denominado marco simple, no tiene que implementar todos los requisitos del contenedor. Puede delegar la mayoría de las llamadas de interfaz de sus controles contenidos en el contenedor que administra el marco simple. Además de las llamadas de interfaz, el marco simple también tiene que tratar Windows mensajes que posiblemente proceden de controles dentro de él. Por esta razón, un contenedor proporciona [**ISimpleFrameSite para**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) permitir que estos controles de marco simples pasen mensajes al contenedor. [**PreMessageFilter procesa**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) primero el mensaje; [**Se llama a PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) después de que el marco simple haya procesado el propio mensaje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




