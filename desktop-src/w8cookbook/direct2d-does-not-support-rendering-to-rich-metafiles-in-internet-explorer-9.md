---
title: Direct2D no admite la representación de metaarchivos enriquecidos en Internet Explorer 9
description: Direct2D no admite la representación de metaarchivos enriquecidos en Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314828"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D no admite la representación de metaarchivos enriquecidos en Internet Explorer 9

## <a name="platforms"></a>Plataformas

**Clientes** : Windows Vista, Windows 7, Windows 8  
**Servidores** : windows Server 2008, windows Server 2008 R2 y windows Server 2012  




## <a name="description"></a>Descripción

Debido a los cambios de representación internos en Internet Explorer 9, las API [IHTMLElementRender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) y [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) crearán ahora un metarchivo que contiene un mapa de bits único que representa el contenido web en lugar de un metarchivo enriquecido que contiene texto e información de vector. Este cambio se debía al procesamiento de la representación de GDI en Direct2D (D2D) con aceleración de hardware.

Este cambio afecta a las aplicaciones que usan estas API y se basan en la información de texto o vector del metarchivo.

## <a name="manifestation"></a>Manifestación

En función de la aplicación que se vea afectada por este cambio, los usuarios podrían ver un comportamiento erróneo o incorrecto en sus aplicaciones.

## <a name="mitigation"></a>Mitigación

Las aplicaciones que solo necesitan extraer información de texto de un documento Web (sin información de posicionamiento) pueden usar la propiedad [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) para extraer texto.

Las aplicaciones que usan IViewObject::D RAW pueden usar la [característica \_ IVIEWOBJECTDRAW \_ DMLT9 \_ con \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) la clave de control de características de GDI para revertir a la representación de GDI si el modo de documento:

-   Es menor o igual que 8
-   FCK autoriza a ese host a usar GDI
-   Y se pasa un DC de metarchivo a la API

## <a name="resources"></a>Recursos

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D RAW](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [IHTMLElement:: innerText (propiedad)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Controles de características de Internet (I.. CG](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 