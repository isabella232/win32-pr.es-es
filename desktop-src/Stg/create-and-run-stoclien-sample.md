---
title: Crear y ejecutar el ejemplo StoClien
description: StoClien funciona en cooperación con un objeto de copapeles en un servidor COM para lograr un almacenamiento persistente de dibujos en archivos compuestos COM.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Crear y ejecutar el ejemplo StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f00274293c05e21e660dc8e9448ca95946cab8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665634"
---
# <a name="create-and-run-stoclien-sample"></a>Crear y ejecutar el ejemplo StoClien

**StoClien** funciona en cooperación con un objeto de copapeles en un servidor com para lograr un almacenamiento persistente de dibujos en archivos compuestos com. Para obtener más información sobre el uso de las secuencias en el archivo compuesto proporcionado al copaper por **StoClien**, vea ejemplo [**StoServe**](structured-storage-server-sample--stoserve-.md) y STOSERVE.HTM. La construcción del copaper y su interfaz IPaper también se incluyen en el ejemplo **StoServe** .

## <a name="code-tour"></a>Paseo por código

Los temas principales que se tratan en este tutorial de código son:

-   Cómo encapsula **CGuiPaper** el comportamiento de la GUI del papel de dibujo electrónico de **StoClien**
-   Cómo captura **StoClien** y muestra la actividad de dibujo interactivo
-   Cómo usa el objeto **CGuiPaper** el copaper para grabar datos de dibujo
-   Cómo se usa una conexión IPaperSink en la repintado
-   Cómo los métodos **Load** y **Save** de CPapFile usan el almacenamiento estructurado en archivos compuestos

Como la clase **CGuiBall** que se usa en los ejemplos FRECLIEN y CONCLIEN encapsulado el comportamiento de una bola de rebote, **StoClien** usa una clase de **CGuiPaper** C++ para encapsular los datos y el comportamiento de la GUI del papel de dibujo electrónico.

En la tabla siguiente se enumeran los archivos pertinentes para el ejemplo **StoClien** .



| Archivos        | Descripción                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Breve descripción del ejemplo.                                                                                                        |
| MAKE     | El archivo make genérico para compilar el ejemplo de código.                                                                               |
| STOCLIEN. C   | El archivo de inclusión de la aplicación **StoClien** . Contiene declaraciones de clase, prototipos de función e identificadores de recursos.   |
| STOCLIEN. CPP | El archivo de implementación principal para STOCLIEN.EXE. Tiene la implementación de WinMain y CMainWindow, así como el menú principal de distribución. |
| STOCLIEN. CR  | El archivo de definición de recursos de la aplicación.                                                                                        |
| STOCLIEN. ICO | El recurso de icono de la aplicación.                                                                                                   |
| STOCLIEN. Papanicolau | Un archivo de dibujo de papel predeterminado para la aplicación.                                                                                |
| Lápiz. Espacia   | Una imagen de lápiz para el cursor de la ventana de cliente.                                                                                     |
| Receptor. C       | La declaración de clase para la clase de objeto COM COPaperSink.                                                                      |
| Receptor. CPP     | Archivo de implementación para la clase de objeto COM COPaperSink.                                                                        |
| PAPFILE. C    | La declaración de clase para la clase de C++ **CPapFile** .                                                                            |
| PAPFILE. CPP  | Archivo de implementación para la clase de C++ **CPapFile** .                                                                              |
| GUIPAPER. C   | La declaración de clase para la clase de C++ **CGuiPaper** .                                                                           |
| GUIPAPER. CPP | Archivo de implementación para la clase de C++ **CGuiPaper** .                                                                             |
| STOCLIEN. DSP | Microsoft Visual Studio archivo de proyecto.                                                                                            |



 

## <a name="compound-files"></a>archivos compuestos

**StoClien** se basa en el copapel para grabar datos de dibujo. También se basa en el copapel para almacenar los datos en un archivo compuesto. Sin embargo, en una división típica de trabajo entre el cliente y el servidor COM, **StoClien** comparte parte de la responsabilidad del almacenamiento de archivos. Esta división de trabajo es importante en las aplicaciones COM donde el cliente es un contenedor y el servidor es un objeto incrustado. En esta disposición, el cliente es responsable de crear o abrir un archivo de almacenamiento estructurado, mientras que el objeto de servidor es responsable de usar ese almacenamiento para sus propios fines de almacenamiento de datos. Esto puede implicar que el objeto de servidor cree subalmacenamientos en el almacenamiento que se le proporciona. Normalmente implica el objeto de servidor que crea los objetos de secuencia en el almacenamiento. El uso del copaper de flujos de almacenamiento se detalla en el ejemplo **StoClien** .

El cliente y el objeto de servidor usan la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para realizar operaciones de archivo. Se usa la implementación de archivos compuestos de la arquitectura de almacenamiento estructurado. Las funciones de servicio estándar se utilizan para las operaciones en archivos compuestos. Por ejemplo, la función [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) crea inicialmente un archivo compuesto y devuelve un puntero **IStorage** que se puede usar para manipular el archivo. Se llama a esta función concreta en **StoClien**. La interfaz **IStorage** que obtiene se pasa como un parámetro al copaper para su uso. El objeto de copaper no crea ni abre archivos compuestos por sí solo: usa las interfaces **IStorage** y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para trabajar en archivos compuestos que se le proporcionan.

Estas interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no se implementan dentro de **StoClien** o **StoServe**. Se implementan dentro de las bibliotecas COM. Cuando se obtiene un puntero a una de estas interfaces, los métodos se usan esencialmente como un conjunto de servicios para operar en un archivo compuesto.

 

 




