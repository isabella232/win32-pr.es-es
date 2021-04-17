---
title: Cómo usan las herramientas de desarrolladores las bibliotecas de tipos
description: Cómo usan las herramientas de desarrolladores las bibliotecas de tipos
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105717321"
---
# <a name="how-developer-tools-use-type-libraries"></a>Cómo usan las herramientas de desarrolladores las bibliotecas de tipos

En el diagrama siguiente se muestra cómo interactúan las diversas herramientas de desarrollo con la biblioteca de tipos de un objeto COM. Cada biblioteca de tipos expone interfaces de programación estándar que las herramientas pueden llamar para obtener información sobre los elementos descritos en esa biblioteca de tipos. En este diagrama, GUID representa el identificador único global y la RPC para la llamada a procedimiento remoto.

![Diagrama que muestra cómo las herramientas de desarrollo interactúan con la biblioteca de tipos de un objeto de C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

En el diagrama anterior, las herramientas de conversión de C++, como el compilador MIDL y los asistentes proporcionados por el sistema de desarrollo de Microsoft Visual C++, generan archivos de encabezado y de código auxiliar. Puede agregar estos archivos al proyecto para usar el objeto COM descrito por la biblioteca de tipos.

Del mismo modo, en Java las herramientas de desarrollo generan archivos de código fuente y de clase Java, que luego puede importar en la aplicación.

En Visual Basic, el escenario es algo más sencillo. No es necesario generar archivos adicionales. El entorno de Visual Basic proporciona cuadros de diálogo que enumeran los objetos COM actualmente instalados en el equipo. Seleccione el componente al que desea llamar desde la aplicación y se agrega al proyecto, ya sea como un componente o como una referencia.

El visor OLE-COM Lee una biblioteca de tipos, genera un archivo IDL temporal basado en la biblioteca de tipos y lo muestra a los usuarios. El visor OLE-COM también muestra la sintaxis de C++ para los elementos COM enumerados en la biblioteca de tipos.

Para obtener más información sobre las bibliotecas de tipos, vea [bibliotecas de tipos y lenguaje de descripción de objetos](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 