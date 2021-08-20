---
title: Leer defaultSecurityDescriptor para una clase object
description: Con ADSI, puede obtener el atributo defaultSecurityDescriptor para una clase de objeto con la interfaz IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , leer defaultSecurityDescriptor para una clase object
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26204ebe31155363a1be8bf30bd1c0495d16a939b58789f421a0772d6d90a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184696"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Leer defaultSecurityDescriptor para una clase object

Con ADSI, puede obtener el atributo **defaultSecurityDescriptor** para una clase de objeto con la [**interfaz IADs.**](/windows/desktop/api/iads/nn-iads-iads) Para obtener el **atributo defaultSecurityDescriptor** para una clase de objeto, realice los pasos siguientes.

1.  Obtiene un [**puntero de interfaz IADs**](/windows/desktop/api/iads/nn-iads-iads) al **objeto classSchema** de la clase de objeto .
2.  Use el [**método IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obtener el descriptor de seguridad predeterminado del objeto . El nombre de la propiedad que contiene el descriptor de seguridad es "defaultSecurityDescriptor". La propiedad se devolverá como [**variant que**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene un BSTR con el descriptor de seguridad predeterminado en formato de cadena SDDL.
3.  Use la [**función ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para convertir el formulario de cadena SDDL en un descriptor de seguridad.
4.  Use las API de seguridad [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)y [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) para leer las partes del descriptor de seguridad.

Para obtener un ejemplo de código que muestra cómo hacerlo, vea Ejemplo de código para leer [defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 