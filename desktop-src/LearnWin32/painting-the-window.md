---
title: Pintar la ventana
description: Ha creado la ventana. Ahora desea mostrar algo dentro de ella. En la terminología de Windows, esto se denomina pintar la ventana. Para mezclar metáforas, una ventana es un lienzo en blanco que espera a que se rellene.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104558165"
---
# <a name="painting-the-window"></a>Pintar la ventana

Ha creado la ventana. Ahora desea mostrar algo dentro de ella. En la terminología de Windows, esto se denomina pintar la ventana. Para mezclar metáforas, una ventana es un lienzo en blanco que espera a que se rellene.

A veces, el programa iniciará el dibujo para actualizar la apariencia de la ventana. En otras ocasiones, el sistema operativo le notificará que debe volver a dibujar una parte de la ventana. Cuando esto ocurre, el sistema operativo envía a la ventana un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) . La parte de la ventana que se debe pintar se denomina *región de actualización*.

La primera vez que se muestra una ventana, se debe pintar todo el área cliente de la ventana. Por lo tanto, siempre recibirá al menos un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) al mostrar una ventana.

![Ilustración en la que se muestra la región de actualización de una ventana](images/painting01.png)

Solo es responsable de pintar el área de cliente. El sistema operativo pinta automáticamente el marco circundante, incluida la barra de título. Una vez que haya terminado de pintar el área de cliente, desactive la región de actualización, que indica al sistema operativo que no necesita enviar otro mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) hasta que algo cambie.

Ahora Supongamos que el usuario mueve otra ventana para ocultar una parte de la ventana. Cuando la parte oscurecida vuelve a estar visible, esa parte se agrega a la región de actualización y la ventana recibe otro mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .

![Ilustración que muestra cómo cambia la región de actualización cuando dos ventanas se superponen](images/painting02.png)

La región de actualización también cambia si el usuario estira la ventana. En el diagrama siguiente, el usuario estira la ventana a la derecha. El área recién expuesta en el lado derecho de la ventana se agrega a la región de actualización:

![Ilustración que muestra cómo cambia la región de actualización cuando se cambia el tamaño de una ventana](images/painting03.png)

En el primer programa de ejemplo, la rutina de pintado es muy sencilla. Simplemente rellena todo el área cliente con un color sólido. Aun así, este ejemplo es suficiente para mostrar algunos de los conceptos importantes.

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

Inicie la operación de dibujo llamando a la función [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) . Esta función rellena la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) con información sobre la solicitud Repaint. La región de actualización actual se proporciona en el miembro **rcPaint** de **paintstruct (**. Esta región de actualización se define en relación con el área de cliente:

![Ilustración que muestra el origen del área cliente](images/painting04.png)

En el código de dibujo, tiene dos opciones básicas:

- Pinte todo el área cliente, independientemente del tamaño de la región de actualización. Se recorta todo lo que queda fuera de la región de actualización. Es decir, el sistema operativo lo omite.
- Optimice dibujando solo la parte de la ventana dentro de la región de actualización.

Si siempre pinta el área de cliente completa, el código será más sencillo. Sin embargo, si tiene una lógica de dibujo complicada, puede ser más eficaz omitir las áreas fuera de la región de actualización.

La siguiente línea de código rellena la región de actualización con un solo color, utilizando el color de fondo de la ventana definida por el sistema (**\_ ventana de color**). El color real indicado por **la \_ ventana de color** depende de la combinación de colores actual del usuario.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Los detalles de [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) no son importantes para este ejemplo, pero el segundo parámetro proporciona las coordenadas del rectángulo que se va a rellenar. En este caso, pasamos toda la región de actualización (el miembro **rcPaint** de [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct)). En el primer mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) , es necesario pintar todo el área cliente, por lo que **rcPaint** contendrá todo el área cliente. En los mensajes de **\_ pintura de WM** posteriores, **rcPaint** podría contener un rectángulo más pequeño.

La función [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) forma parte de la interfaz de dispositivo gráfico (GDI), que ha alimentado los gráficos de Windows durante mucho tiempo. En Windows 7, Microsoft presentó un nuevo motor de gráficos, denominado Direct2D, que admite operaciones de gráficos de alto rendimiento, como la aceleración de hardware. Direct2D también está disponible para Windows Vista a través de la [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) y windows Server 2008 a través de la actualización de la plataforma para windows Server 2008. (La GDI sigue siendo totalmente compatible).

Cuando haya terminado de pintar, llame a la función [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) . Esta función borra la región de actualización, que indica a Windows que la ventana ha finalizado su dibujo.

## <a name="next"></a>Siguientes

[Cerrar la ventana](closing-the-window.md)