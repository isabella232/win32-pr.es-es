---
description: XML es un estándar del sector para describir los datos estructurados. Una firma digital XML es una representación XML de una firma digital que proporciona la capacidad de comprobar el origen y la integridad del documento XML y los datos a los que se hace referencia externamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Información general sobre la firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687579"
---
# <a name="xml-digital-signature-overview"></a>Información general sobre la firma digital XML

XML es un estándar del sector para describir los datos estructurados. Una firma digital XML es una representación XML de una [*firma digital*](../secgloss/d-gly.md) que proporciona la capacidad de comprobar el origen y la integridad del documento XML y los datos a los que se hace referencia externamente. Las firmas digitales XML se pueden usar para firmar datos arbitrarios, como un documento o fragmento XML, una página HTML, texto sin formato o datos codificados en binario, como un archivo JPEG.

El formato de firma digital XML admitido por la API de firma digital de CryptXML se especifica mediante la recomendación de XML Signature Syntax and Processing (Second Edition) W3C.

La firma digital de CryptXML implementa la compatibilidad con los tipos de firma, los algoritmos criptográficos, los algoritmos de canonización y la transformación protegida con envoltorio especificados.

Los desarrolladores pueden extender el conjunto predeterminado de algoritmos criptográficos compatibles con CryptXML mediante la creación de archivos dll de extensión criptográfica. Los desarrolladores también pueden crear sus propias transformaciones y algoritmos de canonización personalizados sobre la API de CryptXML. Los desarrolladores pueden usar las API de CryptXML con las API de certificados de Windows.

 

 
