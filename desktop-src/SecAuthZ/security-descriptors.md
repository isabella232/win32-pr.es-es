---
description: Un descriptor de seguridad contiene la información de seguridad asociada a un objeto protegible.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908169"
---
# <a name="security-descriptors"></a>Descriptor de seguridad

Un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) contiene la información de seguridad asociada a un [objeto protegible](securable-objects.md). Un descriptor de seguridad está formado por una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) y su información de seguridad asociada. Un descriptor de seguridad puede incluir la siguiente información de seguridad:

-   [Identificadores de seguridad](security-identifiers.md) (SID) para el propietario y el grupo primario de un objeto.
-   [DACL](access-control-lists.md) que especifica los derechos de acceso permitidos o denegados a usuarios o grupos determinados.
-   [SACL](access-control-lists.md) que especifica los tipos de intentos de acceso que generan registros de auditoría para el objeto.
-   Conjunto de bits de control que califican el significado de un descriptor de seguridad o sus miembros individuales.

Las aplicaciones no deben manipular directamente el contenido de un descriptor de seguridad. La API de Windows proporciona funciones para establecer y recuperar la información de seguridad en el descriptor de seguridad de un objeto. Además, hay funciones para crear e inicializar un descriptor de seguridad para un nuevo objeto.

Las aplicaciones que trabajan con descriptores de seguridad en Active Directory objetos pueden utilizar las funciones de seguridad de Windows o las interfaces de seguridad proporcionadas por las interfaces de servicio Active Directory (ADSI). Para obtener más información acerca de las interfaces de seguridad ADSI, vea [Cómo funciona Access Control en Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
