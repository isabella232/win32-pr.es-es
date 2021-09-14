---
description: Los datos protegidos se almacenan como blobs codificados por ASN.1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de datos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073656"
---
# <a name="protected-data-format"></a>Formato de datos protegidos

Los datos protegidos se almacenan como blobs codificados por ASN.1. Los datos tienen el formato CMS (sintaxis de mensaje de certificado) con sobres. El sobre digital contiene contenido cifrado, información del destinatario que contiene una clave de cifrado de contenido cifrado (CEK) y un encabezado que contiene información sobre el contenido, incluida la cadena de regla de descriptor de protección sin cifrar. Esto se muestra en el diagrama siguiente.

![datos sobres protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Descriptores de protección](protection-descriptors.md)
</dt> <dt>

[Proveedores de protección](protection-providers.md)
</dt> </dl>

 

 



