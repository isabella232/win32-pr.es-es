---
description: XML es un estándar del sector para describir datos estructurados. Una firma digital XML es una representación XML de una firma digital que proporciona la capacidad de comprobar el origen y la integridad del documento XML y los datos a los que se hace referencia externamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Información general sobre la firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c23089c6bb49aefd58ada376407785434017a0141f4a4996d8590cc2a05f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895733"
---
# <a name="xml-digital-signature-overview"></a>Información general sobre la firma digital XML

XML es un estándar del sector para describir datos estructurados. Una firma digital XML es una representación XML de una firma [*digital*](../secgloss/d-gly.md) que proporciona la capacidad de comprobar el origen y la integridad del documento XML y los datos a los que se hace referencia externamente. Las firmas digitales XML se pueden usar para firmar datos arbitrarios, incluidos un documento o fragmento XML, una página HTML, texto sin formato o datos con codificación binaria, como un archivo JPEG.

El formato de firma digital XML compatible con la API de firma digital CryptXML se especifica mediante la recomendación W3C de sintaxis y procesamiento de firmas XML (segunda edición).

La firma digital CryptXML implementa compatibilidad con los tipos de firma necesarios, los algoritmos criptográficos, los algoritmos de canonización y la transformación con sobre especificada.

Los desarrolladores pueden ampliar el conjunto predeterminado de algoritmos criptográficos admitidos por CryptXML mediante la creación de archivos DLL de extensión criptográfica. Los desarrolladores también pueden crear sus propias transformaciones personalizadas y algoritmos de canonización sobre la API de CryptXML. Los desarrolladores pueden usar las API de CryptXML con Windows API de certificado.

 

 
