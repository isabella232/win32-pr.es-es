---
description: Un descriptor de seguridad contiene la información de seguridad asociada a un objeto protegible.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253658"
---
# <a name="security-descriptors"></a>Descriptor de seguridad

Un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) contiene la información de seguridad asociada a un objeto [protegible](securable-objects.md). Un descriptor de seguridad consta de una estructura [**\_ DE DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) y su información de seguridad asociada. Un descriptor de seguridad puede incluir la siguiente información de seguridad:

-   [Identificadores de](security-identifiers.md) seguridad (SID) para el propietario y el grupo principal de un objeto.
-   UNA [DACL que](access-control-lists.md) especifica los derechos de acceso permitidos o denegados a usuarios o grupos concretos.
-   SACL [que](access-control-lists.md) especifica los tipos de intentos de acceso que generan registros de auditoría para el objeto.
-   Conjunto de bits de control que califican el significado de un descriptor de seguridad o sus miembros individuales.

Las aplicaciones no deben manipular directamente el contenido de un descriptor de seguridad. La API Windows proporciona funciones para establecer y recuperar la información de seguridad en el descriptor de seguridad de un objeto. Además, hay funciones para crear e inicializar un descriptor de seguridad para un nuevo objeto .

Las aplicaciones que trabajan con descriptores de seguridad en objetos Active Directory pueden usar las funciones de seguridad Windows o las interfaces de seguridad proporcionadas por Active Directory Service Interfaces (ADSI). Para obtener más información sobre las interfaces de seguridad ADSI, vea [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
