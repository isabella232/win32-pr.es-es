---
title: Trabajar con Direct3D 11, Direct3D 10 y Direct2D
description: En esta sección se describen las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API 11on12 de Direct3D y las instrucciones de portabilidad de Direct3D 11 a Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103753"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>Trabajar con Direct3D 11, Direct3D 10 y Direct2D

En esta sección se describen las técnicas de interoperabilidad con versiones anteriores de Direct3D y Direct2D, la API 11on12 de Direct3D y las instrucciones de portabilidad de Direct3D 11 a Direct3D 12.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interoperabilidad de Direct3D 12](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 se puede usar para escribir aplicaciones en componentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Direct3D 11 en 12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 es un mecanismo por el que los desarrolladores pueden usar interfaces y objetos de D3D11 para impulsar la API de D3D12. D3D11on12 permite que los componentes escritos con D3D11 (por ejemplo, texto y la interfaz de usuario de D2D) funcionen juntos con los componentes escritos como destino de la API de D3D12. D3D11on12 también habilita el traslado incremental de una aplicación de D3D11 a D3D12, ya que permite que partes de la aplicación continúen orientadas a D3D11 para simplificar, mientras que otras se dirigen a D3D12 de rendimiento, a la vez que siempre tienen una representación completa y correcta. D3D11On12 simplifica el uso de técnicas de interoperabilidad para compartir recursos y sincronizar el trabajo entre las dos API. <br/> |
| [Portabilidad de Direct3D 11 a Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | En esta sección se proporcionan instrucciones sobre cómo migrar desde un motor de gráficos de Direct3D 11 personalizado a Direct3D 12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

 





