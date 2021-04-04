---
title: Los archivos de Common-Store y el almacén común de SIS
description: Todos los archivos de copia de seguridad mantenidos por la copia de seguridad del almacén de instancia única (SIS) se denominan archivos de almacenamiento común.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Copias de seguridad de almacenes comunes
- Copia de seguridad de almacenamiento de instancia única (SIS), almacenes comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904726"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Los archivos de Common-Store y el almacén común de SIS

Todos los archivos de copia de seguridad mantenidos por la copia de seguridad del almacén de instancia única (SIS) se denominan *archivos de almacenamiento común*. Existe un *almacén común* en cada volumen de mantenidos por sis y contiene todos los archivos de almacenamiento común que existen en ese volumen. Este directorio se encuentra en el directorio raíz del volumen y se denomina " \\ SIS Common Store". Common Store se implementa como un directorio protegido contra el acceso de usuario normal, ya que los archivos de almacenamiento común están pensados para que solo los puedan acceder directamente a las funciones de la API de copia de seguridad de SIS y no a las aplicaciones de copia de seguridad y restauración.

Las propiedades de un archivo de almacenamiento común son las siguientes:

-   Un archivo de almacenamiento común puede tener uno o varios vínculos que señalen a él.
-   Una vez creado, el contenido de un archivo de almacenamiento común nunca cambia.
-   Los nombres de los archivos de almacenamiento común son únicos globalmente, es decir, son únicos en todos los volúmenes en todos los sistemas del mundo, y el enlace entre un nombre de archivo de almacenamiento común y sus datos es globalmente estático.

Cuando SIS está habilitado en un volumen, se crea una copia de los archivos duplicados en el almacén común y todos los archivos duplicados se reemplazan por [vínculos de SIS](sis-links-and-reparse-points.md) que señalan al archivo de almacenamiento común. Para obtener más información, consulte [habilitar o deshabilitar SIS en un volumen](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) en la documentación de TechNet.

Cuando se tiene acceso a uno de los vínculos SIS para una operación de escritura, el filtro SIS restaura primero el contenido original del archivo de vínculo SIS del archivo Common-Store, se quita el punto de reanálisis que vincula el archivo de vínculo SIS al almacén común y, a continuación, se realiza la operación de escritura en el archivo de destino original.

El archivo Common-Store se quita solo cuando se elimina el último vínculo SIS que apunta a él.

 

 