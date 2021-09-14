---
description: Obtención de la cadena de certificados de controladores
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Obtención de la cadena de certificados de controladores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362387"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Obtención de la cadena de certificados de controladores

Para usar el Protocolo de protección de salida certificado (COPP), la aplicación debe crear primero un gráfico de DirectShow que incluya el filtro de representación de mezcla de vídeo (VMR-7 o VMR-9). El filtro de representador de vídeo anterior no admite COPP. Antes de llamar a cualquier método COPP, la aplicación debe crear un gráfico de reproducción de vídeo y conectar el descodificador al pin de entrada del filtro VMR. No es necesario reproducir el archivo de vídeo.

Después de compilar el gráfico, consulte el VMR para la interfaz [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) y, a continuación, llame a [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Este método devuelve un número aleatorio de 128 bits con tipo GUID, junto con un puntero a una matriz de bytes que contiene la cadena de certificados XML del controlador en formato UTF-8. El código siguiente muestra cómo obtener la cadena de certificados.


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

[Uso del Protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



