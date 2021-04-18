---
description: Para crear extensiones personalizadas o codificar una extensión compleja, puede escribir sus propios controladores de extensión que exporten interfaces personalizadas.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Escribir controladores de extensión personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688251"
---
# <a name="writing-custom-extension-handlers"></a>Escribir controladores de extensión personalizados

Para crear extensiones personalizadas o codificar una extensión compleja, puede escribir sus propios controladores de extensión que exporten interfaces personalizadas. Los servicios de Certificate Server de Microsoft se distribuyen con las siguientes interfaces que se pueden usar para codificar diversos tipos de datos de extensión: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)y [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray). Estas interfaces están contenidas en Certenc.dll. Además, la información de tipo de estas interfaces se incluye en Certencl.dll, que se encuentra en el kit de desarrollo de software (SDK) de la plataforma.

Para obtener más información sobre los controladores de extensión, vea [controladores de extensión](extension-handlers.md).

 

 



