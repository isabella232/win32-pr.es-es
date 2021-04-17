---
description: Esta sección contiene información sobre las funciones proporcionadas por DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funciones de DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536808"
---
# <a name="dxgi-functions"></a>Funciones de DXGI

Esta sección contiene información sobre las funciones proporcionadas por DXGI.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Crea un generador de DXGI 1,0 que puede usar para generar otros objetos de DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Crea un generador de DXGI 1,1 que puede usar para generar otros objetos de DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Crea un generador de DXGI 1,3 que puede usar para generar otros objetos de DXGI.<br/> En Windows 8, cualquier fábrica de DXGI creada mientras DXGIDebug.dll estaba presente en el sistema la cargaría y la usaría. A partir de Windows 8.1, las aplicaciones solicitan explícitamente que se carguen DXGIDebug.dll en su lugar. Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) y especifique el \_ marcador de \_ depuración de DXGI CREATE Factory \_ para solicitar DXGIDebug.dll; la dll se cargará si está presente en el sistema.<br/> |
| [**DXGIDeclareAdapterRemovalSupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Permite que un proceso indique que es resistente a cualquiera de sus dispositivos de gráficos que se quitan.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Recupera una interfaz de depuración.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | Recupera una interfaz que las aplicaciones de la tienda Windows usan para depurar la infraestructura de gráficos de Microsoft DirectX (DXGI).<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




