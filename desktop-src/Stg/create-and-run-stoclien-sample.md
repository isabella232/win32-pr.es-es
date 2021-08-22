---
title: Creación y ejecución de un ejemplo de StoClien
description: StoClien trabaja en cooperación con un objeto COPaper en un servidor COM para lograr el almacenamiento persistente de dibujos en archivos compuestos COM.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Creación y ejecución de un ejemplo de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3d9526e81fc3fb2d6a0cfb03e8943ccf68688096588122da87861d8c88e531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663465"
---
# <a name="create-and-run-stoclien-sample"></a>Creación y ejecución de un ejemplo de StoClien

**StoClien trabaja** en cooperación con un objeto COPaper en un servidor COM para lograr el almacenamiento persistente de dibujos en archivos compuestos COM. Para obtener más información sobre el uso de secuencias de COPaper en el archivo compuesto proporcionado a COPaper por **StoClien,** vea [**Ejemplo de StoServe**](structured-storage-server-sample--stoserve-.md) y STOSERVE.HTM. La construcción de COPaper y su interfaz IPaper también se tratan en el **ejemplo de StoServe.**

## <a name="code-tour"></a>Paseo por el código

Los temas principales que se tratan en este paseo por el código son:

-   Cómo **encapsula CGuiPaper** el comportamiento de la GUI del papel de dibujo electrónico de **StoClien**
-   Captura y muestra la actividad de dibujo interactiva de **StoClien**
-   Cómo el **objeto CGuiPaper** usa COPaper para registrar datos de dibujo
-   Cómo se usa una conexión IPaperSink para volver a dibujar
-   Cómo los métodos CPapFile **Load** y **Save** usan el almacenamiento estructurado en archivos compuestos

Como la clase **CGuiBall** usada en los ejemplos FRECLIEN y CONCLIEN encapsulaba el comportamiento de una bola de peto, **StoClien** usa una clase **CGuiPaper** de C++ para encapsular los datos y el comportamiento de la GUI del papel de dibujo electrónico.

En la tabla siguiente se enumeran los archivos pertinentes al **ejemplo de StoClien.**



| Files        | Descripción                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Breve descripción de ejemplo.                                                                                                        |
| Makefile     | Archivo make genérico para compilar el ejemplo de código.                                                                               |
| STOCLIEN. H   | Archivo de include para la **aplicación StoClien.** Contiene declaraciones de clase, prototipos de función e identificadores de recursos.   |
| STOCLIEN. Cpp | Archivo de implementación principal para STOCLIEN.EXE. Tiene la implementación de WinMain y CMainWindow, así como el envío del menú principal. |
| STOCLIEN. Rc  | Archivo de definición de recursos de aplicación.                                                                                        |
| STOCLIEN. Ico | Recurso de icono de aplicación.                                                                                                   |
| STOCLIEN. Pap | Un archivo de dibujo en papel predeterminado para la aplicación.                                                                                |
| Lápiz. Cur   | Imagen de lápiz para el cursor de la ventana de cliente.                                                                                     |
| Fregadero. H       | Declaración de clase para la clase de objeto COM COPaperSink.                                                                      |
| Fregadero. Cpp     | Archivo de implementación para la clase de objeto COM COPaperSink.                                                                        |
| PAPFILE. H    | Declaración de clase para la **clase CPapFile** de C++.                                                                            |
| PAPFILE. Cpp  | Archivo de implementación de **la clase CPapFile** de C++.                                                                              |
| GUIPAPER. H   | Declaración de clase para la **clase CGuiPaper** de C++.                                                                           |
| GUIPAPER. Cpp | Archivo de implementación para **la clase CGuiPaper** de C++.                                                                             |
| STOCLIEN. Dsp | Microsoft Visual Studio Project archivo.                                                                                            |



 

## <a name="compound-files"></a>archivos compuestos

**StoClien se** basa en COPaper para registrar datos de dibujo. También se basa en COPaper para almacenar los datos en un archivo compuesto. Sin embargo, en una división típica del trabajo entre el cliente COM y el servidor, **StoClien** comparte parte de la responsabilidad del almacenamiento de archivos. Esta división del trabajo es importante en las aplicaciones COM, donde el cliente es un contenedor y el servidor es un objeto incrustado. En esta disposición, el cliente es responsable de crear o abrir un archivo de almacenamiento estructurado, mientras que el objeto de servidor es responsable de usar ese almacenamiento para sus propios fines de almacenamiento de datos. Esto puede implicar que el objeto de servidor cree subalmacenamientos en el almacenamiento que se le asigna. Normalmente implica que el objeto de servidor cree objetos de secuencia en el almacenamiento. El uso de coPaper de flujos de almacenamiento se detalla en el **ejemplo de StoClien.**

El cliente y el objeto de servidor usan la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para realizar operaciones de archivo. Se usa la implementación de archivos compuestos Storage arquitectura estructurada. Las funciones de servicio estándar se usan para las operaciones en archivos compuestos. Por ejemplo, la función [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) crea inicialmente un archivo compuesto y devuelve un **puntero IStorage** que se puede usar para manipular el archivo. Esta función determinada se llama en **StoClien.** La **interfaz IStorage** que obtiene se pasa como parámetro a COPaper para su uso. El objeto COPaper no crea ni abre archivos compuestos por sí mismo: usa las interfaces **IStorage** e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para trabajar en archivos compuestos que se le han dado.

Estas [**interfaces IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**e IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no se implementan en **StoClien** o **StoServe.** Se implementan dentro de las bibliotecas COM. Cuando se obtiene un puntero a una de estas interfaces, sus métodos se usan básicamente como un conjunto de servicios para operar en un archivo compuesto.

 

 




