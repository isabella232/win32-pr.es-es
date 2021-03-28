---
title: MultiThreading
description: Direct3D 11 implementa la compatibilidad con la creación y representación de objetos mediante varios subprocesos.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269094"
---
# <a name="multithreading"></a>MultiThreading

Direct3D 11 implementa la compatibilidad con la creación y representación de objetos mediante varios subprocesos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                   | Descripción                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción a multithreading en Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | El multithreading está diseñado para mejorar el rendimiento mediante la realización de trabajos mediante uno o varios subprocesos al mismo tiempo. <br/>                                                                                                         |
| [Creación de objetos con multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Use la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para crear recursos y objetos, use [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para la [representación](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Representación inmediata y diferida](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 admite dos tipos de representación: inmediato y aplazado. Ambos se implementan mediante la interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .<br/>                                                      |
| [Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Una lista de comandos es una secuencia de comandos de GPU que se pueden grabar y reproducir. Una lista de comandos puede mejorar el rendimiento reduciendo la cantidad de sobrecarga generada por el tiempo de ejecución.<br/>                                    |
| [Diferencias de subprocesos entre versiones de Direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Muchos modelos de programación multiproceso hacen uso de primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas e impedir que más de un subproceso tenga acceso a código a la vez.<br/>                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo: comprobar la compatibilidad de controladores](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Representación](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





