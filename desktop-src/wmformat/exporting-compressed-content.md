---
title: Exportar contenido comprimido
description: Exportar contenido comprimido
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- SDK de Windows Media Format, exportación de DRM
- SDK de Windows Media Format, exportar
- SDK de Windows Media Format, contenido comprimido
- Administración de derechos digitales (DRM), exportar
- DRM (administración de derechos digitales), exportar
- Administración de derechos digitales (DRM), contenido comprimido
- DRM (administración de derechos digitales), contenido comprimido
- API extendidas del cliente DRM, contenido comprimido
- API extendidas de cliente, contenido comprimido
- API extendidas del cliente DRM, exportar
- API extendidas del cliente, exportar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903361"
---
# <a name="exporting-compressed-content"></a>Exportar contenido comprimido

En esta sección se describe la exportación de medios protegidos con DRM de Windows Media en un archivo de Windows Media en el que la aplicación recibe datos de medios digitales comprimidos. Para ello, la aplicación debe realizar el descifrado alineado de todas las cargas cifradas de DRM de Windows Media en un archivo ASF.

> [!Note]  
> Se le proporciona una biblioteca de análisis ASF como parte del contrato de exportación DRM de Windows Media.

 

Los pasos principales implicados en la exportación de contenido comprimido son:

1.  Realice una individualización de DRM, si es necesario.
2.  Compruebe que el esquema de protección de contenido de destino está permitido explícitamente.
3.  Cree un objeto descifrador para descifrar cada carga de ASF.
4.  El sistema DRM transmite cada carga ASF de Windows Media DRM a RC4 antes de pasarla a la aplicación.

Si la aplicación cambia el tamaño de una carga ASF durante el transcifrado, también debe remultiplexar el archivo ASF.

Pase a la biblioteca de código auxiliar un certificado de aplicación de exportación de DRM de Windows Media. Se comprueba el certificado y, si es válido, el sistema DRM genera un vector de inicialización y lo cifra mediante RSA OAEP.

-   Se crea una clave de sesión RC4 para cada carga mediante la concatenación del vector de inicialización y un valor Salt. Proporcione el valor Salt a la API de descifrado y debe incrementarlo mediante un valor entero positivo distinto de cero para cada carga.

Microsoft le proporcionará una herramienta como parte del contrato de exportación de Windows Media DRM que le permitirá generar su propio par de claves pública y privada RSA. Enviará la clave pública a Microsoft, donde Microsoft la incorporará a un certificado de aplicación DRM de Windows Media firmado y lo devolverá.

Cada carga, una vez descifrada con la clave de descifrado RC4, debe cifrarse inmediatamente en la CPS de salida. Existen otras restricciones en el control de cargas no cifradas que se describen en las reglas de solidez y cumplimiento, que acompañan al contrato de exportación de Windows Media DRM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Descifrado y recifrado de carga ASF**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**Exportación de DRM**](drm-export.md)
</dt> <dt>

[**Realización de una individualización DRM**](performing-drm-individualization.md)
</dt> <dt>

[**Comprobación e inicialización**](verification-and-initialization.md)
</dt> </dl>

 

 




