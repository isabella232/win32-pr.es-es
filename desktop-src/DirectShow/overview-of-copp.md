---
description: Información general de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Información general de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362375"
---
# <a name="overview-of-copp"></a>Información general de COPP

Estos son los pasos básicos que una aplicación debe realizar para usar el Protocolo de protección de salida certificado (COPP).

**Obtener la cadena de certificados del controlador**

1.  Cree un DirectShow de reproducción de vídeo que represente vídeo mediante el representador de mezcla de vídeo (VMR-7 o VMR-9) o el filtro [**Representador**](enhanced-video-renderer-filter.md) de vídeo mejorado (EVR).
2.  Consulte vmr para la [**interfaz IAMCertifiedOutputProtection.**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection)
3.  Llame [**a IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Este método devuelve un número aleatorio de 128 bits del controlador, junto con una cadena de certificados que contiene la clave pública RSA de 2048 bits del controlador.

**Validación de la cadena de certificados**

1.  Valide la cadena de certificados. Si la cadena de certificados no es válida, detenga.
2.  Compruebe la lista de revocación de certificados (CRL). Si alguno de los certificados de la cadena de certificados aparece en la lista de revocación, detenga.
3.  Obtenga la clave pública RSA de la cadena de certificados.

**Inicialización de la sesión copp**

1.  Generar una clave de sesión AES de 128 bits. Esta clave se usa para firmar datos y comprobar que los datos firmados no se han alterado.
2.  Genere dos números aleatorios de 32 bits seguros criptográficamente. El primero es un número de secuencia de estado y el segundo es un número de secuencia de comandos. Cada vez que la aplicación envía un comando o una solicitud de estado, incrementa el número de secuencia correspondiente e incluye este número en el comando COPP o los datos de solicitud.
3.  Concatene el número aleatorio de 128 bits del controlador de gráficos, la clave de sesión AES, el número de secuencia de estado y el número de secuencia de comandos. Cifre esta matriz de bytes mediante la clave pública del controlador y pase el resultado a [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).

**Envío de comandos COPP y solicitudes de estado**

1.  Consulte los tipos de protección disponibles y otra información llamando a [**IAMCertifiedOutputProtection::P rotectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).
2.  Establezca los niveles de protección deseados llamando a [**IAMCertifiedOutputProtection::P rotectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).
3.  Consulte periódicamente el nivel de protección local actual. Detenga la reproducción si el nivel de protección local cambia inesperadamente o si se detecta un problema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



