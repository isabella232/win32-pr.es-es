---
title: Pintar la ventana
description: Ha creado la ventana. Ahora quiere mostrar algo dentro de él. En Windows terminología, esto se denomina pintar la ventana. Para mezclar metáforas, una ventana es un lienzo en blanco, esperando a que lo rellene.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159944"
---
# <a name="painting-the-window"></a>Pintar la ventana

Ha creado la ventana. Ahora quiere mostrar algo dentro de él. En Windows terminología, esto se denomina pintar la ventana. Para mezclar metáforas, una ventana es un lienzo en blanco, esperando a que lo rellene.

A veces, el programa iniciará la pintura para actualizar la apariencia de la ventana. En otras ocasiones, el sistema operativo le notificará que debe volver a dibujar una parte de la ventana. Cuando esto sucede, el sistema operativo envía a la ventana un [**mensaje \_ WM PAINT.**](/windows/desktop/gdi/wm-paint) La parte de la ventana que se debe pintar se denomina región *de actualización*.

La primera vez que se muestra una ventana, se debe pintar todo el área de cliente de la ventana. Por lo tanto, siempre recibirá al menos un [**mensaje \_ WM PAINT**](/windows/desktop/gdi/wm-paint) cuando muestre una ventana.

![ilustración que muestra la región de actualización de una ventana](images/painting01.png)

Solo es responsable de pintar el área de cliente. El sistema operativo pinta automáticamente el marco circundante, incluida la barra de título. Cuando termine de pintar el área de cliente, borre la región de actualización, que indica al sistema operativo que no es necesario enviar otro mensaje [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) hasta que cambie algo.

Ahora supongamos que el usuario mueve otra ventana para que oculte una parte de la ventana. Cuando la parte oculta vuelve a estar visible, esa parte se agrega a la región de actualización y la ventana recibe otro [**mensaje \_ WM PAINT.**](/windows/desktop/gdi/wm-paint)

![ilustración en la que se muestra cómo cambia la región de actualización cuando dos ventanas se superponen](images/painting02.png)

La región de actualización también cambia si el usuario extiende la ventana. En el diagrama siguiente, el usuario extiende la ventana a la derecha. El área recién expuesta en el lado derecho de la ventana se agrega a la región de actualización:

![ilustración en la que se muestra cómo cambia la región de actualización cuando se cambia el tamaño de una ventana](images/painting03.png)

En nuestro primer programa de ejemplo, la rutina de dibujo es muy sencilla. Simplemente rellena todo el área de cliente con un color sólido. Aun así, este ejemplo es suficiente para demostrar algunos de los conceptos importantes.

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

Inicie la operación de dibujo mediante una llamada a [**la función BeginPaint.**](/windows/desktop/api/winuser/nf-winuser-beginpaint) Esta función rellena la estructura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con información sobre la solicitud de repintado. La región de actualización actual se indica en el **miembro rcPaint** de **PAINTSTRUCT**. Esta región de actualización se define en relación con el área de cliente:

![ilustración que muestra el origen del área cliente](images/painting04.png)

En el código de dibujo, tiene dos opciones básicas:

- Paint área de cliente completa, independientemente del tamaño de la región de actualización. Todo lo que se encuentra fuera de la región de actualización se recorta. Es decir, el sistema operativo lo omite.
- Optimice pintando solo la parte de la ventana dentro de la región de actualización.

Si siempre pinta todo el área de cliente, el código será más sencillo. Sin embargo, si tiene lógica de dibujo complicada, puede ser más eficaz omitir las áreas fuera de la región de actualización.

La siguiente línea de código rellena la región de actualización con un único color, usando el color de fondo de la ventana definida por el sistema (**COLOR \_ WINDOW**). El color real indicado por **COLOR \_ WINDOW** depende de la combinación de colores actual del usuario.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Los detalles de [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) no son importantes para este ejemplo, pero el segundo parámetro proporciona las coordenadas del rectángulo que se va a rellenar. En este caso, se pasa toda la región de actualización (el **miembro rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)). En el primer [**mensaje \_ WM PAINT,**](/windows/desktop/gdi/wm-paint) es necesario pintar todo el área de cliente, por lo que **rcPaint** contendrá todo el área de cliente. En los **mensajes \_ WM PAINT** posteriores, **rcPaint** podría contener un rectángulo más pequeño.

La [**función FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) forma parte de la Interfaz de dispositivo gráfico (GDI), que ha Windows gráficos durante mucho tiempo. En Windows 7, Microsoft introdujo un nuevo motor de gráficos, denominado Direct2D, que admite operaciones de gráficos de alto rendimiento, como la aceleración de hardware. Direct2D también está disponible para Windows Vista a través de la actualización de plataforma para [Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) y para Windows Server 2008 a través de la actualización de plataforma para Windows Server 2008. (GDI sigue siendo totalmente compatible).

Cuando haya terminado de pintar, llame a [**la función EndPaint.**](/windows/desktop/api/winuser/nf-winuser-endpaint) Esta función borra la región de actualización, que indica Windows que la ventana ha terminado de pintarse.

## <a name="next"></a>Siguientes

[Cerrar la ventana](closing-the-window.md)