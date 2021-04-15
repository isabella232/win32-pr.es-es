---
description: El componente principal de la interfaz de impresión es el administrador de trabajos de impresión.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Administrador de trabajos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcc6ea2e46c06b5e51032a4c43f46df7f07c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545590"
---
# <a name="print-spooler"></a>Administrador de trabajos de impresión

El componente principal de la interfaz de impresión es el administrador de trabajos de impresión. El administrador de trabajos de impresión es un archivo ejecutable que administra el proceso de impresión. La administración de la impresión implica la recuperación de la ubicación del controlador de impresora correcto, la carga del controlador, la puesta en cola de las llamadas de función de alto nivel en un trabajo de impresión, la programación del trabajo de impresión para la impresión, etc. El administrador de trabajos de impresión se carga durante el inicio del sistema y continúa ejecutándose hasta que se apaga el sistema operativo.

Las aplicaciones que imprimen crean un contexto de dispositivo de impresora (DC). Cuando una aplicación crea un controlador de dominio de impresora, el administrador de trabajos de impresión realiza las tareas necesarias, como determinar la ubicación del controlador de impresora necesario y, a continuación, cargar ese controlador. El administrador de trabajos de impresión también determina el tipo de datos utilizado para registrar el trabajo de impresión.

El administrador de trabajos de impresión admite los siguientes tipos de datos:

-   Metarchivo mejorado (EMF).
-   Texto ASCII.
-   Datos sin procesar, que incluyen tipos de datos de impresora como PostScript, PCL y tipos de datos personalizados.

Se pueden agregar tipos de datos personalizados a la cola de impresión mediante la instalación de controladores de impresora y procesadores de impresión adicionales. Un trabajo de impresión es un documento almacenado internamente y codificado mediante uno de los tipos de datos admitidos, y un trabajo de impresión puede contener una o varias páginas de salida. El trabajo de impresión puede constar de varias formas; por ejemplo, un trabajo puede constar de un sobre y tres páginas de papel A4. Las funciones [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) definen (o entre corchetes) un trabajo de impresión.

El tipo de datos predeterminado para un trabajo de impresión es el metarchivo mejorado. Un registro EMF es una estructura compacta que se usa para almacenar comandos de salida de texto, comandos de gráficos de tramas, etc. Cuando una aplicación llama a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca), el administrador de trabajos de impresión crea un archivo de cola de impresión y un archivo de datos y comienza a almacenar los registros EMF en el archivo de cola. Cada vez que la aplicación llama a una de las funciones de dibujo de GDI, se crean uno o más registros EMF nuevos y se almacenan en el archivo de cola. Los archivos de datos y de cola se crean en un directorio de sistema operativo. El administrador de trabajos de impresión utiliza el archivo de cola para almacenar los registros EMF y usa el archivo de datos para registrar el tipo de formulario, el tipo de datos para el trabajo de impresión, la impresora de destino, etc. El administrador de trabajos de impresión elimina estos archivos cuando el trabajo se ha impreso correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metaarchivos con formato mejorado](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
