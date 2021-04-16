---
description: Información general de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Información general de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686335"
---
# <a name="overview-of-copp"></a>Información general de COPP

Estos son los pasos básicos que una aplicación debe realizar para usar el protocolo de protección de la salida certificada (COPP).

**Obtención de la cadena de certificados del controlador**

1.  Cree un gráfico de reproducción de DirectShow que represente vídeo con el representador de mezcla de vídeo (VMR-7 o VMR-9) o el filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR).
2.  Consulte el VMR para la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .
3.  Llame a [**IAMCertifiedOutputProtection:: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Este método devuelve un número aleatorio de 128 bits del controlador, junto con una cadena de certificados que contiene la clave pública RSA de 2048 bits del controlador.

**Validar la cadena de certificados**

1.  Validar la cadena de certificados. Si la cadena de certificados no es válida, detenga.
2.  Compruebe la lista de revocación de certificados (CRL). Si alguno de los certificados de la cadena de certificados aparece en la lista de revocación, detenga.
3.  Obtiene la clave pública RSA de la cadena de certificados.

**Inicializar la sesión COPP**

1.  Genere una clave de sesión AES de 128 bits. Esta clave se usa para firmar datos y para comprobar que los datos firmados no se han alterado.
2.  Genera dos números aleatorios de 32 bits criptográficamente seguros. El primero es un número de secuencia de estado y el segundo es un número de secuencia de comandos. Cada vez que la aplicación envía un comando o una solicitud de estado, incrementa el número de secuencia correspondiente e incluye este número en el comando COPP o en los datos de la solicitud.
3.  Concatene el número aleatorio de 128 bits del controlador de gráficos, la clave de sesión AES, el número de secuencia de estado y el número de secuencia de comandos. Cifre esta matriz de bytes mediante la clave pública del controlador y pase el resultado a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).

**Enviar comandos COPP y solicitudes de estado**

1.  Consulte los tipos de protección disponibles y otra información mediante una llamada a [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).
2.  Establezca los niveles de protección deseados llamando a [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).
3.  Consulta periódicamente el nivel de protección local actual. Detener la reproducción si el nivel de protección local cambia de forma inesperada o si se detecta un problema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



