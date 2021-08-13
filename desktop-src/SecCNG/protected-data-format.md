---
description: Los datos protegidos se almacenan como un BLOB codificado en ASN.1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de datos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907416"
---
# <a name="protected-data-format"></a>Formato de datos protegidos

Los datos protegidos se almacenan como un BLOB codificado en ASN.1. El formato de los datos es CMS (sintaxis de mensaje de certificado). El sobre digital contiene contenido cifrado, información del destinatario que contiene una clave de cifrado de contenido cifrado (CEK) y un encabezado que contiene información sobre el contenido, incluida la cadena de regla de descriptor de protección sin cifrar. Esto se muestra en el diagrama siguiente.

![datos sobres protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Descriptores de protección](protection-descriptors.md)
</dt> <dt>

[Proveedores de protección](protection-providers.md)
</dt> </dl>

 

 



