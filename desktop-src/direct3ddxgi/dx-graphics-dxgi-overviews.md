---
description: Microsoft Infraestructura de gráficos de DirectX (DXGI) administra tareas de bajo nivel que pueden ser independientes del entorno de ejecución de gráficos de Direct3D. DXGI proporciona un marco común para varias versiones de Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Guía de programación para DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0ac41155557c14ca41f8e0ea9f1836247bd3b78da213c1fbbed521499eae7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518388"
---
# <a name="programming-guide-for-dxgi"></a>Guía de programación para DXGI

Microsoft Infraestructura de gráficos de DirectX (DXGI) administra tareas de bajo nivel que pueden ser independientes del entorno de ejecución de gráficos de Direct3D. DXGI proporciona un marco común para varias versiones de Direct3D.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                              | Descripción                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | En este tema se incluyen las siguientes secciones.<br/>                                                                                                                   |
| [Mejoras de DXGI 1.2](dxgi-1-2-improvements.md)<br/>                                                                      | Se ha agregado la siguiente funcionalidad en DXGI 1.2.<br/>                                                                                                       |
| [Mejoras de DXGI 1.3](dxgi-1-3-improvements.md)<br/>                                                                      | La siguiente funcionalidad se ha agregado en DXGI 1.3, que se incluye a partir de Windows 8.1.<br/>                                                            |
| [Mejoras de DXGI 1.4](dxgi-1-4-improvements.md)<br/>                                                                      | La siguiente funcionalidad se ha agregado o cambiado en DXGI 1.4, en gran medida para admitir Direct3D 12. <br/>                                                           |
| [Mejoras de DXGI 1.5](dxgi-1-5-improvements.md)<br/>                                                                      | La siguiente funcionalidad se ha agregado a DXGI 1.5, para admitir la especificación y duplicación más flexibles de formatos de salida.<br/>                                |
| [Mejoras de DXGI 1.6](dxgi-1-6-improvements.md)<br/>                                                                      | Se ha agregado la siguiente funcionalidad a DXGI 1.6 para detectar pantallas HDR.<br/>                                                                       |
| [Uso de DirectX con pantallas de alto rango dinámico y color avanzado](../direct3darticles/high-dynamic-range.md)     | En este tema se proporciona información general técnica sobre la representación de contenido de direct3D 11 y Direct3D 12 de alto rango dinámico en una pantalla DE HDR10 Windows 10 compatibilidad avanzada con colores.<br/> |
| [Se muestra la frecuencia de actualización variable](variable-refresh-rate-displays.md)<br/>                                                    | Las pantallas de *frecuencia* de actualización variable requieren que se habilite el desmontado, lo que también se conoce como compatibilidad con "vsync-off".<br/>                                                    |
| [Uso de la corrección gamma](using-gamma-correction.md)<br/>                                                                    | Corrección gamma, o gamma para abre abrez, es el nombre de una operación no lineal que los sistemas usan para codificar y descodificar valores de píxeles en imágenes.<br/>                        |
| [Compatibilidad con formatos para hardware de direct3D Feature 10Level9 9.1](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D Feature 10Level9 9.1.<br/>        |
| [Compatibilidad con formatos para hardware de direct3D Feature 10Level9 9.3](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D Feature 10Level9 9.3.<br/>        |
| [Compatibilidad de formato con hardware de nivel de característica 10.0 de Direct3D](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D 10.0.<br/>                        |
| [Compatibilidad de formato con hardware de nivel de característica 10.1 de Direct3D](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D 10.1.<br/>                        |
| [Compatibilidad de formato con hardware de nivel de característica 11.0 de Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 11.0 de Direct3D.<br/>          |
| [Compatibilidad de formato con hardware de nivel 11.1 de características de Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 11.1 de Direct3D.<br/>          |
| [Compatibilidad de formato con hardware de nivel de característica 12.0 de Direct3D](hardware-support-for-direct3d-12-0-formats.md)<br/>               | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de nivel de característica 12.0 de Direct3D.<br/>          |
| [Compatibilidad con formatos para hardware de nivel 12.1 de características de Direct3D](hardware-support-for-direct3d-12-1-formats.md)<br/>               | En esta sección se especifican los formatos [**(valores \_ DXGI FORMAT)**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que se admiten en el hardware de Direct3D 12.1.<br/>                        |
| [Comprobación de la compatibilidad con características de hardware](checking-hardware-feature-support.md)<br/>                                              | En esta sección se explica cómo comprobar la compatibilidad con el formato del hardware de nivel de característica de Direct3D mediante llamadas API.<br/>                                                       |
| [Para obtener el mejor rendimiento, use el modelo de volteo DXGI.](for-best-performance--use-dxgi-flip-model.md)<br/>                              | En este tema se proporcionan instrucciones para desarrolladores sobre cómo maximizar el rendimiento y la eficacia en la pila de presentación en versiones modernas de Windows.<br/>                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Referencia de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[Infraestructura de gráficos de DirectX (DXGI): Procedimientos recomendados](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
