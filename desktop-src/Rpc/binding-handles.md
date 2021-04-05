---
title: Identificadores de enlace
description: El enlace es el proceso de creación de una conexión lógica entre un programa cliente y un programa de servidor. La información que constituye el enlace entre el cliente y el servidor se representa mediante una estructura denominada identificador de enlace.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533232"
---
# <a name="binding-handles"></a>Identificadores de enlace

El enlace es el proceso de creación de una conexión lógica entre un programa cliente y un programa de servidor. La información que constituye el enlace entre el cliente y el servidor se representa mediante una estructura denominada identificador de enlace.

Un identificador de enlace es análogo a un identificador de archivo que la función de la biblioteca en tiempo de ejecución fopen de C devuelve, o un identificador de ventana que devuelve la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .

Al igual que con estos identificadores, la aplicación no puede tener acceso a la información del controlador de enlace ni manipularla directamente. La información de una estructura de datos de controlador de enlace solo está disponible para las bibliotecas en tiempo de ejecución de RPC. Proporciona el identificador, las bibliotecas en tiempo de ejecución tienen acceso y manipulan los datos adecuados.

En esta sección se presenta una descripción de los identificadores de enlace de los temas siguientes:

-   [Tipos de identificadores de enlace](types-of-binding-handles.md)
-   [Enlace del lado cliente](client-side-binding.md)
-   [Enlace del lado servidor](server-side-binding.md)
-   [Identificadores de enlace completo y parcialmente](fully-and-partially-bound-handles.md)
-   [Interpretar la información de enlace](interpreting-binding-information.md)
-   [Extensiones de Binding-Handle de Microsoft RPC](microsoft-rpc-binding-handle-extensions.md)
-   [Funciones de control de enlace](binding-handle-functions.md)
-   [La base de datos del servicio de nombres RPC](the-rpc-name-service-database.md)

 

 