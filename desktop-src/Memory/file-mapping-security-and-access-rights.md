---
description: El modelo de seguridad de Windows permite controlar el acceso a los objetos de asignación de archivos. Para obtener más información, vea modelo de Access-Control.
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: Derechos de acceso y seguridad de asignación de archivos
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: 65d520e12d1b555e7c633f0d1e0ba5142c330ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677357"
---
# <a name="file-mapping-security-and-access-rights"></a>Derechos de acceso y seguridad de asignación de archivos

El modelo de seguridad de Windows permite controlar el acceso a los objetos de asignación de archivos. Para obtener más información, vea [modelo de control de acceso](../secauthz/access-control-model.md).

Puede especificar un [descriptor de seguridad](../secauthz/security-descriptors.md) para un objeto de asignación de archivos al llamar a la función [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) . Si especifica **null**, el objeto obtiene un descriptor de seguridad predeterminado. Las ACL del descriptor de seguridad predeterminado para un objeto de asignación de archivos proceden del token principal o de suplantación del creador.

Para recuperar el descriptor de seguridad de un objeto de asignación de archivos, llame a la función [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) o [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) . Para establecer el descriptor de seguridad de un objeto de asignación de archivos, llame a la función [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) o [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Los derechos de acceso válidos para los objetos de asignación de archivos incluyen los [derechos de acceso](../secauthz/standard-access-rights.md)de **eliminación**, **\_ control de lectura**, **\_ DAC de escritura** y **\_ propietario de escritura** . Los objetos de asignación de archivos no admiten el derecho **sincronizar** el acceso estándar. En la tabla siguiente se enumeran los derechos de acceso que son específicos de los objetos de asignación de archivos.

| Derecho de acceso | Significado |
|-|-|
| **asignación de archivos \_ \_ todos los \_ accesos** | Incluye todos los derechos de acceso a un objeto de asignación de archivos, excepto la **\_ \_ ejecución de asignación de archivos**. Las funciones [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) y [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) tratan esto igual que si se especifica **la \_ \_ escritura de asignación de archivos**. |
| **\_ejecución de asignación de archivos \_** | Permite la asignación de vistas ejecutables del objeto de asignación de archivos. El objeto se debe haber creado con protección de página que permita el acceso de ejecución, como **Page \_ Execute \_ Read**, **Page \_ Execute \_ WRITECOPY** o **Page \_ Execute \_ ReadWrite** Protection.  |
| **\_lectura del mapa de archivos \_** | Permite la asignación de vistas de solo lectura o de copia en escritura del objeto de asignación de archivos.  |
| **\_escritura de asignación de archivos \_** | Permite asignar vistas de solo lectura, de copia en escritura o de lectura y escritura de un objeto de asignación de archivos. El objeto se debe haber creado con protección de página que permita el acceso de escritura, como la **página \_ ReadWrite** o la protección **\_ \_ ReadWrite de ejecución de página** . |

La asignación de una vista de copia en escritura de un objeto de asignación de archivos requiere el mismo acceso que la asignación de una vista de solo lectura. La marca de **\_ \_ copia del mapa de archivos** no es un derecho de acceso y no debe especificarse como parte de una DACL en un descriptor de seguridad. Este valor solo se puede usar con funciones que asignan una vista de un objeto de asignación de archivos, como las funciones [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) y [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) , o con la función [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) , que trata la **copia del \_ mapa \_ de archivos** de la misma forma que trata la **lectura del \_ mapa \_ de archivos**.

Puede solicitar el derecho de acceso de **\_ \_ seguridad del sistema de acceso** a un objeto de asignación de archivos si desea leer o escribir la SACL del objeto. Para obtener más información, consulte derechos [de acceso de las listas de control de acceso (ACL)](../secauthz/access-control-lists.md) y [SACL](../secauthz/sacl-access-right.md).
