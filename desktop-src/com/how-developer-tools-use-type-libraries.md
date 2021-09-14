---
title: Cómo usan las herramientas de desarrolladores las bibliotecas de tipos
description: Cómo usan las herramientas de desarrolladores las bibliotecas de tipos
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973626"
---
# <a name="how-developer-tools-use-type-libraries"></a>Cómo usan las herramientas de desarrolladores las bibliotecas de tipos

En el diagrama siguiente se muestra cómo interactúan las distintas herramientas de desarrollo con la biblioteca de tipos de un objeto COM. Cada biblioteca de tipos expone interfaces de programación estándar a las que las herramientas pueden llamar para obtener información sobre los elementos descritos en esa biblioteca de tipos. En este diagrama, GUID representa el identificador único global y RPC para la llamada a procedimiento remoto.

![Diagrama que muestra cómo interactúan las herramientas de desarrollo con la biblioteca de tipos de un objeto de C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

En el diagrama anterior, las herramientas de conversión de C++, como el compilador MIDL y los asistentes proporcionados por el sistema de desarrollo de Microsoft Visual C++, generan archivos de encabezado y código auxiliar. Puede agregar estos archivos al proyecto para usar el objeto COM descrito por la biblioteca de tipos.

De forma similar, en Java, las herramientas de desarrollo generan archivos de clase y código fuente de Java, que luego se pueden importar en la aplicación.

En Visual Basic, el escenario es algo más sencillo. No es necesario generar archivos adicionales. El Visual Basic proporciona cuadros de diálogo que enumeran los objetos COM instalados actualmente en el equipo. Seleccione el componente al que desea llamar desde la aplicación y se agrega al proyecto, ya sea como componente o como referencia.

El visor OLE-COM lee una biblioteca de tipos, genera un archivo IDL temporal basado en la biblioteca de tipos y lo muestra a los usuarios. El visor OLE-COM también muestra la sintaxis de C++ para los elementos COM enumerados en la biblioteca de tipos.

Para obtener más información sobre las bibliotecas de tipos, vea [Bibliotecas de tipos y el lenguaje de descripción de objetos](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 