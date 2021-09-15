---
description: Los almacenes del sistema predeterminados, incluidos MY, CA y ROOT, se implementan como almacenes de recopilación lógicos con una serie de almacenes físicos predefinidos como almacenes de miembros.
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: Almacenes lógicos y físicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270948"
---
# <a name="logical-and-physical-stores"></a>Almacenes lógicos y físicos

Los almacenes del sistema predeterminados, incluidos MY, CA y ROOT, se implementan como almacenes de recopilación lógicos con una serie de almacenes físicos predefinidos como almacenes de miembros. Los almacenes físicos miembros de un almacén del sistema se abren automáticamente cuando se abre el almacén del sistema. Un usuario puede agregar almacenes físicos adicionales a cualquier colección de almacenes del sistema. La función CryptoAPI [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) agrega un nuevo almacén físico a una colección de almacenes del sistema. [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) desasocia un almacén físico de un almacén del sistema lógico. [**CertRegisterSystemStore crea**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) un nuevo almacén del sistema en un hKey del Registro, mientras [**que CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) quita un almacén del sistema del Registro.

En CryptoAPI, los almacenes del sistema son almacenes lógicos con almacenes físicos asociados. Todos los certificados de un almacén del sistema existente siguen estando disponibles y la adición física de nuevos certificados se realiza en los almacenes físicos que son el almacén del sistema lógico.

Los usuarios que prefieran seguir usando almacenes físicos del sistema y que no se conviertan en almacenes lógicos pueden abrir almacenes del sistema con el proveedor CERT \_ STORE \_ PROV \_ SYSTEM \_ REGISTRY. Este proveedor seguirá usando cada almacén del sistema como un único almacén físico.

Las funciones [**CertEnumSystemStoreLocation,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)y [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) enumeran las ubicaciones del almacén del sistema, los almacenes del sistema disponibles y todos los almacenes físicos que son miembros de un almacén del sistema.

Los almacenes del sistema también se pueden reubicar. De forma predeterminada, un almacén del sistema se abre en relación con una subclave del Registro siguiendo un patrón predefinido. Para obtener más información, vea [System Store Locations](system-store-locations.md). Al establecer CERT SYSTEM STORE RELOCATE FLAG en el parámetro \_ \_ \_ \_ *dwFlags* pasado a [**CertOpenStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) se coloca un almacén del sistema en el Registro bajo una subclave del Registro especificada por el usuario en lugar de la predefinida.

 

 



