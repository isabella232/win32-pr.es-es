---
description: El sistema reduce la ventana principal de una aplicación (estilo superpuesto) a una ventana minimizada cuando el usuario hace clic en Minimizar en el menú de la ventana o la aplicación llama a la función ShowWindow y especifica un valor como SW \_ MINIMIZE.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Minimizado Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475930"
---
# <a name="minimized-windows"></a>Minimizado Windows

El sistema reduce la ventana principal de una aplicación (estilo superpuesto) a una ventana minimizada cuando el usuario hace clic en Minimizar en el menú de la ventana o la aplicación llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) y especifica un valor como SW \_ MINIMIZE. Minimizar una ventana acelera el rendimiento del sistema al reducir la cantidad de trabajo que debe realizar una aplicación al actualizar su ventana principal.

En el caso de una aplicación típica, el sistema dibuja un icono, denominado icono de clase, cuando se minimiza la ventana, etiquetando el icono con el nombre de la ventana. La aplicación especifica el icono de clase, una imagen estática que representa la aplicación, cuando registra la clase de ventana. La aplicación asigna un identificador al icono de clase al **miembro hIcon** de [**WNDCLASS antes**](/windows/win32/api/winuser/ns-winuser-wndclassa) de llamar a [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). La aplicación puede usar la [**función LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para recuperar el identificador de icono.

 

 
