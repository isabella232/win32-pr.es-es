---
description: El Windows de seguridad le permite controlar el acceso a los objetos de asignación de archivos. Para obtener más información, vea Access-Control Modelo.
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: Derechos de acceso y seguridad de asignación de archivos
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: 65d520e12d1b555e7c633f0d1e0ba5142c330ce8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159868"
---
# <a name="file-mapping-security-and-access-rights"></a>Derechos de acceso y seguridad de asignación de archivos

El Windows de seguridad permite controlar el acceso a los objetos de asignación de archivos. Para obtener más información, vea [Modelo de control de acceso](../secauthz/access-control-model.md).

Puede especificar un [descriptor de seguridad para](../secauthz/security-descriptors.md) un objeto de asignación de archivos al llamar a la función [**CreateFileMapping.**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) Si especifica **NULL,** el objeto obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para un objeto de asignación de archivos proceden del token principal o de suplantación del creador.

Para recuperar el descriptor de seguridad de un objeto de asignación de archivos, llame a [**la función GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) o [**GetSecurityInfo.**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) Para establecer el descriptor de seguridad de un objeto de asignación de archivos, llame a la [**función SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**o SetSecurityInfo.**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo)

Los derechos de acceso válidos para los objetos de asignación de archivos incluyen los derechos de acceso estándar **DELETE**, **READ \_ CONTROL**, **WRITE \_ DAC** [y](../secauthz/standard-access-rights.md) **WRITE \_ OWNER** . Los objetos de asignación de archivos no admiten el derecho de acceso estándar **SYNCHRONIZE.** En la tabla siguiente se enumeran los derechos de acceso específicos de los objetos de asignación de archivos.

| Derecho de acceso | Significado |
|-|-|
| **ASIGNACIÓN \_ DE \_ ARCHIVOS ALL \_ ACCESS** | Incluye todos los derechos de acceso a un objeto de asignación de archivos, excepto **FILE \_ MAP \_ EXECUTE.** Las [**funciones MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) y [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) tratan esto igual que la especificación de **FILE MAP \_ \_ WRITE.** |
| **EJECUCIÓN DE \_ ASIGNACIÓN \_ DE ARCHIVOS** | Permite la asignación de vistas ejecutables del objeto de asignación de archivos. El objeto debe haber sido creado con protección de página que permita el acceso de ejecución, como **PAGE \_ EXECUTE \_ READ,** **PAGE EXECUTE \_ \_ WRITECOPY** o **la protección PAGE EXECUTE \_ \_ READWRITE.**  |
| **LECTURA DEL \_ MAPA \_ DE ARCHIVOS** | Permite la asignación de vistas de solo lectura o de copia en escritura del objeto de asignación de archivos.  |
| **ESCRITURA DE \_ ASIGNACIÓN \_ DE ARCHIVOS** | Permite la asignación de vistas de solo lectura, copia en escritura o lectura/escritura de un objeto de asignación de archivos. El objeto debe haber sido creado con protección de página que permita el acceso de escritura, como **la protección PAGE \_ READWRITE** o **PAGE EXECUTE \_ \_ READWRITE.** |

La asignación de una vista de copia en escritura de un objeto de asignación de archivos requiere el mismo acceso que asignar una vista de solo lectura. La **marca FILE MAP \_ \_ COPY** no es un derecho de acceso y no debe especificarse como parte de una DACL en un descriptor de seguridad. Este valor solo se puede usar con funciones que asignan una vista de un objeto de asignación de archivos, como las funciones [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) y [**MapViewOfFileEx,**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) o con la función [**OpenFileMapping,**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) que trata **FILE MAP \_ \_ COPY** de la misma manera que trata **FILE MAP \_ \_ READ.**

Puede solicitar el derecho **de acceso ACCESS SYSTEM \_ \_ SECURITY** a un objeto de asignación de archivos si desea leer o escribir la SACL del objeto. Para obtener más información, vea [Listas de control de acceso (ACL)](../secauthz/access-control-lists.md) y Derecho de acceso [sacl](../secauthz/sacl-access-right.md).
