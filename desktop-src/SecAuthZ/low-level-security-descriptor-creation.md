---
description: Funciones para crear un descriptor de seguridad y obtener y establecer los componentes de un descriptor de seguridad.
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: Creación de descriptores de seguridad de bajo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781488"
---
# <a name="low-level-security-descriptor-creation"></a>Creación de descriptores de seguridad de bajo nivel

El control de acceso de bajo nivel proporciona un conjunto de funciones para crear un descriptor de [*seguridad*](/windows/desktop/SecGloss/s-gly) y obtener y establecer los componentes de un descriptor de seguridad. Las funciones de bajo nivel para inicializar y establecer los componentes de un descriptor de seguridad solo funcionan con descriptores de seguridad de formato absoluto. Las funciones de bajo nivel para obtener los componentes de un descriptor de seguridad funcionan con descriptores de seguridad [absolutos y auto relativos.](absolute-and-self-relative-security-descriptors.md)

La [**función InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) inicializa un búfer [**DEL DESCRIPTOR \_ DE**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) SEGURIDAD. El descriptor de seguridad [](/windows/desktop/SecGloss/a-gly) inicializado está en formato absoluto y no tiene ningún propietario, grupo principal, lista de control de acceso [*discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) ni lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL). Puede usar las siguientes funciones de bajo nivel para obtener o establecer componentes específicos de un descriptor de seguridad especificado.



| Función                                                             | Descripción                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | Recupera información de revisión y control de un descriptor de seguridad.                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | Recupera la DACL de un descriptor de seguridad.                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | Recupera el identificador de seguridad [*de grupo principal*](/windows/desktop/SecGloss/s-gly) (SID) de un descriptor de seguridad. |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | Devuelve la longitud de un descriptor de seguridad.                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | Recupera el SID del propietario de un descriptor de seguridad.                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | Recupera la SACL de un descriptor de seguridad.                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | Coloca una DACL en un descriptor de seguridad, superando cualquier DACL existente.                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | Establece el SID del grupo principal de un descriptor de seguridad.                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | Establece el SID del propietario de un descriptor de seguridad.                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | Coloca una SACL en un descriptor de seguridad, superando cualquier SACL existente.                                                                                                    |



 

Para comprobar el nivel de revisión y la [*integridad estructural*](/windows/desktop/SecGloss/i-gly) de un descriptor de seguridad, llame a la [**función IsValidSecurityDescriptor.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor)

 

 
