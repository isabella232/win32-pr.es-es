---
description: Cuando se realiza una operación de copia de seguridad de VSS sin la intervención de un escritor, todavía puede producirse la creación de instantáneas.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Copias de seguridad sin participación del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bd1d402b53c48fd82085110e4d58600c92fbdd72defc47dee326c8fa1d4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248285"
---
# <a name="backups-without-writer-participation"></a>Copias de seguridad sin participación del escritor

Cuando se realiza una operación de copia de seguridad de VSS sin la intervención de un escritor, todavía puede producirse la creación de instantáneas.

Como se indicó en otra parte (consulte Estado predeterminado de la [instantánea),](shadow-copies-and-shadow-copy-sets.md)el resultado de este tipo de instantánea es un volumen que refleja el estado de un disco en el momento de la instantánea: los datos del volumen de instantáneas pueden reflejar operaciones de E/S incompletas o parciales y se describen como en un estado coherente con bloqueos. [](vssgloss-c.md)

Hay varias situaciones que requerirán que una aplicación de copia de seguridad funcione con datos copiados en la sombra coherentes con bloqueos:

-   **Los datos se administran mediante aplicaciones que no son conscientes de VSS**

    Casi todos los sistemas tendrán algunas aplicaciones (editores de texto, lectores de correo electrónico, procesadores de palabras, etc.) que no son conscientes de VSS, por lo que siempre es probable que algunos de los datos de una instantánea deba tenerse en cuenta como en un estado coherente frente a bloqueos.

    Este tipo de datos no suele ser crítico para el sistema o el servicio, por lo que la copia de seguridad no debería ser problemática o, al menos, no ser más problemática que durante una copia de seguridad convencional.

    Al igual que con los preparativos para las copias de seguridad convencionales, si es posible, los operadores de copia de seguridad deben intentar suspender o finalizar dichas aplicaciones antes de iniciar un trabajo de copia de seguridad de VSS.

-   **Sistema sin escritores compatibles con VSS**

    Esta situación puede ser relativamente poco frecuente porque la mayoría de los sistemas de los que se puede hacer una copia de seguridad mediante una aplicación de copia de seguridad de VSS tendrán una versión habilitada para VSS de Windows, que debe contener escritores.

    Sin embargo, hay ciertas circunstancias en las que podría surgir este problema, por ejemplo, si va a hacer una copia de seguridad de un sistema sin compatibilidad con VSS, pero el sistema usa un dispositivo en red habilitado para VSS para su almacenamiento.

    Aunque la copia de seguridad del estado de un sistema a partir de una imagen coherente con los bloqueos no es óptima, puede ser suficiente para que un equipo se reinicie a un estado operativo. En muchos casos, el equipo se recuperará de las operaciones de E/S incompletas en los sistemas de archivos y funcionará con normalidad.

-   **Un solicitante que decide no trabajar con los escritores del sistema**

    Esta circunstancia se produciría si un solicitante decide agregar ningún componente de escritor o deshabilitar todos los escritores.

    Por lo general, no se recomienda realizar copias de seguridad de esta manera. Aunque el volumen de instantáneas del que se va a realizar una copia de seguridad puede ser suficiente para restaurar un sistema a en ejecución, no es deseable. De hecho, dado que los escritores que se ejecutan en el sistema están diseñados con funcionalidad para colaborar con VSS y instantáneas, la copia de seguridad de sus datos de esta manera podría provocar inestabilidad.

 

 



