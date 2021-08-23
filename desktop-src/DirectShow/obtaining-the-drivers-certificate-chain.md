---
description: Obtención de la cadena de certificados de controladores
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Obtención de la cadena de certificados de controladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2641c27c3d24ab45a87b16e8c805228c316d9f89428cd29abbaff347b5aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684565"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Obtención de la cadena de certificados de controladores

Para usar el Protocolo de protección de salida certificado (COPP), la aplicación primero debe crear un gráfico de DirectShow que incluya el filtro de representación de mezcla de vídeo (VMR-7 o VMR-9). El filtro De representador de vídeo anterior no admite COPP. Antes de llamar a cualquier método COPP, la aplicación debe crear un gráfico de reproducción de vídeo y conectar el descodificador al pin de entrada del filtro de VMR. No es necesario reproducir el archivo de vídeo.

Después de compilar el gráfico, consulte vmr para la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) y, a continuación, llame a [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Este método devuelve un número aleatorio de 128 bits con tipo GUID, junto con un puntero a una matriz de bytes que contiene la cadena de certificados XML del controlador en formato UTF-8. El código siguiente muestra cómo obtener la cadena de certificados.


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



