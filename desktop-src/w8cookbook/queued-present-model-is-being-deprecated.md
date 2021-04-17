---
title: El modelo de presentación en cola está en desuso
description: El modelo de presentación en cola está en desuso
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "105705067"
---
# <a name="queued-present-model-is-being-deprecated"></a>El modelo de presentación en cola está en desuso

## <a name="platforms"></a>Plataformas

**Clientes** : después de Windows 8  
**Servidores** : después de Windows Server 2012  


## <a name="description"></a>Descripción

En la versión de Windows después de Windows 8, estas API devolverán E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Además, esta API solo aceptará el valor NULL para el parámetro HWND:

-   DwmGetCompositionTimingInfo

Se dejará de admitir DwmGetCompositionTimingInfo con HWND! = NULL y se quitará la funcionalidad asociada. Si se especifica un valor distinto de NULL para HWND, esta API devolverá E \_ INVALIDARG.

También se desaconseja el uso de la API de DwmGetCompositionTimingInfo y se sugiere que los desarrolladores cambien a DXGI Flip Model y la API de DX present Statistics asociada.

## <a name="manifestation"></a>Manifestación

Las aplicaciones que usan el modelo de presentación en cola no funcionarán correctamente. La manifestación exacta depende de la aplicación determinada, pero puede variar de un tiempo de presentación incorrecto a la aplicación saliendo inesperadamente). En la práctica, no esperamos ver muchas aplicaciones (si las hay). El reproductor de media de vista usó este modelo, que no se usará en Windows 8 (y posiblemente el reproductor de Zune anterior). En este momento, no tenemos información sobre otras aplicaciones que usan realmente este modelo.

## <a name="solution"></a>Solución

Los desarrolladores deben usar el modo de presentación de flip de DXGI en lugar de presentar la cola (disponible en el tiempo de ejecución de DX9 desde Windows 7 y en los tiempos de ejecución de contenido DX10 y DX11 en Windows 8).

## <a name="tests"></a>Pruebas

Ejecute pruebas generales para asegurarse de que los componentes de Windows de la bandeja de entrada y los productos principales continúan funcionando en la siguiente versión de Windows.

 

 




