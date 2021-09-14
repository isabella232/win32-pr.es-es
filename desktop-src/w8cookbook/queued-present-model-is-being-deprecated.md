---
title: El modelo actual en cola está en desuso
description: El modelo actual en cola está en desuso
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360633"
---
# <a name="queued-present-model-is-being-deprecated"></a>El modelo actual en cola está en desuso

## <a name="platforms"></a>Plataformas

**Clientes:** después de Windows 8  
**Servidores:** después de Windows Server 2012  


## <a name="description"></a>Descripción

En la Windows versión posterior a Windows 8, estas API devolverán E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Además, esta API solo aceptará el valor NULL para el parámetro hwnd:

-   DwmGetCompositionTimingInfo

Dejaremos de admitir DwmGetCompositionTimingInfo con hwnd != NULL y quitaremos la funcionalidad asociada. Si se especifica un valor distinto de NULL para hwnd, esta API devolverá E \_ INVALIDARG.

También se desaconseja el uso de la API DwmGetCompositionTimingInfo y se recomienda que los desarrolladores cambien al modelo de volteo DXGI y la API de estadísticas de DX asociada presente.

## <a name="manifestation"></a>Manifestación

Las aplicaciones que usan el modelo presente en cola no funcionarán correctamente. La expresión exacta depende de la aplicación en particular, pero puede abarcar desde un tiempo de presentación incorrecto hasta la salida inesperada de la aplicación. En la práctica, no esperamos ver muchas (si existen) estas aplicaciones. Este modelo lo usó el Reproductor de Vista Media, que no se usará en Windows 8 (y posiblemente en el reproductor Zune anterior). En este momento no tenemos información sobre ninguna otra aplicación que use realmente este modelo.

## <a name="solution"></a>Solución

Los desarrolladores deben usar el modo de presentación de volteo DXGI en lugar de los presentes en cola (disponibles en el entorno de ejecución DX9 desde Windows 7 y en los entornos de ejecución DX10 y DX11 en Windows 8).

## <a name="tests"></a>Pruebas

Ejecute pruebas generales para asegurarse de que los componentes de Windows y los productos principales siguen funcionando en la siguiente versión de Windows.

 

 




