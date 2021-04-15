---
title: Interfaces de controles ActiveX
description: Interfaces de controles ActiveX
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695264"
---
# <a name="activex-controls-interfaces"></a><span data-ttu-id="2eb06-103">Interfaces de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="2eb06-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="2eb06-104">Además de otros mecanismos para la comunicación entre el control y su cliente, la tecnología de controles ActiveX especifica las interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) y [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) para la comunicación de control de cliente.</span><span class="sxs-lookup"><span data-stu-id="2eb06-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="2eb06-105">También hay la interfaz [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para los contenedores de control simples.</span><span class="sxs-lookup"><span data-stu-id="2eb06-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="2eb06-106">Sin embargo, estas tres interfaces son específicas de los controles y no suelen ser útiles fuera del contexto de los controles.</span><span class="sxs-lookup"><span data-stu-id="2eb06-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="2eb06-107">Estas interfaces se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2eb06-107">These interfaces are defined as follows.</span></span>

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

<span data-ttu-id="2eb06-108">Algunos controles, como un cuadro de grupo, son simplemente un contenedor simple de otros controles.</span><span class="sxs-lookup"><span data-stu-id="2eb06-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="2eb06-109">En tales casos, el control simple, denominado fotograma simple, no tiene que implementar todos los requisitos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="2eb06-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="2eb06-110">Puede delegar la mayoría de las llamadas de interfaz de sus controles contenidos en el contenedor que administra el marco simple.</span><span class="sxs-lookup"><span data-stu-id="2eb06-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="2eb06-111">Además de las llamadas a la interfaz, el marco sencillo también tiene que tratar los mensajes de Windows que pueden provienen de los controles que contiene.</span><span class="sxs-lookup"><span data-stu-id="2eb06-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="2eb06-112">Por esta razón, un contenedor proporciona [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para permitir que estos controles de marco sencillos pasen los mensajes al contenedor.</span><span class="sxs-lookup"><span data-stu-id="2eb06-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="2eb06-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) procesa el mensaje en primer lugar; Se llama a [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) después de que el marco simple haya procesado el propio mensaje.</span><span class="sxs-lookup"><span data-stu-id="2eb06-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2eb06-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2eb06-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb06-115">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="2eb06-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




