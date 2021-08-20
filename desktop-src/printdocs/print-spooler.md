---
description: El componente principal de la interfaz de impresión es el administrador de trabajos de impresión.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Administrador de trabajos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bac19b44ebed5762abdb00b9ea044cf775a7a7ca8193c641709ad2c39436dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033933"
---
# <a name="print-spooler"></a>Administrador de trabajos de impresión

El componente principal de la interfaz de impresión es el administrador de trabajos de impresión. El cola de impresión es un archivo ejecutable que administra el proceso de impresión. La administración de la impresión implica recuperar la ubicación del controlador de impresora correcto, cargar ese controlador, colocar llamadas de función de alto nivel en un trabajo de impresión, programar el trabajo de impresión para imprimir, y así sucesivamente. El administrador de trabajos de cola se carga al iniciar el sistema y continúa en ejecución hasta que se apaga el sistema operativo.

Las aplicaciones que imprimen crean un contexto de dispositivo de impresora (DC). Cuando una aplicación crea un controlador de dominio de impresora, el administrador de trabajos realiza las tareas necesarias, como determinar la ubicación del controlador de impresora necesario y, a continuación, cargar ese controlador. El colador de impresión también determina el tipo de datos usado para registrar el trabajo de impresión.

El colador de impresión admite los siguientes tipos de datos:

-   Metarchivo mejorado (EMF).
-   Texto ASCII.
-   Datos sin procesar, que incluyen tipos de datos de impresora como PostScript, PCL y tipos de datos personalizados.

Los tipos de datos personalizados se pueden agregar al colador mediante la instalación de controladores de impresora adicionales y procesadores de impresión. Un trabajo de impresión es un documento almacenado internamente y codificado mediante uno de los tipos de datos admitidos, y un trabajo de impresión puede contener una o varias páginas de salida. El trabajo de impresión puede constar de varios formularios; Por ejemplo, un trabajo puede constar de un sobre y tres páginas de papel A4. Las funciones [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) definen (o entre corchetes) un trabajo de impresión.

El tipo de datos predeterminado para un trabajo de impresión es el metarchivo mejorado. Un registro EMF es una estructura compacta que se usa para almacenar comandos de salida de texto, comandos de gráficos de trama, y así sucesivamente. Cuando una aplicación llama a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca), el colador crea un archivo de cola y un archivo de datos y comienza a almacenar registros EMF en el archivo de cola. Cada vez que la aplicación llama a una de las funciones de dibujo de GDI, se crean y almacenan uno o varios registros EMF nuevos en el archivo de cola. Los archivos de datos y de cola se crean en un directorio de sistema operativo. El colador usa el archivo spool para almacenar registros EMF y usa el archivo de datos para registrar el tipo de formulario, el tipo de datos para el trabajo de impresión, la impresora de destino, y así sucesivamente. El colador elimina estos archivos cuando el trabajo se ha impreso correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metarchivos de formato mejorado](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
