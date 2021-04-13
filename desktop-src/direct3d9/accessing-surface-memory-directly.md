---
description: 'Puede acceder directamente a la memoria de la superficie mediante el método IDirect3DSurface9:: LockRect.'
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: Acceso directo a la memoria de la superficie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360043"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>Acceso directo a la memoria de la superficie (Direct3D 9)

Puede acceder directamente a la memoria de la superficie mediante el método [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) . Cuando se llama a este método, el parámetro pRect es un puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que describe el rectángulo en la superficie para tener acceso a él directamente. Para solicitar que se bloquee toda la superficie, establezca pRect en **null**. Además, puede especificar un **Rect** que cubra solo una parte de la superficie. Siempre que no se superpongan dos rectángulos, dos subprocesos o procesos pueden bloquear simultáneamente varios rectángulos en una superficie. Tenga en cuenta que no se puede bloquear un búfer de reserva de muestreo.

El método [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) rellena una estructura de [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) con toda la información para tener acceso correctamente a la memoria de la superficie. La estructura incluye información sobre el paso y tiene un puntero a los bits bloqueados. Cuando termine de acceder a la memoria de la superficie, llame al método [**IDirect3DSurface9:: UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) para desbloquearlo.

Mientras tiene una superficie bloqueada, puede manipular directamente el contenido. En la lista siguiente se describen algunas sugerencias para evitar problemas comunes con la representación directa de la memoria de superficie.

-   No asuma nunca un tono de visualización constante. Examine siempre la información de tono devuelta por el método [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) . Este paso puede variar por una serie de motivos, como la ubicación de la memoria de la superficie, el tipo de tarjeta de visualización o incluso la versión del controlador de Direct3D. Para obtener más información, vea [ancho frente a tono (Direct3D 9)](width-vs--pitch.md).
-   Asegúrese de que copia en superficies desbloqueadas. Los métodos de copia de Direct3D producirán un error si se llaman en una superficie bloqueada.
-   Limite la actividad de la aplicación mientras se bloquea una superficie.
-   Copiar siempre los datos alineados para mostrar la memoria. Windows 98 usa un controlador de errores de página, Vflatd. 386, para implementar un búfer de fotogramas virtuales para mostrar tarjetas con memoria conmutada por Banco. El controlador permite que estos dispositivos de pantalla presenten un búfer de fotogramas lineal a Direct3D. La copia de datos sin alinear para mostrar la memoria puede hacer que el sistema suspenda las operaciones si la copia abarca los bancos de memoria.
-   Una superficie no puede estar bloqueada si pertenece a un recurso asignado al bloque de \_ memoria predeterminado de D3DPOOL a menos que sea una textura dinámica o una superficie creada con [**IDirect3DDevice9:: CreateOffscreenPlainSurface**](/windows/desktop/api). Las superficies de búfer de reserva, a las que se puede tener acceso mediante los métodos [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) y [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) , solo se pueden bloquear si la cadena de intercambio se ha creado con el miembro flags de [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) para incluir D3DPRESENTFLAG búfer de reserva con bloqueo \_ \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
