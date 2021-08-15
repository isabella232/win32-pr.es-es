---
title: Diferencias de subprocesos entre versiones de Direct3D
description: Muchos modelos de programación multiproceso usan primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas y evitar que más de un subproceso a la vez acceda al código.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9b53e53ad10dc662bfb57dc880c6423b3df0f320d109f212e54c10f3b9f314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913062"
---
# <a name="threading-differences-between-direct3d-versions"></a>Diferencias de subprocesos entre versiones de Direct3D

Muchos modelos de programación multiproceso usan primitivas de sincronización (como exclusiones mutuas) para crear secciones críticas y evitar que más de un subproceso a la vez acceda al código.

Sin embargo, los métodos de creación de recursos de la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) se diseñaron para volver a participar, sin necesidad de primitivas de sincronización y secciones críticas. Como resultado, los métodos de creación de recursos son eficaces y fáciles de usar.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 11, 10 y 9:<br/> El valor predeterminado de Direct3D 11 es principalmente seguro para subprocesos y sigue permitiendo que las aplicaciones opten por no usar D3D11 \_ CREATE \_ DEVICE \_ SINGLETHREADED. Si las aplicaciones optan por no ser seguras para subprocesos, deben cumplir las reglas de subprocesos. El tiempo de ejecución sincroniza los subprocesos en nombre de la aplicación, lo que permite ejecutar subprocesos simultáneos. De hecho, la sincronización en Direct3D 11 es más eficaz que usar la capa segura para subprocesos en Direct3D 10.<br/> Direct3D 10 puede admitir la ejecución de solo un subproceso a la vez. Direct3D 10 es totalmente seguro para subprocesos y permite a una aplicación rechazar ese comportamiento mediante D3D10 \_ CREATE \_ DEVICE SINGLE \_ \_ THREADED. <br/> Direct3D 9 no tiene como valor predeterminado la seguridad para subprocesos. Sin embargo, al llamar a [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) o [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) para crear un dispositivo, puede especificar la marca D3DCREATE MULTITHREADED para que el subproceso de LA API de \_ Direct3D 9 sea seguro. Esto provoca una sobrecarga de sincronización significativa. Por lo tanto, no se recomienda hacer que el subproceso de la API de Direct3D 9 sea seguro porque el rendimiento se puede degradar.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

