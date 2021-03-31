---
title: Herramienta de Command-Line de JavaTLB
description: Herramienta de Command-Line de JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779963"
---
# <a name="javatlb-command-line-tool"></a>Herramienta de Command-Line de JavaTLB

JavaTLB es un componente de Visual J++ 5,0. JavaTLB es una aplicación de línea de comandos que genera archivos de clase para un objeto COM. Los métodos que contienen tipos de datos que no se pueden representar con precisión y de forma segura en Java no se convierten.

A diferencia del [Asistente para la biblioteca de tipos de Java](java-type-library-wizard.md), JavaTLB no genera un archivo de resumen que contiene la información de la biblioteca de tipos de Java.

Para generar archivos de clase de Java para un único objeto COM, en el símbolo del sistema, ejecute:

 *nombre de archivo* JavaTLB

donde *filename* es el nombre del archivo que contiene la biblioteca de tipos. Este archivo puede tener cualquiera de las siguientes extensiones de nombre de archivo:. tlb,. olb,. ocx,. dll o. exe.

Para generar archivos de clase de Java para varios objetos COM, en el símbolo del sistema, ejecute:

**JavaTLB @ * * * TextFile*

donde *TextFile* es el nombre de un archivo de texto que contiene una lista de los archivos que contienen las bibliotecas de tipos del objeto com.

> [!Note]  
> En Visual J++ 6,0, la herramienta de línea de comandos JavaTLB se reemplaza por la [herramienta JActiveX](jactivex-command-line-tool.md). Para obtener más información, vea la documentación de Visual J++ 6,0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a Java](translating-to-java.md)
</dt> </dl>

 

 




