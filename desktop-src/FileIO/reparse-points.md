---
description: Describe los puntos de reanción.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Puntos de análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069860"
---
# <a name="reparse-points"></a>Puntos de análisis

Un archivo o directorio puede contener un *punto de análisis,* que es una colección de datos definidos por el usuario. El formato de estos datos lo entiende la aplicación que almacena los datos y un filtro del sistema de archivos, que se instala para interpretar los datos y procesar el archivo. Cuando una aplicación establece un punto de repetición de análisis, almacena estos datos, además de una etiqueta *de rean* aproximado , que identifica de forma única los datos que almacena. Cuando el sistema de archivos abre un archivo con un punto de análisis, intenta encontrar el filtro del sistema de archivos asociado al formato de datos identificado por la etiqueta de análisis. Si se encuentra un filtro del sistema de archivos, el filtro procesa el archivo según lo indicado por los datos de análisis. Si no se encuentra un filtro del sistema de archivos, se produce un error en la operación de apertura de archivos.

Por ejemplo, los puntos de análisis se usan para implementar vínculos del sistema de archivos NTFS y Microsoft Remote Storage Server (RSS). RSS usa un conjunto de reglas definido por el administrador para mover archivos usados con poca frecuencia al almacenamiento a largo plazo, como cinta o medios ópticos. Usa puntos de análisis para almacenar información sobre el archivo en el sistema de archivos. Esta información se almacena en un archivo de código auxiliar que contiene un punto de análisis de análisis cuyos datos apuntan al dispositivo donde se encuentra ahora el archivo real. El filtro del sistema de archivos puede usar esta información para recuperar el archivo.

Los puntos de reanción también se usan para implementar carpetas montadas. Para obtener más información, vea [Determinar si un directorio es una carpeta montada.](determining-whether-a-directory-is-a-volume-mount-point.md)

Las restricciones siguientes se aplican a los puntos de reanualizado:

-   Se pueden establecer puntos de reanción para un directorio, pero el directorio debe estar vacío. De lo contrario, el sistema de archivos NTFS no puede establecer el punto de análisis. Además, no puede crear directorios o archivos en un directorio que contenga un punto de reandición.
-   Los puntos de reanúse y los atributos extendidos son mutuamente excluyentes. El sistema de archivos NTFS no puede crear un punto de análisis cuando el archivo contiene atributos extendidos y no puede crear atributos extendidos en un archivo que contiene un punto de análisis.
-   Los datos de punto de análisis, incluida la etiqueta y el **GUID opcional,** no pueden superar los 16 kilobytes. Se produce un error al establecer un punto de repetición de análisis si la cantidad de datos que se colocarán en el punto de análisis supera este límite.
-   Hay un límite de 63 puntos de rean aproximado en cualquier ruta de acceso determinada.

    **Windows Server 2003 y Windows XP:** Hay un límite de 31 puntos de rean aproximado en cualquier ruta de acceso determinada.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Etiquetas de punto de reanción](reparse-point-tags.md)<br/>                                 | Cada punto de análisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de análisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis de análisis.<br/> |
| [Operaciones de punto de reanción](reparse-point-operations.md)<br/>                     | Describe las operaciones de punto de análisis que puede realizar mediante [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).<br/>                                                                                       |
| [Análisis de puntos y operaciones de archivo](reparse-points-and-file-operations.md)<br/> | Describe cómo los puntos de análisis permiten el comportamiento del sistema de archivos que se aleja del comportamiento que la mayoría Windows los desarrolladores esperan.<br/>                                                                                     |



 

 

