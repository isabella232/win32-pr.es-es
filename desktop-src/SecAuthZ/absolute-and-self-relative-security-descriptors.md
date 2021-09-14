---
description: Para determinar si un descriptor de seguridad es relativo o absoluto, llame a la función GetSecurityDescriptorControl y compruebe la marca SELF RELATIVE SE del parámetro \_ \_ SECURITY DESCRIPTOR \_ \_ CONTROL.
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descriptores de seguridad Self-Relative y absolutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57406e194a31e79594394913055609e2981e5cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160862"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descriptores de seguridad Self-Relative y absolutos

Un [*descriptor de*](/windows/desktop/SecGloss/s-gly) seguridad puede tener un formato [*absoluto*](/windows/desktop/SecGloss/a-gly) o [*auto relativo.*](/windows/desktop/SecGloss/s-gly) En formato absoluto, un descriptor de seguridad contiene punteros a su información, no a la propia información. En formato auto-relativo, un descriptor de seguridad almacena una estructura [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) y la información de seguridad asociada en un bloque contiguo de memoria. Para determinar si un descriptor de seguridad es auto relativo o absoluto, llame a la función [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) y compruebe la marca SELF RELATIVE SE del parámetro \_ SECURITY DESCRIPTOR \_ [**\_ \_ CONTROL.**](security-descriptor-control.md) Puede usar las [**funciones MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) y [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) para convertir entre estos dos formatos.

El formato absoluto es útil cuando se crea un descriptor de seguridad y se tienen punteros a todos los componentes, por ejemplo, cuando la configuración predeterminada del propietario, el grupo y la ACL discrecional están disponibles. En este caso, puede llamar a la función [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) para inicializar una estructura [**\_ DE DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) DE SEGURIDAD y, a continuación, llamar a funciones como [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) para asignar punteros ACL y SID al descriptor de seguridad.

En formato auto relativo, un descriptor de seguridad siempre comienza con una estructura [**DESCRIPTOR DE \_ SEGURIDAD,**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) pero los demás componentes del descriptor de seguridad pueden seguir la estructura en cualquier orden. En lugar de usar direcciones de memoria, los componentes del descriptor de seguridad se identifican mediante desplazamientos desde el principio del descriptor. Este formato es útil cuando un descriptor de seguridad se debe almacenar en el disco, transmitirse mediante un protocolo de comunicaciones o copiarse en memoria.

Excepto [**MakeAbsoluteSD,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd)todas las funciones que devuelven un descriptor de seguridad lo hacen con el formato auto relativo. Los descriptores de seguridad pasados como argumentos a una función pueden ser de forma relativa o absoluta. Para obtener más información, consulte la documentación de la función.

 

 
