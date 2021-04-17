---
description: Evita comportamientos de gestos perimetrales cuando una ventana de la aplicación está activa y en modo de pantalla completa (o una ventana propiedad está activa).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659968"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="e6d22-103">System. EdgeGesture. DisableTouchWhenFullscreen</span><span class="sxs-lookup"><span data-stu-id="e6d22-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="e6d22-104">Evita comportamientos de gestos perimetrales cuando una ventana de la aplicación está activa y en modo de pantalla completa (o una ventana propiedad está activa).</span><span class="sxs-lookup"><span data-stu-id="e6d22-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="e6d22-105">En el modo de pantalla completa, el tamaño de la ventana de la aplicación coincide con la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e6d22-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="e6d22-106">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6d22-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="e6d22-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6d22-107">Remarks</span></span>

<span data-ttu-id="e6d22-108">En Windows 8, las interacciones de los usuarios con los bordes de la pantalla muestran la interfaz de usuario del sistema, como las barras de la aplicación, los accesos y las aplicaciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="e6d22-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="e6d22-109">En el caso de las aplicaciones remotas de pantalla completa, este comportamiento de la interfaz de usuario en el equipo local podría invalidar e interferir con la interfaz de usuario de la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="e6d22-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="e6d22-110">Esta propiedad permite a una aplicación deshabilitar la interfaz de usuario perimetral en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="e6d22-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="e6d22-111">Para deshabilitar la interfaz de usuario perimetral, establezca esta propiedad en VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="e6d22-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="e6d22-112">El valor predeterminado es VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="e6d22-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="e6d22-113">Esta propiedad no tiene ningún efecto en las aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="e6d22-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="e6d22-114">En el ejemplo siguiente se muestra cómo establecer los comportamientos de la interfaz de usuario perimetral.</span><span class="sxs-lookup"><span data-stu-id="e6d22-114">The following example shows how to set edge UI behaviors.</span></span>


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a><span data-ttu-id="e6d22-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6d22-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6d22-116">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e6d22-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e6d22-117">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e6d22-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e6d22-118">Requerida</span><span class="sxs-lookup"><span data-stu-id="e6d22-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
