---
description: El sistema reduce la ventana principal de una aplicación (estilo superpuesto) a una ventana minimizada cuando el usuario hace clic en minimizar en el menú ventana o la aplicación llama a la función ShowWindow y especifica un valor como SW \_ minimizar.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Ventanas minimizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811935"
---
# <a name="minimized-windows"></a>Ventanas minimizadas

El sistema reduce la ventana principal de una aplicación (estilo superpuesto) a una ventana minimizada cuando el usuario hace clic en minimizar en el menú ventana o la aplicación llama a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) y especifica un valor como SW \_ minimizar. Minimizar una ventana acelera el rendimiento del sistema reduciendo la cantidad de trabajo que debe realizar una aplicación al actualizar su ventana principal.

En el caso de una aplicación típica, el sistema dibuja un icono, denominado icono de clase, cuando se minimiza la ventana, etiquetando el icono con el nombre de la ventana. La aplicación especifica el icono de clase, una imagen estática que representa la aplicación, cuando registra la clase de ventana. La aplicación asigna un identificador al icono de clase al miembro **hIcon** de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) antes de llamar a [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). La aplicación puede usar la función [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para recuperar el identificador de icono.

 

 
