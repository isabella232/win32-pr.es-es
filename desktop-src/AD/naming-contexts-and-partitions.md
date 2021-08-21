---
title: Contextos de nomenclatura y particiones de directorio
description: Cada controlador de dominio de un bosque de dominio controlado por Active Directory Domain Services incluye particiones de directorio.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Asignación de nombres a contextos y particiones de directorio de AD
- Contextos de nomenclatura de AD , Acerca de
- Particiones de directorio AD , Acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309b76b50270f093b3a4930680b343d517976e269e731082696b89bf6a58c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025713"
---
# <a name="naming-contexts-and-directory-partitions"></a>Contextos de nomenclatura y particiones de directorio

Cada controlador de dominio de un bosque de dominio controlado por Active Directory Domain Services incluye [*particiones de directorio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). Las particiones de directorio también se conocen [*como contextos de nomenclatura.*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)) Una partición de directorio es una parte contigua del directorio general que tiene datos de programación y ámbito de replicación independientes. De forma predeterminada, Dominio de Active Directory Service para una empresa contiene las siguientes particiones:

-   [*Partición de*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85))esquema: la partición de esquema contiene los objetos **classSchema** y **attributeSchema** que definen los tipos de objetos que pueden existir en el bosque. Cada controlador de dominio del bosque tiene una réplica de la misma partición de esquema.
-   [*Partición de configuración:*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85))la partición de configuración contiene la topología de replicación y otros datos de configuración que se deben replicar en todo el bosque. Cada controlador de dominio del bosque tiene una réplica de la misma partición de configuración.
-   [*Partición de*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))dominio: la partición de dominio contiene los objetos de directorio, como usuarios y equipos, asociados al dominio local. Un dominio puede tener varios controladores de dominio y un bosque puede tener varios dominios. Cada controlador de dominio almacena una réplica completa de la partición de dominio para su dominio local, pero no almacena las réplicas de las particiones de dominio para otros dominios.

Windows Server 2003 presenta la partición de directorio de aplicación *,* que proporciona la capacidad de controlar el ámbito de replicación y permitir la colocación de réplicas de una manera más adecuada para los datos dinámicos. Para obtener más información sobre las particiones de directorio de aplicación, vea [Acerca de las particiones de directorio de aplicación.](about-application-directory-partitions.md)

Para obtener más información sobre cómo Active Directory Domain Services mantener la coherencia entre las distintas réplicas de una partición de directorio, vea [Replicación e integridad de datos.](replication-and-data-integrity.md)

 

 