---
description: Las aplicaciones de Direct3D de pantalla completa proporcionan un identificador de ventana para el tiempo de ejecución de Direct3D.
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: Problemas de multithreading (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d163698e6cc1b4855668d255ed46fd28700d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422800"
---
# <a name="multithreading-issues-direct3d-9"></a>Problemas de multithreading (Direct3D 9)

Las aplicaciones de Direct3D de pantalla completa proporcionan un identificador de ventana para el tiempo de ejecución de Direct3D. La ventana está enlazada por el tiempo de ejecución. Esto significa que todos los mensajes pasados al procedimiento de mensaje de ventana de la aplicación se han examinado primero con el procedimiento de control de mensajes propio del tiempo de ejecución de Direct3D.

Los cambios en el modo de presentación se ven afectados por las rutinas de compatibilidad integradas en el sistema operativo subyacente. Cuando se producen cambios en el modo, el sistema difunde varios mensajes a todas las aplicaciones. En las aplicaciones de Direct3D, los mensajes se reciben en el subproceso de procedimiento de ventana, que no es necesariamente el mismo subproceso que llamó a [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) o [**IDirect3D9:: CreateDevice**](/windows/desktop/api) (o la versión final de [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9), que puede provocar un cambio en el modo de presentación). El tiempo de ejecución de Direct3D mantiene varias secciones críticas internamente. Dado que al menos una de estas secciones críticas se mantiene en el modificador de modo producido por **IDirect3DDevice9:: RESET** o **IDirect3D9:: CreateDevice**, estas secciones críticas se siguen conservando cuando la aplicación recibe los mensajes de ventana relacionados con el cambio de modo.

Este diseño tiene algunas implicaciones para las aplicaciones multiproceso. En concreto, una aplicación debe estar seguro de separar los subprocesos de control de mensajes de ventana de sus subprocesos de Direct3D. Una aplicación que provoca un cambio de modo en un subproceso, pero hace que las llamadas de Direct3D en un subproceso diferente en el procedimiento de ventana esté en peligro del interbloqueo.

Por estos motivos, Direct3D está diseñado de modo que los métodos [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), [**IDirect3D9:: CreateDevice**](/windows/desktop/api), [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)o la versión final de [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) solo se pueden llamar desde el mismo subproceso que controla los mensajes de ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
