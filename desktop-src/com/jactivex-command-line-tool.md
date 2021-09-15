---
title: Herramienta de Command-Line JActiveX
description: La aplicación de línea de comandos JActiveX es un componente de Visual J++ 6.0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9975e060a3967f927440111719045378aa812f16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571008"
---
# <a name="jactivex-command-line-tool"></a>Herramienta de Command-Line JActiveX

La aplicación de línea de comandos JActiveX es un componente de Visual J++ 6.0. Lee la biblioteca de tipos de un control de ActiveX Microsoft y genera los archivos de código fuente de Java correspondientes. A continuación, puede compilar estos archivos de origen e importarlos en la aplicación Java.

Para generar archivos de origen de Java para un objeto COM, desde el símbolo del sistema, ejecute:

**nombre de archivo de jactivex** 

donde *filename* es el nombre del archivo que contiene la biblioteca de tipos. Este archivo puede tener cualquiera de las siguientes extensiones de nombre de archivo: .tlb, .olb, .ocx, .dll o .exe.

Para obtener más información sobre los parámetros opcionales que puede establecer en JActiveX, consulte la documentación de Visual J++ o escriba la siguiente línea de comandos:

**jactivex /?**

> [!WARNING]
> No use compiladores de Visual J++ anteriores a la versión 1.02.3920 para compilar los archivos generados por JActiveX.exe. Esto se debe a que los archivos de origen generados deben compilarse con un @com-aware compilador. Solo los compiladores de Visual J++ posteriores a la versión 1.02.3920 son @com-aware .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a Java](translating-to-java.md)
</dt> </dl>

 

 




