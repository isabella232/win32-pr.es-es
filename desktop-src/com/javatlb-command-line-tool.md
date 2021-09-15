---
title: Herramienta de Command-Line JavaTLB
description: Herramienta de Command-Line JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570997"
---
# <a name="javatlb-command-line-tool"></a>Herramienta de Command-Line JavaTLB

JavaTLB es un componente de Visual J++ 5.0. JavaTLB es una aplicación de línea de comandos que genera archivos de clase para un objeto COM. Los métodos que contienen tipos de datos que no se pueden representar de forma precisa y segura en Java no se convierten.

A diferencia [del Asistente para biblioteca de tipos de Java,](java-type-library-wizard.md)JavaTLB no genera un archivo de resumen que contenga la información de la biblioteca de tipos de Java.

Para generar archivos de clase Java para un único objeto COM, desde el símbolo del sistema ejecute:

**nombre de archivo de javatlb** 

donde *filename* es el nombre del archivo que contiene la biblioteca de tipos. Este archivo puede tener cualquiera de las siguientes extensiones de nombre de archivo: .tlb, .olb, .ocx, .dll o .exe.

Para generar archivos de clase Java para varios objetos COM, desde el símbolo del sistema, ejecute:

**javatlb @**_TextFile_

donde *TextFile* es el nombre de un archivo de texto que contiene una lista de los archivos que contienen las bibliotecas de tipos del objeto COM.

> [!Note]  
> En Visual J++ 6.0, la herramienta de línea de comandos de JavaTLB se reemplaza por la [herramienta JActiveX](jactivex-command-line-tool.md). Para obtener más información, vea la documentación de Visual J++ 6.0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a Java](translating-to-java.md)
</dt> </dl>

 

 




