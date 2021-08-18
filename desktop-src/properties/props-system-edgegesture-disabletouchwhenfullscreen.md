---
description: Evita los comportamientos de gestos perimetrales cuando una ventana de aplicación está activa y en modo de pantalla completa (o una ventana de propiedad está activa).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System.EdgeGesture.DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13132ba30fd3f1e594ec54966dfe2268ce66d570b66ca6d34b1c63b03bfc0c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845125"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System.EdgeGesture.DisableTouchWhenFullscreen

Evita los comportamientos de gestos perimetrales cuando una ventana de aplicación está activa y en modo de pantalla completa (o una ventana de propiedad está activa).

> [!Note]  
> En el modo de pantalla completa, el tamaño de la ventana de la aplicación coincide con la resolución de pantalla.

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8

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

## <a name="remarks"></a>Comentarios

En Windows 8, las interacciones del usuario con los bordes de la pantalla muestran la interfaz de usuario del sistema, como barras de aplicaciones, accesos y aplicaciones en ejecución.

En el caso de las aplicaciones remotas a pantalla completa, este comportamiento de la interfaz de usuario en el equipo local podría invalidar e interferir con la interfaz de usuario de la sesión remota. Esta propiedad permite que una aplicación deshabilite la interfaz de usuario perimetral en el equipo local.

Para deshabilitar la interfaz de usuario perimetral, establezca esta propiedad en VARIANT \_ TRUE. El valor predeterminado es VARIANT \_ FALSE.

Esta propiedad no tiene ningún efecto en las Windows Store.

En el ejemplo siguiente se muestra cómo establecer comportamientos de interfaz de usuario perimetral.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
