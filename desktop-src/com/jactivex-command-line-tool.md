---
title: Herramienta de Command-Line JActiveX
description: La aplicación de línea de comandos JActiveX es un componente de Visual J++ 6,0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9975e060a3967f927440111719045378aa812f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714257"
---
# <a name="jactivex-command-line-tool"></a>Herramienta de Command-Line JActiveX

La aplicación de línea de comandos JActiveX es un componente de Visual J++ 6,0. Lee la biblioteca de tipos de un control ActiveX de Microsoft y genera los archivos de código fuente de Java correspondientes. Después, puede compilar estos archivos de origen e importarlos en la aplicación de Java.

Para generar archivos de código fuente de Java para un objeto COM, desde el símbolo del sistema, ejecute:

 *nombre de archivo* JActiveX

donde *filename* es el nombre del archivo que contiene la biblioteca de tipos. Este archivo puede tener cualquiera de las siguientes extensiones de nombre de archivo:. tlb,. olb,. ocx,. dll o. exe.

Para obtener más información sobre los parámetros opcionales que se pueden establecer en JActiveX, vea la documentación de Visual J++ o escriba la siguiente línea de comandos:

**JActiveX/?**

> [!WARNING]
> No utilice compiladores de Visual J++ anteriores a la versión 1.02.3920 para compilar los archivos generados por JActiveX.exe. Esto se debe a que los archivos de código fuente generados se deben compilar con un @com-aware compilador. Solo los compiladores de Visual J++ posteriores a la versión 1.02.3920 son @com-aware .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a Java](translating-to-java.md)
</dt> </dl>

 

 




