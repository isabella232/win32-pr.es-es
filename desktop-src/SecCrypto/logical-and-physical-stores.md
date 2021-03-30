---
description: Los almacenes del sistema predeterminados, incluidos MY, CA y ROOT, se implementan como almacenes de recopilación lógica con un número de almacenes físicos predefinidos como sus almacenes de miembros.
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: Almacenes lógicos y físicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810255"
---
# <a name="logical-and-physical-stores"></a>Almacenes lógicos y físicos

Los almacenes del sistema predeterminados, incluidos MY, CA y ROOT, se implementan como almacenes de recopilación lógica con un número de almacenes físicos predefinidos como sus almacenes de miembros. Los almacenes físicos de miembros de un almacén del sistema se abren automáticamente al abrir el almacén del sistema. Un usuario puede Agregar almacenes físicos adicionales a cualquier colección de almacenes del sistema. La función CryptoAPI [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) agrega un nuevo almacén físico a una colección de almacenes del sistema. [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) desasocia un almacén físico de un almacén lógico del sistema. [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) crea un nuevo almacén del sistema en un registro hKey, mientras que [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) quita un almacén del sistema del registro.

En CryptoAPI, los almacenes de sistema son almacenes lógicos con almacenes físicos asociados. Todos los certificados de un almacén del sistema existente permanecen disponibles y la adición física de nuevos certificados se realiza en los almacenes físicos que componen el almacén lógico del sistema.

Los usuarios que prefieren seguir usando almacenes físicos del sistema y no convertirlos en almacenes lógicos pueden abrir almacenes del sistema con el \_ \_ \_ \_ proveedor del registro del sistema del almacén de certificados. Este proveedor seguirá usando cada almacén del sistema como un único almacén físico.

Las funciones [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation), [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)y [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) muestran las ubicaciones del almacén del sistema, los almacenes del sistema disponibles y todos los almacenes físicos que son miembros de un almacén del sistema.

También se pueden reubicar los almacenes del sistema. De forma predeterminada, se abre un almacén del sistema en relación con una subclave del registro después de un patrón predefinido. Para obtener más información, vea [ubicaciones del almacén del sistema](system-store-locations.md). La configuración de la \_ \_ marca de reubicación del almacén del sistema de certificados \_ \_ en el parámetro *DwFlags* que se pasa a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) coloca un almacén del sistema en el registro en una subclave del registro especificada por el usuario en lugar de la predefinida.

 

 



