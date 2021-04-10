---
title: Nomenclatura de contextos y particiones de directorio
description: Cada controlador de dominio de un bosque de dominio controlado por Active Directory Domain Services incluye particiones de directorio.
ms.assetid: 77ac171c-2031-46d7-b81e-dd9ae0c70ccb
ms.tgt_platform: multiple
keywords:
- Nomenclatura de los contextos y las particiones de directorio AD
- Nomenclatura de contextos AD, acerca de
- Particiones de directorio AD, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39934f0236e927bff281230c41a303f5e6d2bb0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995070"
---
# <a name="naming-contexts-and-directory-partitions"></a>Nomenclatura de contextos y particiones de directorio

Cada controlador de dominio de un bosque de dominio controlado por Active Directory Domain Services incluye [*particiones de directorio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)). Las particiones de directorio también se conocen como [*contextos de nomenclatura*](/previous-versions/windows/desktop/legacy/ms681918(v=vs.85)). Una partición de directorio es una parte contigua del directorio general que tiene un ámbito de replicación independiente y datos de programación. De forma predeterminada, el servicio Dominio de Active Directory de una empresa contiene las siguientes particiones:

-   [*Partición de esquema*](/previous-versions/windows/desktop/legacy/ms681936(v=vs.85)): la partición de esquema contiene los objetos **ClassSchema** y **attributeSchema** que definen los tipos de objetos que pueden existir en el bosque. Cada controlador de dominio del bosque tiene una réplica de la misma partición de esquema.
-   [*Partición de configuración*](/previous-versions/windows/desktop/legacy/ms681898(v=vs.85)): la partición de configuración contiene la topología de replicación y otros datos de configuración que deben replicarse en todo el bosque. Cada controlador de dominio del bosque tiene una réplica de la misma partición de configuración.
-   [*Partición de dominio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)): la partición de dominio contiene los objetos de directorio, como usuarios y equipos, asociados con el dominio local. Un dominio puede tener varios controladores de dominio y un bosque puede tener varios dominios. Cada controlador de dominio almacena una réplica completa de la partición de dominio para su dominio local, pero no almacena réplicas de las particiones de dominio para otros dominios.

Windows Server 2003 presenta la *partición del directorio de aplicaciones*, que proporciona la capacidad de controlar el ámbito de replicación y permitir la colocación de las réplicas de una manera más adecuada para los datos dinámicos. Para obtener más información acerca de las particiones de directorio de aplicaciones, consulte [acerca de las particiones de directorio de aplicaciones](about-application-directory-partitions.md).

Para obtener más información sobre cómo Active Directory Domain Services mantener la coherencia entre las distintas réplicas de una partición de directorio, vea [replicación e integridad](replication-and-data-integrity.md)de los datos.

 

 