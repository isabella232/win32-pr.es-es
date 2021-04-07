---
description: Para determinar si un descriptor de seguridad es autorelativo o absoluto, llame a la función GetSecurityDescriptorControl y Compruebe la \_ \_ marca autorelative del \_ parámetro de control del descriptor de seguridad \_ .
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descriptores de seguridad Absolute y Self-Relative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57406e194a31e79594394913055609e2981e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002177"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descriptores de seguridad Absolute y Self-Relative

Un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) puede tener un formato [*absoluto*](/windows/desktop/SecGloss/a-gly) o [*autorelativo*](/windows/desktop/SecGloss/s-gly) . En el formato absoluto, un descriptor de seguridad contiene punteros a su información, no la propia información. En el formato autorelativo, un descriptor de seguridad almacena una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) y la información de seguridad asociada en un bloque de memoria contiguo. Para determinar si un descriptor de seguridad es autorelativo o absoluto, llame a la función [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) y Compruebe la \_ \_ marca autorelative del parámetro de [**\_ \_ control del descriptor de seguridad**](security-descriptor-control.md) . Puede usar las funciones [**MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) y [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) para convertir entre estos dos formatos.

El formato absoluto es útil cuando se crea un descriptor de seguridad y se tienen punteros a todos los componentes, por ejemplo, cuando están disponibles los valores predeterminados para el propietario, el grupo y la ACL discrecional. En este caso, puede llamar a la función [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) para inicializar una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) y, a continuación, llamar a funciones como [**SETSECURITYDESCRIPTORDACL**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) para asignar punteros de ACL y SID al descriptor de seguridad.

En el formato autorelativo, un descriptor de seguridad siempre comienza con una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , pero los demás componentes del descriptor de seguridad pueden seguir la estructura en cualquier orden. En lugar de utilizar direcciones de memoria, los componentes del descriptor de seguridad se identifican mediante desplazamientos desde el principio del descriptor. Este formato resulta útil cuando un descriptor de seguridad debe almacenarse en el disco, transmitirse por medio de un protocolo de comunicaciones o copiarse en memoria.

Excepto en el caso de [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd), todas las funciones que devuelven un descriptor de seguridad lo hacen con el formato autorelativo. Los descriptores de seguridad que se pasan como argumentos a una función pueden ser de forma automática o absoluta. Para obtener más información, consulte la documentación de la función.

 

 
