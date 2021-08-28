---
title: Visores de biblioteca de tipos y herramientas de conversión
description: Visores de biblioteca de tipos y herramientas de conversión
ms.assetid: 35c29e2c-3ee3-4e73-b925-6aa0ccb50a00
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b0687769367edad4fd1c7325be943dfae74aae643789791396089cd6c6ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309011"
---
# <a name="type-library-viewers-and-conversion-tools"></a>Visores de biblioteca de tipos y herramientas de conversión

Las bibliotecas de tipos contienen la especificación de uno o varios elementos COM, incluidas clases, interfaces, enumeraciones, etc. Estos archivos se almacenan en un formato binario estándar. Una biblioteca de tipos puede ser un archivo independiente con la extensión de nombre de archivo .tlb, o puede almacenarse como un recurso en un archivo ejecutable, que puede tener una extensión de nombre de archivo .ocx, .dll o .exe. Los visores de bibliotecas de tipos y las herramientas de conversión que se describen a continuación leen este formato para obtener información sobre los elementos COM de la biblioteca.

Para poder programar un objeto en un lenguaje de programación determinado, debe poder ver su biblioteca de tipos en ese lenguaje. Esto proporciona la sintaxis adecuada para las clases, interfaces, métodos, propiedades y eventos del objeto COM.

Los productos de desarrollo de Microsoft proporcionan las siguientes herramientas que puede usar para generar, extraer y ver información de la biblioteca de tipos.

## <a name="c"></a>C++

-   [Visor de objetos OLE-COM](ole-com-object-viewer.md)
-   [Compilador midl](midl-compiler.md)
-   [MkTypLib](mktyplib-command-line-tool.md)

## <a name="visual-basic"></a>Visual Basic

-   [Visual Basic Explorador de objetos](visual-basic-object-browser.md)

## <a name="java"></a>Java

-   [JActiveX](jactivex-command-line-tool.md)
-   [Asistente para biblioteca de tipos de Java](java-type-library-wizard.md)
-   [JavaTLB](javatlb-command-line-tool.md)

Para obtener información general sobre cómo interactúan estas herramientas con las bibliotecas de tipos, vea [How Herramientas de desarrollo Use Type Libraries](how-developer-tools-use-type-libraries.md).

 

 




