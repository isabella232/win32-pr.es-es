---
title: Trabajar con Direct3D 11, Direct3D 10 y Direct2D
description: En esta sección se tratan las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API de Direct3D 11on12 y las directrices de porte de Direct3D 11 a Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462febfc36c15e2af50f0d4f031bec026bbd8cd3713dafbd9678e733978f484e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989704"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Trabajar con Direct3D 11, Direct3D 10 y Direct2D

En esta sección se tratan las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API de Direct3D 11on12 y las directrices de porte de Direct3D 11 a Direct3D 12.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interoperabilidad de Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 se puede usar para escribir aplicaciones con componentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Direct3D 11 en 12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos D3D11 para impulsar la API D3D12. D3D11on12 permite que los componentes escritos mediante D3D11 (por ejemplo, texto D2D e interfaz de usuario) funcionen junto con componentes escritos que tienen como destino la API D3D12. D3D11on12 también permite la porción incremental de una aplicación de D3D11 a D3D12, al permitir que las partes de la aplicación sigan teniendo como destino D3D11 por motivos de simplicidad, mientras que otras tienen como destino D3D12 para el rendimiento, mientras que siempre tienen una representación completa y correcta. D3D11On12 simplifica el uso de técnicas de interoperabilidad para compartir recursos y sincronizar el trabajo entre las dos API. <br/> |
| [Portabilidad de Direct3D 11 a Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | En esta sección se proporcionan algunas instrucciones sobre cómo portear desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





