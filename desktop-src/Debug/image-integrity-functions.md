---
description: Las funciones de integridad de la imagen administran el conjunto de certificados en un archivo de imagen.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funciones de integridad de la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080174"
---
# <a name="image-integrity-functions"></a>Funciones de integridad de la imagen

Las funciones de integridad de la imagen administran el conjunto de certificados en un archivo de imagen. Se proporcionan rutinas para agregar, quitar y consultar certificados. También hay una función disponible para obtener la secuencia de bytes de un archivo de imagen necesario para calcular una síntesis del mensaje del archivo de imagen. Esto es necesario para crear certificados de firma.

Todos los certificados de un archivo tienen un índice que puede cambiar a medida que se quitan los certificados. Siempre se agregarán nuevos certificados "al final" de la lista de certificados existentes. Es decir, se les asignarán índices que son mayores que cualquier índice actualmente en uso. En general, una aplicación no debe suponer que un certificado determinado tiene el mismo índice que tenía la última vez que se hacía referencia a él.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



