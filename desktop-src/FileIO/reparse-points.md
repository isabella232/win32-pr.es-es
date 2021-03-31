---
description: Describe los puntos de reanálisis.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Puntos de análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912098"
---
# <a name="reparse-points"></a>Puntos de análisis

Un archivo o directorio puede contener un *punto de reanálisis*, que es una colección de datos definidos por el usuario. El formato de estos datos lo entiende la aplicación que almacena los datos y un filtro del sistema de archivos que se instala para interpretar los datos y procesar el archivo. Cuando una aplicación establece un punto de reanálisis, almacena estos datos, además de una *etiqueta de reanálisis*, que identifica de forma única los datos que almacena. Cuando el sistema de archivos abre un archivo con un punto de reanálisis, intenta encontrar el filtro del sistema de archivos asociado con el formato de datos identificado por la etiqueta de reanálisis. Si se encuentra un filtro del sistema de archivos, el filtro procesa el archivo según lo indicado por los datos de reanálisis. Si no se encuentra un filtro del sistema de archivos, se producirá un error en la operación de apertura de archivo.

Por ejemplo, los puntos de análisis se utilizan para implementar vínculos del sistema de archivos NTFS y el servidor de almacenamiento remoto (RSS) de Microsoft. RSS usa un conjunto de reglas definido por el administrador para Desplace los archivos que se usan con poca frecuencia a un almacenamiento a largo plazo, como los medios ópticos o de cinta. Utiliza puntos de reanálisis para almacenar información sobre el archivo en el sistema de archivos. Esta información se almacena en un archivo de código auxiliar que contiene un punto de análisis cuyos datos apuntan al dispositivo en el que se encuentra ahora el archivo real. El filtro del sistema de archivos puede usar esta información para recuperar el archivo.

Los puntos de reanálisis también se usan para implementar carpetas montadas. Para obtener más información, vea [determinar si un directorio es una carpeta montada](determining-whether-a-directory-is-a-volume-mount-point.md).

Las restricciones siguientes se aplican a los puntos de reanálisis:

-   Se pueden establecer puntos de reanálisis para un directorio, pero el directorio debe estar vacío. De lo contrario, el sistema de archivos NTFS no puede establecer el punto de reanálisis. Además, no puede crear directorios o archivos en un directorio que contenga un punto de análisis.
-   Los puntos de reanálisis y los atributos extendidos son mutuamente excluyentes. El sistema de archivos NTFS no puede crear un punto de reanálisis cuando el archivo contiene atributos extendidos y no puede crear atributos extendidos en un archivo que contiene un punto de análisis.
-   Los datos de punto de reanálisis, incluida la etiqueta y el **GUID** opcional, no pueden superar los 16 kilobytes. No se puede establecer un punto de reanálisis si la cantidad de datos que se van a colocar en el punto de análisis supera este límite.
-   Hay un límite de 63 puntos de análisis en una ruta de acceso dada.

    **Windows Server 2003 y Windows XP:** Hay un límite de 31 puntos de análisis en una ruta de acceso dada.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etiquetas de punto de reanálisis](reparse-point-tags.md)<br/>                                 | Cada punto de reanálisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de reanálisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis.<br/> |
| [Operaciones de punto de análisis](reparse-point-operations.md)<br/>                     | Describe las operaciones de punto de reanálisis que se pueden realizar mediante [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).<br/>                                                                                       |
| [Puntos de análisis y operaciones de archivo](reparse-points-and-file-operations.md)<br/> | Describe cómo los puntos de reanálisis habilitan el comportamiento del sistema de archivos que se deriva del comportamiento que esperan la mayoría de los desarrolladores de Windows.<br/>                                                                                     |



 

 

