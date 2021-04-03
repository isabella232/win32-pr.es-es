---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Introducción a los gráficos de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082736"
---
# <a name="getting-started-with-directx-graphics"></a>Introducción a los gráficos de DirectX

Microsoft DirectX Graphics proporciona un conjunto de API que puede usar para crear juegos y otras aplicaciones multimedia de alto rendimiento. DirectX Graphics incluye compatibilidad con gráficos 2D y 3D de alto rendimiento.

En el caso de los gráficos 3D, use la API de Microsoft Direct3D 11. Aunque tenga hardware de nivel de Microsoft Direct3D 9 o Microsoft Direct3D 10, puede usar la API de Direct3D 11 y tener como [destino un](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) dispositivo de nivel de \_ característica 9 x o 10 x de nivel de características \_ . Para obtener información sobre cómo desarrollar gráficos 3D con DirectX, vea [crear gráficos 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

En el caso de texto y gráficos 2D, use Direct2D y [DirectWrite](./directwrite/direct-write-portal.md) en lugar de Windows interfaz de dispositivo gráfico (GDI).

Para crear mapas de bits rellenados por Direct3D 11 o Direct2D, use [DirectComposition](./directcomp/directcomposition-portal.md).

Para obtener información sobre cómo crear una aplicación de la tienda Windows que use DirectX, consulte [crear la primera aplicación de la tienda Windows con DirectX](/previous-versions/windows/apps/br229580(v=win.10)
). Puede usar la clase [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) para crear aplicaciones de DirectX de alto rendimiento con una superposición de la interfaz de usuario XAML. Para obtener más información sobre la combinación de XAML y DirectX en una aplicación de Windows, consulte [interoperabilidad de DirectX y XAML](/previous-versions/windows/apps/hh825871(v=win.10)).

Para obtener información sobre cómo crear un controlador de pantalla para Windows 8, consulte [el mapa de ruta del modelo de controladores de pantalla de Windows (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Si necesita la documentación de las versiones anteriores de DirectX, consulte [gráficos clásicos de DirectX](/windows/desktop/classic-directx-graphics).


 

 
