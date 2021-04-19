---
description: Un proceso primario puede especificar propiedades asociadas a la ventana principal de su proceso secundario.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Establecer las propiedades de la ventana mediante STARTUPINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff59f9ae4473174325880a863f5b1f2fc4203e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677829"
---
# <a name="setting-window-properties-using-startupinfo"></a>Establecer las propiedades de la ventana mediante STARTUPINFO

Un proceso primario puede especificar propiedades asociadas a la ventana principal de su proceso secundario. La función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) toma un puntero a una estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) como uno de sus parámetros. Use los miembros de esta estructura para especificar las características de la ventana principal del proceso secundario. El miembro **dwFlags** contiene un campo de bits que determina qué otros miembros de la estructura se usan. Esto le permite especificar valores para cualquier subconjunto de las propiedades de la ventana. El sistema utiliza los valores predeterminados para las propiedades que no se especifican. El miembro **dwFlags** también puede forzar que se muestre un cursor de comentarios durante la inicialización del nuevo proceso.

Para los procesos de GUI, la estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especifica los valores predeterminados que se van a usar la primera vez que el nuevo proceso llame a las funciones [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) y [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) para crear y mostrar una ventana superpuesta. Se pueden especificar los siguientes valores predeterminados:

-   Ancho y alto, en píxeles, de la ventana creada por [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   La ubicación, en coordenadas de pantalla de la ventana creada por [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   Parámetro *nCmdShow* de [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).

Para los procesos de la consola, use la estructura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) para especificar las propiedades de la ventana solo al crear una nueva consola (ya sea mediante [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) con crear \_ nueva \_ consola o con la función [**AllocConsole**](/windows/console/allocconsole) ). La estructura **STARTUPINFO** se puede utilizar para especificar las siguientes propiedades de la ventana de la consola:

-   Tamaño de la nueva ventana de la consola, en celdas de caracteres.
-   Ubicación de la nueva ventana de la consola, en coordenadas de la pantalla.
-   Tamaño, en celdas de carácter, del búfer de pantalla de la nueva consola.
-   Los atributos de color de fondo y de texto del búfer de pantalla de la nueva consola.
-   Título de la ventana de la nueva consola.

 

 
