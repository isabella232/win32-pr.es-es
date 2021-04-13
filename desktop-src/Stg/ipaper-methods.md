---
title: Métodos IPaper
description: Proporciona objetos de copapeles controlados principalmente por su interfaz IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269317"
---
# <a name="ipaper-methods"></a>Métodos IPaper

**StoServe** proporciona objetos de copapeles controlados principalmente por su interfaz **IPaper** nativa.

En la tabla siguiente se enumeran los métodos de **IPaper** de IPaper. H en el directorio del mismo nivel \\ .



| Método    | Descripción                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Inicializa el objeto paper y crea una matriz de datos de tinta.                 |
| Lock      | Proporciona al cliente control del papel y bloquea a otros clientes.      |
| Desbloquear    | Abandona el control de la documentación del cliente.                           |
| Cargar      | Carga el contenido de papel del archivo compuesto del cliente y notifica a los receptores. |
| Guardar      | Guarda el contenido del papel en el archivo compuesto del cliente.                      |
| InkStart  | Inicia el dibujo de la tinta de color en la superficie del papel.                      |
| InkDraw   | Coloca los puntos de datos de tinta en la superficie electrónica del papel.               |
| InkStop   | Detiene el dibujo de la tinta en la superficie del papel.                             |
| Borrar     | Borre el contenido del papel actual y notifique a los receptores.                 |
| Cambiar de tamaño    | Cambia el tamaño del rectángulo del papel del dibujo y notifica a los receptores.        |
| Volver a dibujar    | Vuelve a dibujar el contenido del objeto de papel y notifica a los receptores.                |



 

Los métodos de interés para este ejemplo de código en archivos compuestos son cargar, [**Guardar**](ipaper--save.md)y [**volver**](ipaper--load.md)a [**dibujar**](ipaper--redraw.md).

[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) son métodos usados por los clientes para el copapel del comando para grabar secuencias de dibujo de tinta. Normalmente, el cliente responderá a un \_ mensaje de LBUTTONDOWN de WM como el inicio de una secuencia de dibujo de tinta mediante una llamada a **InkStart** en el copaper. A medida que el usuario mueve el mouse o el lápiz para dibujar mientras mantiene presionado el botón primario, el cliente responderá a los mensajes de la MOUSEMOVE de WM repetidos \_ con las llamadas correspondientes a **InkDraw**. Cuando el usuario suelta el botón primario del mouse, el cliente responde a un mensaje de WM \_ LBUTTONUP con una llamada a **InkStop**, que marca el final de la secuencia de dibujo de la tinta.

[**InkStart**](inkstart-method.md) indica al copaper la posición inicial de la secuencia de dibujo en coordenadas de la ventana del cliente. También pasa el color y el ancho de la tinta seleccionados actualmente. El cliente mantiene estas selecciones; El copapel simplemente los registra cuando se realiza la llamada a **InkStart** . Se llama a [**InkDraw**](inkdraw-method.md) varias veces para indicar a los copapeles la sucesión de coordenadas de la ventana que representan el movimiento del dibujo del mouse o del lápiz. [**InkStop**](cguipaper-methods.md) indica al copaper que marque el final de una secuencia de dibujo.

 

 




