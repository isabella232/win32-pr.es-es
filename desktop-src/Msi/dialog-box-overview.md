---
description: El proceso de creación de un cuadro de diálogo en Windows Installer es similar al proceso de creación de un cuadro de diálogo mediante programación con una plantilla de cuadro de diálogo de la API de Microsoft Windows.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Información general del cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360866"
---
# <a name="dialog-box-overview"></a>Información general del cuadro de diálogo

El proceso de creación de un cuadro de diálogo en Windows Installer es similar al proceso de creación de un cuadro de diálogo mediante programación con una plantilla de cuadro de diálogo de la API de Microsoft Windows. Mientras que una plantilla de cuadro de diálogo de Windows se almacena en una cadena de caracteres terminada en null, Windows Installer almacena los parámetros del cuadro de diálogo en la tabla de diálogo. La tabla del cuadro de diálogo contiene una columna de atributos que es análoga a los estilos de ventana de la API de la interfaz de usuario de Microsoft Windows. Sin embargo, el número de bits de estilo de cuadro de diálogo de Windows Installer es un conjunto reducido y especializado.

Para crear físicamente el cuadro de diálogo mediante la API de la interfaz de usuario de Windows, se llama a [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) y pasa un puntero a la plantilla. En Windows Installer, el cuadro de diálogo se crea durante la ejecución de una de las tres tablas de secuencia de interfaz de usuario.

Windows Installer no contiene una interfaz de usuario predeterminada que los autores de paquetes pueden emplear para sus paquetes. Contiene un conjunto limitado de cuadros de diálogo predeterminados que muestran los mensajes de error y de información, pero solo se muestran si Windows Installer consulta las tablas de la secuencia de cuadros de diálogo y de la interfaz de usuario y detecta que no hay cuadros de diálogo personalizados disponibles.

El SDK del instalador incluye una base de datos mínima denominada Uisample.msi que contiene tablas de secuencia de ejecución y IU llenas y una interfaz de usuario completa. Esta base de datos se personaliza y combina con facilidad en cualquier paquete.

Algunas acciones estándar e internas Windows Installer condiciones de error devuelven un conjunto específico de datos de interfaz de usuario y, por tanto, requieren un cuadro de diálogo con un conjunto específico de controles para acomodar esos datos. Windows Installer comprueba dos ubicaciones independientes para los identificadores de estos cuadros de diálogo.

-   Windows Installer contiene un conjunto de nombres de cuadros de diálogo incrustados. La acción personalizada consulta en la tabla de diálogo los nombres reservados.
-   En cada una de las tres tablas de secuencias de la interfaz de usuario, los nombres de cuadro de diálogo con un número de secuencia de-1,-2 o-3 se muestran como respuesta a la salida, salida solicitada por el usuario y mensajes de error irrecuperables de Windows Installer.

En los [cuadros de diálogo](dialog-boxes.md)hay disponible una lista completa de los nombres de los cuadros de diálogo de clave principal reservados. Tenga en cuenta que el nombre del cuadro de diálogo de la clave principal solo está reservado por el instalador y no hay ninguna implementación específica del cuadro de diálogo en Windows Installer. Los autores de paquetes deben rellenar todos los campos de la base de datos que especifiquen los atributos y controles de estos cuadros de diálogo reservados.

 

 
