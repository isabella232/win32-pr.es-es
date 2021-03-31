---
title: Consideraciones sobre la copia de seguridad de Active Directory Domain Services
description: Se pueden replicar los datos del servicio de directorio. Un plan de recuperación debe crearse antes de la restauración.
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory de Active Directory Domain Services, planificación de recuperación
- Active Directory de Active Directory Domain Services, copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bf284804ba5a8882ecee6f6e03ae95249e5435
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077554"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a>Consideraciones sobre la copia de seguridad de Active Directory Domain Services

Se pueden replicar los datos del servicio de directorio. Un plan de recuperación debe crearse antes de la restauración. Una opción consiste en restaurar una réplica de un directorio y, a continuación, propagar los cambios que se produjeron desde la copia de seguridad de otras réplicas del dominio.

En algunos casos, puede que desee que la réplica restaurada tenga prioridad sobre las demás réplicas del dominio. Por ejemplo, si un objeto se elimina accidentalmente y la eliminación se replica en todos los controladores de dominio, puede restaurar el objeto restaurando una réplica a partir de una copia de seguridad realizada antes de que se eliminara el objeto. A continuación, usaría la utilidad NTDSUtil para marcar el objeto restaurado como restaurado de forma autoritativa. Después, el objeto restaurado se replicará en los demás controladores de seguridad y la réplica que se restauró recibirá las actualizaciones para todos los demás objetos que se produjeron desde el momento en que se realizó la copia de seguridad. El resultado final de todas las réplicas es el mismo que antes de la restauración, salvo que ya no se elimina el objeto restaurado de forma autoritativa.

Todos los cambios que se producen durante la copia de seguridad se almacenan en un registro temporal y se agregan al final del conjunto de copia de seguridad cuando se completa la copia de seguridad.

Cualquier plan de recuperación debe asegurarse de que la antigüedad de la copia de seguridad no debe superar la duración de los Active Directory de desecho. Para obtener más información sobre la duración de los marcadores de exclusión, vea el tema de TechNet: [Introducción a la administración de copias de seguridad y recuperación de Active Directory](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10)). La restauración de una copia de seguridad anterior a la duración del objeto de desecho puede hacer que el controlador de dominio restaurado tenga objetos que no se replicarán en otros controladores de dominio. Esto sucede si se elimina un objeto una vez realizada la copia de seguridad y la restauración se produce después de que el objeto de desecho del objeto eliminado se haya quitado permanentemente. El controlador de dominio restaurado tendría el objeto tal como existía antes de la eliminación, y los demás controladores de dominio no tendrían ningún registro que el objeto existiera. En este caso, un administrador tendrá que eliminar manualmente cada objeto no replicado en el controlador de dominio restaurado.

No se admiten copias de seguridad incrementales de Active Directory Domain Services; se requieren copias de seguridad completas.

 

 