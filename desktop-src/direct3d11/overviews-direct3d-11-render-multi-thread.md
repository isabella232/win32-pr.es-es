---
title: Multithreading
description: Direct3D 11 implementa compatibilidad con la creación y representación de objetos mediante varios subprocesos.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718d80d9b70db0d6102d746168f338ddd8099339cee349724d87036714b16580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124330"
---
# <a name="multithreading"></a>Multithreading

Direct3D 11 implementa compatibilidad con la creación y representación de objetos mediante varios subprocesos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                   | Descripción                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción a multithreading en Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | Multithreading está diseñado para mejorar el rendimiento mediante el trabajo mediante uno o varios subprocesos al mismo tiempo. <br/>                                                                                                         |
| [Creación de objetos con multithreading](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | Use la [**interfaz ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para crear recursos y objetos, use [**id3D11DeviceContext para**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) [representar](overviews-direct3d-11-render-multi-thread-render.md).<br/> |
| [Representación inmediata y diferida](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | Direct3D 11 admite dos tipos de representación: inmediato y aplazado. Ambos se implementan mediante la [**interfaz ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/>                                                      |
| [Lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | Una lista de comandos es una secuencia de comandos de GPU que se pueden grabar y reproducir. Una lista de comandos puede mejorar el rendimiento al reducir la cantidad de sobrecarga generada por el tiempo de ejecución.<br/>                                    |
| [Diferencias de subprocesos entre versiones de Direct3D](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | Muchos modelos de programación multiproceso usan primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas e impedir que más de un subproceso a la vez acceda al código.<br/>                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comprobación de la compatibilidad con controladores](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[Representación](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





