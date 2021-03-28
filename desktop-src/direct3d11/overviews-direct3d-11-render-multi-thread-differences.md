---
title: Diferencias de subprocesos entre versiones de Direct3D
description: Muchos modelos de programación multiproceso hacen uso de primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas e impedir que más de un subproceso tenga acceso a código a la vez.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e99c68dbdba1d6f0cdd789f6ccac8b81d4ac03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421042"
---
# <a name="threading-differences-between-direct3d-versions"></a>Diferencias de subprocesos entre versiones de Direct3D

Muchos modelos de programación multiproceso hacen uso de primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas e impedir que más de un subproceso tenga acceso a código a la vez.

Sin embargo, los métodos de creación de recursos de la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) se diseñaron para ser reentrantes, sin necesidad de primitivas de sincronización ni secciones críticas. Como resultado, los métodos de creación de recursos son eficaces y fáciles de usar.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 11, 10 y 9:<br/> Direct3D 11 tiene como valor predeterminado la mayoría de los subprocesos y sigue permitiendo que las aplicaciones no puedan optar por usar D3D11 \_ crear \_ dispositivo \_ SINGLETHREADED. Si las aplicaciones no están seguras para subprocesos, deben cumplir las reglas de subprocesamiento. El tiempo de ejecución sincroniza los subprocesos en nombre de la aplicación, lo que permite la ejecución de subprocesos simultáneos. De hecho, la sincronización en Direct3D 11 es más eficaz que el uso de la capa segura para subprocesos en Direct3D 10.<br/> Direct3D 10 solo admite la ejecución de un subproceso a la vez. Direct3D 10 es totalmente seguro para subprocesos y permite que una aplicación opte por ese comportamiento mediante D3D10 \_ crear \_ dispositivo de un \_ solo \_ subproceso. <br/> Direct3D 9 no tiene como valor predeterminado la seguridad para subprocesos. Sin embargo, cuando se llama a [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) o [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) para crear un dispositivo, se puede especificar la \_ marca multiproceso D3DCREATE para que la seguridad de SUBprocesos de la API de Direct3D 9 sea segura. Esto produce una sobrecarga de sincronización significativa. Por lo tanto, no se recomienda hacer que la seguridad para subprocesos de la API de Direct3D 9 sea posible, ya que se puede degradar el rendimiento.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

