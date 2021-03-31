---
title: Leer defaultSecurityDescriptor para una clase de objeto
description: Con ADSI, puede obtener el atributo defaultSecurityDescriptor de una clase de objeto con la interfaz IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, leer defaultSecurityDescriptor para una clase de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077500"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Leer defaultSecurityDescriptor para una clase de objeto

Con ADSI, puede obtener el atributo **defaultSecurityDescriptor** de una clase de objeto con la interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) . Para obtener el atributo **defaultSecurityDescriptor** de una clase de objeto, realice los pasos siguientes.

1.  Obtiene un puntero de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) al objeto **ClassSchema** para la clase de objeto.
2.  Use el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obtener el descriptor de seguridad predeterminado del objeto. El nombre de la propiedad que contiene el descriptor de seguridad es "defaultSecurityDescriptor". La propiedad se devolverá como una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que contiene un BSTR con el descriptor de seguridad predeterminado en el formato de cadena SDDL.
3.  Utilice la función [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para convertir el formato de cadena SDDL en un descriptor de seguridad.
4.  Use las API de seguridad [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)y [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) para leer los elementos del descriptor de seguridad.

Para ver un ejemplo de código que muestra cómo hacerlo, consulte el [código de ejemplo para leer defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 