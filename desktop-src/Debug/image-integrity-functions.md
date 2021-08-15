---
description: Las funciones de integridad de imagen administran el conjunto de certificados en un archivo de imagen.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funciones de integridad de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a2311ccfc59fb228a8f71c380205dc754452ba4a9d0a7e1dcb3c9edcd92a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957107"
---
# <a name="image-integrity-functions"></a>Funciones de integridad de imágenes

Las funciones de integridad de imagen administran el conjunto de certificados en un archivo de imagen. Se proporcionan rutinas para agregar, quitar y consultar certificados. También hay una función disponible para obtener la secuencia de bytes de un archivo de imagen necesaria para calcular un resumen del mensaje del archivo de imagen. Esto es necesario para crear certificados de firma.

Cada certificado de un archivo tiene un índice que puede cambiar a medida que se quitan los certificados. Los nuevos certificados siempre se agregarán "al final" de la lista de certificados existentes. Es decir, se les asignarán índices mayores que cualquier índice actualmente en uso. En general, una aplicación no debe suponer que un certificado determinado tiene el mismo índice que tenía la última vez que se presentó la referencia.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



