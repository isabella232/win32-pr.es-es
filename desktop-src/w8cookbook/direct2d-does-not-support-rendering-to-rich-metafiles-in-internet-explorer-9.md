---
title: Direct2D no admite la representación en metarchivos enriquecidos en Internet Explorer 9
description: Direct2D no admite la representación en metarchivos enriquecidos en Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebe10310202385fa4e9458cb1a442cbf98a3f6f178331d888c096449631ca61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057355"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D no admite la representación en metarchivos enriquecidos en Internet Explorer 9

## <a name="platforms"></a>Plataformas

**Clientes:** Windows Vista, Windows 7, Windows 8  
**Servidores:** Windows Server 2008, Windows Server 2008 R2, Windows Server 2012  




## <a name="description"></a>Descripción

Debido a los cambios de representación internos en Internet Explorer 9, las API [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D raw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) ahora crean un metarchivo que contiene un único mapa de bits que representa el contenido web en lugar de un metarchivo enriquecido que contiene información de texto e vector. Este cambio se debe al cambio de la representación de GDI a la representación de Direct2D (D2D) acelerada por hardware.

Este cambio afecta a las aplicaciones que usan estas API y se basan en información de texto o vector en el metarchivo.

## <a name="manifestation"></a>Manifestación

Dependiendo de la aplicación que se vea afectada por este cambio, es posible que los usuarios vean un comportamiento incorrecto o roto en sus aplicaciones.

## <a name="mitigation"></a>Mitigación

Las aplicaciones que solo necesitan extraer información de texto de un documento web (sin información de posición) pueden usar la [propiedad innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) para extraer texto.

Las aplicaciones que usan IViewObject::D raw pueden usar la clave de control de características [FEATURE \_ IVIEWOBJECTDRAW \_ DMLT9 \_ WITH GDI \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) para revertir a la representación de GDI si el modo de documento:

-   Es menor o igual que 8
-   La FCK autoriza a ese host a usar GDI
-   Y se pasa un controlador de dominio de metarchivo a la API

## <a name="resources"></a>Recursos

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D raw](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [IHTMLElement::innerText (Propiedad)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Controles de características de Internet (es decir, L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 