---
description: Cuando se realiza una operación de copia de seguridad de VSS sin la implicación de un escritor, todavía se puede producir la creación de la instantánea.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Copias de seguridad sin participación del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653046"
---
# <a name="backups-without-writer-participation"></a>Copias de seguridad sin participación del escritor

Cuando se realiza una operación de copia de seguridad de VSS sin la implicación de un escritor, todavía se puede producir la creación de la instantánea.

Como se indicó en otra parte (vea el estado de la [instantánea predeterminada](shadow-copies-and-shadow-copy-sets.md)), el resultado de este tipo de instantánea es un volumen que refleja el estado de un disco en el momento de la instantánea: los datos del volumen de copia sombra pueden reflejar operaciones de e/s parciales o incompletas y se describe como si estuvieran en un [*Estado de bloqueo coherente*](vssgloss-c.md).

Hay varias situaciones que requerirán que una aplicación de copia de seguridad funcione con datos de instantáneas coherentes de bloqueos:

-   **Los datos están administrados por aplicaciones que no reconocen VSS**

    Casi todos los sistemas tendrán algunas aplicaciones (editores de texto, lectores de correo, procesadores de palabras, etc.) que no reconocen VSS, por lo que siempre es probable que algunos de los datos de una instantánea tengan que considerarse como si estuvieran en un estado coherente con el bloqueo.

    Este tipo de datos no suele ser crítico para el sistema o el servicio, por lo que realizar una copia de seguridad no debe ser problemático o, al menos, no ser problemático que durante una copia de seguridad convencional.

    Al igual que con los preparativos de las copias de seguridad convencionales, si es posible, los operadores de copia de seguridad deben intentar suspender o finalizar dichas aplicaciones antes de iniciar un trabajo de copia de seguridad de VSS.

-   **Sistema sin escritores compatibles con VSS**

    Esta situación puede ser relativamente poco frecuente, porque la mayoría de los sistemas de los que una aplicación de copia de seguridad de VSS puede realizar la copia de seguridad tendrá una versión habilitada para VSS de Windows, que debe contener escritores.

    Sin embargo, hay ciertas circunstancias en las que puede surgir este problema, por ejemplo, si se realiza una copia de seguridad de un sistema sin compatibilidad con VSS, pero el sistema usa un dispositivo en red habilitado para VSS para su almacenamiento.

    Aunque la copia de seguridad del estado de un sistema desde una imagen coherente con bloqueos no es óptima, puede ser suficiente para que un equipo se reinicie en un estado operativo. En muchos casos, el equipo se recuperará de las operaciones de e/s incompletas en los sistemas de archivos y funcionará con normalidad.

-   **Un solicitante que elige no trabajar con los escritores del sistema**

    Esta circunstancia se produciría si un solicitante decidió no agregar ningún componente de escritura o deshabilitar todos los escritores.

    En general, no se recomienda realizar copias de seguridad de esta manera. Aunque el volumen de copia sombra del que se va a realizar la copia de seguridad puede ser suficiente para restaurar un sistema en ejecución, no es deseable. De hecho, dado que los escritores que se ejecutan en el sistema están diseñados con funcionalidad para cooperar con VSS e instantáneas, la realización de copias de seguridad de los datos de esta manera podría provocar inestabilidad.

 

 



