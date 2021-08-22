---
title: Desarrollo de la interfaz
description: Una interfaz RPC describe las funciones remotas que implementa el programa de servidor.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- Llamada a procedimiento remoto RPC, tareas, desarrollo de la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23829dcf143f63e791984e51194686d193d69cd575fadbc0e29c13a6f2279df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930615"
---
# <a name="developing-the-interface"></a>Desarrollo de la interfaz

Una interfaz RPC describe las funciones remotas que implementa el programa de servidor. La interfaz garantiza que el cliente y el servidor se comuniquen con las mismas reglas cuando el cliente invoca un procedimiento remoto que ofrece el servidor. Una interfaz consta de un nombre de interfaz, algunos atributos, definiciones opcionales de tipo o constante y un conjunto de declaraciones de procedimiento. Cada declaración de procedimiento debe contener un nombre de procedimiento, un tipo de valor devuelto y una lista de parámetros.

Las interfaces se definen en el Lenguaje de definición de interfaz de Microsoft (MIDL). Si está familiarizado con C o C++, las definiciones de la interfaz MIDL parecerán bastante sencillas. MIDL se parece a C y C++ de muchas maneras.

Al desarrollar una aplicación RPC, se usa un editor de texto para definir la interfaz y almacenarla en un archivo de texto con una extensión .idl. Para obtener más información, [vea The IDL and ACF Files](the-idl-and-acf-files.md). El compilador MIDL genera un archivo de encabezado que el programa incluye en los archivos de origen de cliente y servidor. El compilador MIDL también genera dos archivos de código fuente de C. Compile y vincule uno de ellos al programa cliente y el otro al programa de servidor. Estos dos archivos de código fuente de C son los códigos auxiliares de cliente y servidor. Para obtener información general sobre los códigos auxiliares de cliente y servidor, vea [Funcionamiento de RPC.](how-rpc-works.md) Para obtener información general sobre el compilador midl, [vea Compilar un archivo MIDL](using-midl.md).

De forma predeterminada, el código auxiliar de cliente y servidor tiene el mismo nombre, lo que puede causar problemas si el cliente se vincula con el código auxiliar del servidor, o viceversa. El uso de la opción [**MIDL /prefix**](/windows/desktop/Midl/-prefix) evita que se produzca este error común.

En la ilustración siguiente se muestra el proceso de creación de una interfaz.

![La creación de código auxiliar de cliente y servidor con la opción /prefix evita problemas de compilación accidentales](images/idldev.png)

Es posible que también tenga que especificar un archivo de configuración de aplicación (ACF) para la entrada al compilador MIDL. Para obtener más información sobre los archivos de configuración de la aplicación, [vea The IDL and ACF Files](the-idl-and-acf-files.md).

Además del compilador MIDL, normalmente deberá usar la utilidad Uuidgen para generar un identificador único universal (UUID, intercambiable con el término GUID). En esta sección se presenta información sobre ambas herramientas, dividida en los temas siguientes:

-   [Generación de UUID de interfaz](generating-interface-uuids.md)
-   [Uso de MIDL](using-midl.md)

 

 