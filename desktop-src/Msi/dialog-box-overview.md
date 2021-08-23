---
description: El proceso de creación de un cuadro de diálogo en Windows Installer es similar al proceso de creación de un cuadro de diálogo mediante programación mediante una plantilla de cuadro de diálogo de api de Microsoft Windows.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Información general del cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17963148100d8f0d99a6fdb9e043654e089880b81ade0a943b92b4bfcd35f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764175"
---
# <a name="dialog-box-overview"></a>Información general del cuadro de diálogo

El proceso de creación de un cuadro de diálogo en Windows Installer es similar al proceso de creación de un cuadro de diálogo mediante programación mediante una plantilla de cuadro de diálogo de api de Microsoft Windows. Mientras que una Windows de cuadro de diálogo se almacena en una cadena de caracteres terminados en NULL, Windows Installer almacena los parámetros del cuadro de diálogo en la tabla Diálogo. La tabla Dialog contiene una columna de atributos que es análoga a los estilos de Ventana en la API de Windows de usuario de Microsoft. Sin embargo, el número de bits de estilo de diálogo Windows Installer es un conjunto reducido y especializado.

Para crear físicamente el cuadro de diálogo mediante la API Windows de interfaz de usuario, se llama a [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) y se pasa un puntero a la plantilla. En Windows instalador, el cuadro de diálogo se crea durante la ejecución de una de las tres tablas de secuencia de interfaz de usuario.

Windows El instalador no contiene una interfaz de usuario predeterminada que los autores de paquetes pueden utilizar para sus paquetes. Contiene un conjunto limitado de cuadros de diálogo predeterminados que muestran mensajes de error e información, pero solo se muestran si el instalador de Windows consulta las tablas Diálogo y Secuencia de interfaz de usuario y encuentra que no hay cuadros de diálogo personalizados disponibles.

El SDK del instalador incluye una base de datos mínima denominada Uisample.msi que contiene tablas de secuencia de ejecución y de interfaz de usuario rellenas y una interfaz de usuario completa. Esta base de datos se personaliza y combina fácilmente en cualquier paquete.

Algunas acciones estándar y condiciones de error Windows installer devuelven un conjunto específico de datos de interfaz de usuario y, por tanto, requieren un cuadro de diálogo con un conjunto específico de controles para dar cabida a los datos. Windows El instalador comprueba dos ubicaciones independientes para los identificadores de estos cuadros de diálogo.

-   Windows El instalador contiene un conjunto de nombres de cuadro de diálogo incrustados. La acción personalizada consulta estos nombres reservados en la tabla Dialog.
-   En cada una de las tres tablas de secuencia de interfaz de usuario, los nombres de diálogo con un número de secuencia de -1, -2 o -3 se muestran como respuesta a la salida, la salida solicitada por el usuario y los mensajes de error irreales de Windows Installer.

Hay disponible una lista completa de nombres de cuadro de diálogo de clave principal reservada en los [cuadros de diálogo](dialog-boxes.md). Tenga en cuenta que el nombre del cuadro de diálogo de clave principal solo está reservado por el instalador y no hay ninguna implementación específica del cuadro de diálogo en Windows Instalador. Los autores de paquetes deben rellenar todos los campos de la base de datos que especifican los atributos y controles de estos cuadros de diálogo reservados.

 

 
