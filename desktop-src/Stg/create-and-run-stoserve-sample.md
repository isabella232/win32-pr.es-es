---
title: Crear y ejecutar el ejemplo StoServe
description: El ejemplo de cliente y otros ejemplos relacionados deben compilarse antes de poder ejecutar el cliente.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665633"
---
# <a name="create-and-run-stoserve-sample"></a>Crear y ejecutar el ejemplo StoServe

El ejemplo de cliente y otros ejemplos relacionados deben compilarse antes de poder ejecutar el cliente. Para obtener más información sobre la creación de los ejemplos, vea [Cómo crear ejemplos](how-to-build-samples.md). Si ya ha creado los ejemplos adecuados, STOCLIEN.EXE es el ejecutable de cliente que se ejecutará para el ejemplo **StoServe** .

## <a name="code-tour"></a>Paseo por código

En la tabla siguiente se enumeran los archivos pertinentes para el ejemplo **StoServe** .



| Archivos        | Descripción                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| STOSERVE.TXT | Breve descripción del ejemplo                                                                                                  |
| MAKE     | El archivo make genérico para generar el STOSERVE.DLL ejemplo de código de esta lección.                                            |
| STOSERVE. C   | Archivo de inclusión para declarar como importado o que define como exportado las funciones de servicio en STOSERVE.DLL.                 |
| STOSERVE. CPP | El archivo de implementación principal para STOSERVE.DLL. Tiene DllMain y las funciones de servidor COM (por ejemplo, DllGetClassObject). |
| STOSERVE. DEF | Archivo de definición de módulo. Exporta las funciones de alojamiento de servidor.                                                             |
| STOSERVE. CR  | El archivo de definición de recursos DLL para el ejecutable.                                                                      |
| STOSERVE. ICO | El recurso de icono para el ejecutable.                                                                                     |
| Servidor. C     | Archivo de inclusión para el objeto de C++ de control de servidor.                                                                       |
| Servidor. CPP   | El archivo de implementación para el objeto de C++ de control de servidor.                                                                |
| Factory. C    | Archivo de inclusión de los objetos COM del generador de clases del servidor.                                                              |
| Factory. CPP  | El archivo de implementación para los generadores de clases del servidor.                                                                 |
| Conéctelo. C    | Archivo de inclusión para las clases de enumerador de punto de conexión, punto de conexión y enumerador de conexión.                |
| Conéctelo. CPP  | El archivo de implementación para el enumerador de puntos de conexión, el punto de conexión y los objetos de enumerador de conexión.         |
| Papel. C      | Archivo de inclusión de la clase de objeto COM de copaper.                                                                        |
| Papel. CPP    | El archivo de implementación para la clase de objeto COM de copaper y los puntos de conexión.                                       |
| STOSERVE. DSP | Microsoft Visual Studio archivo de proyecto.                                                                                     |



 

Los temas principales que se tratan en este tutorial de código son:

-   Los métodos de la interfaz [**IPaper**](ipaper-methods.md) .
-   El uso del copaper de la interfaz [**IPaperSink**](ipapersink-methods.md) para las notificaciones de cliente.
-   [**Estructuras**](structures---stoserve.md) en StoServe.
-   [Consideraciones de Unicode](unicode-considerations.md).

 

 




