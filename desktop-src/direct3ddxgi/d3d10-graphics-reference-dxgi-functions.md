---
description: Esta sección contiene información sobre las funciones proporcionadas por DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: Funciones DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881151c2225d58f583c466b799f15002bc9a23a83f56d878c76088a85f500f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745685"
---
# <a name="dxgi-functions"></a>Funciones DXGI

Esta sección contiene información sobre las funciones proporcionadas por DXGI.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Crea un generador DXGI 1.0 que puede usar para generar otros objetos DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Crea un generador DXGI 1.1 que puede usar para generar otros objetos DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Crea un generador DXGI 1.3 que puede usar para generar otros objetos DXGI.<br/> En Windows 8, cualquier generador DXGI creado mientras DXGIDebug.dll estaba presente en el sistema se cargaría y usaría. A partir Windows 8.1, las aplicaciones solicitan explícitamente que DXGIDebug.dll cargar en su lugar. Use [**CreateDXGIFactory2 y**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) especifique la marca DXGI CREATE FACTORY DEBUG para solicitar DXGIDebug.dll; el archivo DLL se cargará si está \_ presente en el \_ \_ sistema.<br/> |
| [**DXGIDeclareAdapterRemovalSupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Permite que un proceso indique que es resistente a cualquiera de sus dispositivos gráficos que se quitan.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Recupera una interfaz de depuración.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | Recupera una interfaz que usa Windows store para depurar microsoft Infraestructura de gráficos de DirectX (DXGI).<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




