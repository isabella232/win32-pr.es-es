---
title: Métodos de IPaper
description: Proporciona objetos COPaper controlados principalmente por su interfaz IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a45322e35f07a6f136e76ecaad6ae237891a741dfb44a6b5db0702c87bda33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662725"
---
# <a name="ipaper-methods"></a>Métodos de IPaper

**StoServe proporciona** objetos COPaper controlados principalmente por su interfaz **IPaper** nativa.

En la tabla siguiente se **enumeran los métodos IPaper** de IPAPER. H en el directorio \\ INC relacionado.



| Método    | Descripción                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Inicializa el objeto de papel y crea una matriz de datos de entrada de lápiz.                 |
| Lock      | Proporciona al cliente el control del papel y bloquea a otros clientes.      |
| Desbloquear    | Relinquisa el control de cliente del documento.                           |
| Cargar      | Carga contenido de papel desde el archivo compuesto del cliente y notifica a los receptores. |
| Guardar      | Guarda el contenido del papel en el archivo compuesto del cliente.                      |
| InkStart  | Inicia el dibujo de lápiz de color en la superficie del papel.                      |
| InkDraw   | Coloca puntos de datos de entrada de lápiz en la superficie de papel electrónico.               |
| InkStop   | Detiene el dibujo con lápiz en la superficie de papel.                             |
| Borrar     | Borre el contenido del papel actual y notimente a los receptores.                 |
| Cambiar de tamaño    | Cambia el tamaño del rectángulo de papel de dibujo y notifica a los receptores.        |
| Redibujar    | Vuelve a dibujar el contenido del objeto de papel y notifica a los receptores.                |



 

Los métodos de interés para este ejemplo de código en archivos compuestos son [**Cargar,**](ipaper--load.md) [**Guardar**](ipaper--save.md)y Volver [**a dibujar.**](ipaper--redraw.md)

[**InkStart,**](inkstart-method.md) [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) son métodos usados por los clientes para comando COPaper para registrar secuencias de dibujo de lápiz. El cliente normalmente responderá a un mensaje WM LBUTTONDOWN como el inicio de una secuencia de dibujo de entrada manuscrita mediante una llamada a \_ **InkStart** en COPaper. A medida que el usuario mueve el mouse o el lápiz para dibujar mientras mantiene presionado el botón izquierdo, el cliente responderá a mensajes WM MOUSEMOVE repetidos con las llamadas correspondientes a \_ **InkDraw.** Cuando el usuario suelta el botón izquierdo del mouse, el cliente responderá a un mensaje LBUTTONUP de WM con una llamada \_ a **InkStop**, que marca el final de la secuencia de dibujo de lápiz.

[**InkStart indica**](inkstart-method.md) a COPaper la posición inicial de la secuencia de dibujo en coordenadas de ventana de cliente. También pasa el color y el ancho de lápiz seleccionados actualmente. El cliente mantiene estas selecciones; COPaper simplemente los registra cuando se realiza la llamada **a InkStart.** [**Se llama a InkDraw**](inkdraw-method.md) repetidamente para decir a COPaper la sucesión de coordenadas de ventana que representan el movimiento de dibujo del mouse o del lápiz. [**InkStop indica**](cguipaper-methods.md) a COPaper que marque el final de una secuencia de dibujo.

 

 




