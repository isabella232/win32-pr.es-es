---
description: Puede acceder directamente a la memoria de la superficie mediante el método IDirect3DSurface9::LockRect.
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: Acceso directo a la memoria de surface (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174842"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>Acceso directo a la memoria de surface (Direct3D 9)

Puede acceder directamente a la memoria de la superficie mediante el [**método IDirect3DSurface9::LockRect.**](/windows/desktop/api) Cuando se llama a este método, el parámetro pRect es un puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que describe el rectángulo de la superficie al que se va a acceder directamente. Para solicitar que se bloquee toda la superficie, establezca pRect en **NULL.** Además, puede especificar un **RECT** que cubre solo una parte de la superficie. Siempre que no se superpongan dos rectángulos, dos subprocesos o procesos pueden bloquear simultáneamente varios rectángulos en una superficie. Tenga en cuenta que no se puede bloquear un búfer de copia de seguridad de varias muestras.

El [**método IDirect3DSurface9::LockRect**](/windows/desktop/api) rellena una estructura [**\_ RECT D3DLOCKED**](d3dlocked-rect.md) con toda la información para acceder correctamente a la memoria de la superficie. La estructura incluye información sobre el paso y tiene un puntero a los bits bloqueados. Cuando termine de acceder a la memoria de superficie, llame al método [**IDirect3DSurface9::UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) para desbloquearla.

Aunque tiene una superficie bloqueada, puede manipular directamente el contenido. En la lista siguiente se describen algunas sugerencias para evitar problemas comunes con la representación directa de la memoria de la superficie.

-   No suponga nunca un tono de presentación constante. Examine siempre la información de tono devuelta por [**el método IDirect3DSurface9::LockRect.**](/windows/desktop/api) Este tono puede variar por varias razones, incluida la ubicación de la memoria de superficie, el tipo de tarjeta de presentación o incluso la versión del controlador Direct3D. Para obtener más información, [vea Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).
-   Asegúrese de copiar en superficies desbloqueadas. Los métodos de copia de Direct3D producirán un error si se llama a en una superficie bloqueada.
-   Limite la actividad de la aplicación mientras se bloquea una superficie.
-   Copie siempre los datos alineados para mostrar la memoria. Windows 98 usa un controlador de errores de página, Vflatd.386, para implementar un búfer de marco plano virtual para tarjetas de presentación con memoria conmutada por banco. El controlador permite que estos dispositivos de visualización presenten un búfer de fotograma lineal en Direct3D. Copiar datos no alineados para mostrar memoria puede hacer que el sistema suspenda las operaciones si la copia abarca bancos de memoria.
-   Es posible que una superficie no se bloquee si pertenece a un recurso asignado al grupo de memoria D3DPOOL DEFAULT a menos que sea una textura dinámica o una superficie creada mediante \_ [**IDirect3DDevice9::CreateOffscreenPlainSurface**](/windows/desktop/api). Las superficies de búfer de reserva, a las que se puede acceder mediante los métodos [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) e [**IDirect3DSwapChain9::GetBackBuffer,**](/windows/desktop/api) solo se pueden bloquear si la cadena de intercambio se creó con el miembro Flags de [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) para incluir D3DPRESENTFLAG \_ LOCKABLE \_ BACKBUFFER.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
