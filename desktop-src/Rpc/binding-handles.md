---
title: Identificadores de enlace
description: El enlace es el proceso de crear una conexión lógica entre un programa cliente y un programa de servidor. La información que compone el enlace entre el cliente y el servidor se representa mediante una estructura denominada identificador de enlace.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09eae434fde790531a6f723cab6dc0b0613ee2fc99d680478d697cb550d6a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932345"
---
# <a name="binding-handles"></a>Identificadores de enlace

El enlace es el proceso de crear una conexión lógica entre un programa cliente y un programa de servidor. La información que compone el enlace entre el cliente y el servidor se representa mediante una estructura denominada identificador de enlace.

Un identificador de enlace es análogo a un identificador de archivo que devuelve la función de biblioteca en tiempo de ejecución fopen C o un identificador de ventana que devuelve [**la función CreateWindow.**](/windows/win32/api/winuser/nf-winuser-createwindowa)

Al igual que con estos identificadores, la aplicación no puede acceder directamente a la información del identificador de enlace ni manipularla. La información de una estructura de datos de identificador de enlace solo está disponible para las bibliotecas en tiempo de ejecución de RPC. Proporcione el identificador y las bibliotecas en tiempo de ejecución accedan y manipulen los datos adecuados.

En esta sección se presenta una explicación sobre los identificadores de enlace en los temas siguientes:

-   [Tipos de identificadores de enlace](types-of-binding-handles.md)
-   [Enlace del lado cliente](client-side-binding.md)
-   [Enlace del lado servidor](server-side-binding.md)
-   [Identificadores totalmente y parcialmente enlazados](fully-and-partially-bound-handles.md)
-   [Interpretación de la información de enlace](interpreting-binding-information.md)
-   [Extensiones de Binding-Handle RPC de Microsoft](microsoft-rpc-binding-handle-extensions.md)
-   [Funciones de identificador de enlace](binding-handle-functions.md)
-   [La base de datos del servicio de nombres RPC](the-rpc-name-service-database.md)

 

 