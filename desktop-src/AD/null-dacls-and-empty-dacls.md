---
title: DACL null y DACL vacías (AD DS)
description: La presencia de una lista de control de acceso discrecional (DACL) nula en el atributo nTSecurityDescriptor de cualquier objeto puede crear un riesgo de seguridad grave.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACL null y AD DACL vacío
- DACLs AD, Null y Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185800"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACL null y DACL vacías (AD DS)

La presencia de una lista de control de acceso discrecional (DACL) nula en el atributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) de cualquier objeto puede crear un riesgo de seguridad grave. Una DACL nula concede acceso total a cualquier usuario que lo solicite; No se realiza la comprobación de seguridad normal con respecto al objeto . Una DACL null no se debería confundir con una DACL vacía. Una DACL vacía es una DACL asignada e inicializada correctamente que no contiene entradas de control de acceso (ACE). Una DACL vacía no concede ningún acceso al objeto al que se asigna.

Para obtener más información, [vea NULL DACLs y Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 