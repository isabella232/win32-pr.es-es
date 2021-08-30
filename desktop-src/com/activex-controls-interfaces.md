---
title: ActiveX Interfaces de controles
description: ActiveX Interfaces de controles
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4d56bd5dbd4feb22341850189132d011bcf160421d9ef26904a3d147166b75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120555"
---
# <a name="activex-controls-interfaces"></a>ActiveX Interfaces de controles

Además de otros mecanismos para la comunicación entre el control y su cliente, la tecnología de controles ActiveX especifica las interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) e [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) para la comunicación de control de cliente. También está la interfaz [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para contenedores de control simples.

Sin embargo, estas tres interfaces son específicas de los controles y no suelen ser útiles fuera del contexto de los controles. Estas interfaces se definen de la manera siguiente.

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

Algunos controles, como un cuadro de grupo, son simplemente un contenedor simple de otros controles. En tales casos, el control simple, denominado marco simple, no tiene que implementar todos los requisitos del contenedor. Puede delegar la mayoría de las llamadas de interfaz de sus controles contenidos en el contenedor que administra el marco simple. Además de las llamadas de interfaz, el marco simple también tiene que tratar con Windows mensajes que potencialmente proceden de controles dentro de él. Por este motivo, un contenedor proporciona [**ISimpleFrameSite para**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) permitir que estos controles de marco simples pasen mensajes al contenedor. [**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) procesa primero el mensaje; [**Se llama a PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) después de que el marco simple haya procesado el propio mensaje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




