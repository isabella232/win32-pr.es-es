---
title: Desarrollo de la interfaz
description: Una interfaz RPC describe las funciones remotas que implementa el programa de servidor.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- RPC llamada a procedimiento remoto, tareas, desarrollar la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b6f720bcd492e784ad07fe20e221ac54951680
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149503"
---
# <a name="developing-the-interface"></a>Desarrollo de la interfaz

Una interfaz RPC describe las funciones remotas que implementa el programa de servidor. La interfaz garantiza que el cliente y el servidor se comunican con las mismas reglas cuando el cliente invoca un procedimiento remoto que ofrece el servidor. Una interfaz está formada por un nombre de interfaz, algunos atributos, definiciones de tipo opcional o constantes y un conjunto de declaraciones de procedimiento. Cada declaración de procedimiento debe contener un nombre de procedimiento, el tipo de valor devuelto y la lista de parámetros.

Las interfaces se definen en el Lenguaje de definición de interfaz de Microsoft (MIDL). Si está familiarizado con C o C++, las definiciones de la interfaz MIDL serán bastante sencillas. MIDL es similar a C y C++ en muchos sentidos.

Al desarrollar una aplicación RPC, se usa un editor de texto para definir la interfaz y almacenarla en un archivo de texto con una extensión. idl. Para obtener más información, vea [los archivos IDL y ACF](the-idl-and-acf-files.md). El compilador MIDL genera un archivo de encabezado que el programa incluye en los archivos de origen del cliente y del servidor. El compilador MIDL también genera dos archivos de código fuente de C. Puede compilar y vincular uno de ellos al programa cliente y el otro al programa de servidor. Estos dos archivos de código fuente de C son el código auxiliar de cliente y de servidor. Para obtener información general sobre el cliente y el código auxiliar del servidor, consulte [Cómo funciona RPC](how-rpc-works.md). Para obtener información general sobre el compilador MIDL, vea [compilar un archivo MIDL](using-midl.md).

De forma predeterminada, el código auxiliar del cliente y del servidor tienen el mismo nombre, lo que puede causar problemas si el cliente se vincula con el código auxiliar del servidor, o viceversa. El uso de la opción [**/prefix**](/windows/desktop/Midl/-prefix) de MIDL evita que se produzca este error común.

En la ilustración siguiente se muestra el proceso de creación de una interfaz.

![la creación de códigos auxiliares de cliente y servidor con la opción/prefix evita problemas de compilación accidental](images/idldev.png)

También es posible que también necesite especificar un archivo de configuración de la aplicación (ACF) para la entrada en el compilador de MIDL. Para obtener más información sobre los archivos de configuración de la aplicación, vea [los archivos IDL y ACF](the-idl-and-acf-files.md).

Además del compilador de MIDL, normalmente tendrá que usar la utilidad uuidgen para generar un identificador único universal (UUID, intercambiable con el término GUID). En esta sección se ofrece información sobre ambas herramientas, dividida en los temas siguientes:

-   [Generando interfaz UUID](generating-interface-uuids.md)
-   [Usar MIDL](using-midl.md)

 

 