---
description: La infraestructura de gráficos de Microsoft DirectX (DXGI) administra tareas de bajo nivel que pueden ser independientes del tiempo de ejecución de gráficos de Direct3D. DXGI proporciona un marco de trabajo común para varias versiones de Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Guía de programación para DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7834b2fc68019dccfb8ab8b2e62698465ff1ea2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274641"
---
# <a name="programming-guide-for-dxgi"></a>Guía de programación para DXGI

La infraestructura de gráficos de Microsoft DirectX (DXGI) administra tareas de bajo nivel que pueden ser independientes del tiempo de ejecución de gráficos de Direct3D. DXGI proporciona un marco de trabajo común para varias versiones de Direct3D.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                              | Descripción                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | En este tema se incluyen las siguientes secciones.<br/>                                                                                                                   |
| [Mejoras en DXGI 1,2](dxgi-1-2-improvements.md)<br/>                                                                      | En DXGI 1,2 se ha agregado la siguiente funcionalidad.<br/>                                                                                                       |
| [Mejoras en DXGI 1,3](dxgi-1-3-improvements.md)<br/>                                                                      | La siguiente funcionalidad se ha agregado en DXGI 1,3, que se incluye a partir de Windows 8.1.<br/>                                                            |
| [Mejoras en DXGI 1,4](dxgi-1-4-improvements.md)<br/>                                                                      | La siguiente funcionalidad se ha agregado o cambiado en DXGI 1,4, en gran medida para admitir Direct3D 12. <br/>                                                           |
| [Mejoras en DXGI 1,5](dxgi-1-5-improvements.md)<br/>                                                                      | Se ha agregado la siguiente funcionalidad a DXGI 1,5, para admitir la especificación y la duplicación más flexibles de los formatos de salida.<br/>                                |
| [Mejoras en DXGI 1,6](dxgi-1-6-improvements.md)<br/>                                                                      | Se ha agregado la siguiente funcionalidad a DXGI 1,6 para detectar pantallas HDR.<br/>                                                                       |
| [Uso de DirectX con pantallas de alto rango dinámico y color avanzado](../direct3darticles/high-dynamic-range.md)     | En este tema se proporciona información general técnica sobre la representación de contenido de Direct3D 11 y Direct3D 12 de rango dinámico alto en una pantalla de HDR10 con compatibilidad con el color avanzado de Windows 10.<br/> |
| [Se muestra la frecuencia de actualización de variables](variable-refresh-rate-displays.md)<br/>                                                    | La frecuencia de *actualización de variables muestra requerir el* desactivado para habilitarla, lo que también se conoce como compatibilidad con "VSYNC".<br/>                                                    |
| [Usar corrección gamma](using-gamma-correction.md)<br/>                                                                    | Corrección gamma, o gamma para abreviar, es el nombre de una operación no lineal que los sistemas usan para codificar y descodificar los valores de píxeles de las imágenes.<br/>                        |
| [Compatibilidad con el formato de la característica Direct3D 10Level9 9,1 hardware](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware 10Level9 9,1 de la característica Direct3D.<br/>        |
| [Compatibilidad con el formato de la característica Direct3D 10Level9 9,3 hardware](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware 10Level9 9,3 de la característica Direct3D.<br/>        |
| [Compatibilidad con el formato de hardware de nivel de característica de Direct3D 10,0](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware de Direct3D 10,0.<br/>                        |
| [Compatibilidad con el formato de hardware de nivel de característica de Direct3D 10,1](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware de Direct3D 10,1.<br/>                        |
| [Compatibilidad con el formato de hardware de nivel de característica de Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware de nivel de característica de Direct3D 11,0.<br/>          |
| [Compatibilidad con el formato de hardware de nivel de característica de Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware de nivel de característica de Direct3D 11,1.<br/>          |
| [Compatibilidad con el formato de hardware de nivel de característica de Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)<br/>               | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware de nivel de característica de Direct3D 12,0.<br/>          |
| [Compatibilidad con el formato de hardware de nivel de característica de Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)<br/>               | En esta sección se especifican los formatos (valores de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) que se admiten en el hardware de Direct3D 12,1.<br/>                        |
| [Comprobando la compatibilidad con las características de hardware](checking-hardware-feature-support.md)<br/>                                              | En esta sección se explica cómo comprobar la compatibilidad con el formato de hardware de nivel de característica de Direct3D mediante llamadas API.<br/>                                                       |
| [Para obtener el mejor rendimiento, use DXGI Flip Model](for-best-performance--use-dxgi-flip-model.md)<br/>                              | En este tema se proporcionan instrucciones para desarrolladores sobre cómo maximizar el rendimiento y la eficacia en la pila de presentaciones en versiones modernas de Windows.<br/>                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Referencia de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[Infraestructura de gráficos de DirectX (DXGI): procedimientos recomendados](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
