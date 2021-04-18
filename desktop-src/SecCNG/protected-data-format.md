---
description: Los datos protegidos se almacenan como un BLOB con codificación ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de datos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156145"
---
# <a name="protected-data-format"></a>Formato de datos protegidos

Los datos protegidos se almacenan como un BLOB con codificación ASN. 1. Los datos tienen el formato CMS (sintaxis de mensajes de certificado). La envoltura digital contiene contenido cifrado, información de destinatarios que contiene una clave de cifrado de contenido cifrada (CEK) y un encabezado que contiene información sobre el contenido, incluida la cadena de regla del descriptor de protección sin cifrar. Esto se muestra en el diagrama siguiente.

![datos con doble cifrado protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DPAPI DE CNG](cng-dpapi.md)
</dt> <dt>

[Descriptores de protección](protection-descriptors.md)
</dt> <dt>

[Proveedores de protección](protection-providers.md)
</dt> </dl>

 

 



