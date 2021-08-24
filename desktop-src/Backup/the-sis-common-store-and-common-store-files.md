---
title: El almacén común de SIS y Common-Store archivos
description: Todos los archivos de copia de seguridad que mantiene la copia de seguridad del almacén de instancia única (SIS) se denominan archivos de almacenamiento común.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- copias de seguridad de almacenes comunes
- Copia de seguridad de un almacén de instancia única (SIS), almacenes comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19337a967fd858c149bc9d4261abc44214d4c76023abe022b5e1c5efd5f8ed3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529475"
---
# <a name="the-sis-common-store-and-common-store-files"></a>El almacén común de SIS y Common-Store archivos

Todos los archivos de copia de seguridad que mantiene la copia de seguridad del almacén de instancia única (SIS) se *denominan archivos de almacenamiento común.* Existe *un almacén común* en cada volumen mantenido por SIS y contiene todos los archivos de almacenamiento común que existen en ese volumen. Este directorio se encuentra en el directorio raíz del volumen y se denomina \\ "SIS Common Store". El almacén común se implementa como un directorio que está protegido contra el acceso de usuario normal, ya que los archivos de almacenamiento común están diseñados para que solo puedan acceder directamente las funciones de la API de copia de seguridad de SIS y no las aplicaciones de copia de seguridad y restauración.

Las propiedades de un archivo common-store son las siguientes:

-   Un archivo de almacén común puede tener uno o varios vínculos que apunten a él.
-   Una vez creado, el contenido de un archivo de common-store nunca cambia.
-   Los nombres de los archivos de almacenamiento común son únicos globalmente, es decir, son únicos en todos los volúmenes de todos los sistemas del mundo y el enlace entre un nombre de archivo de almacén común y sus datos es globalmente estático.

Cuando SIS está habilitado en un volumen, se crea una copia de los archivos duplicados en el almacén común y todos los archivos duplicados se reemplazan por [vínculos SIS](sis-links-and-reparse-points.md) que apuntan al archivo de almacenamiento común. Para más información, consulte [Habilitación o deshabilitación de SIS en un volumen en](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) la documentación de TechNet.

Cuando se tiene acceso a uno de los vínculos SIS para una operación de escritura, el filtro SIS restaura primero el contenido original del archivo de vínculo DE SIS desde el archivo de almacenamiento común, se quita el punto de análisis que vincula el archivo de vínculo SIS al almacén común y, a continuación, la operación de escritura se realiza en el archivo de destino original.

El archivo de almacenamiento común solo se quita cuando se elimina el último vínculo de SIS que apunta a él.

 

 