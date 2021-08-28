---
title: Exportar contenido comprimido
description: Exportar contenido comprimido
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows SDK de formato multimedia, exportación de DRM
- Windows SDK de formato multimedia, exportación
- Windows SDK de formato multimedia, contenido comprimido
- digital rights management (DRM),export
- DRM (administración de derechos digitales), exportación
- administración de derechos digitales (DRM), contenido comprimido
- DRM (administración de derechos digitales), contenido comprimido
- API extendidas de cliente DRM, contenido comprimido
- API extendidas de cliente, contenido comprimido
- API extendidas de cliente DRM, exportación
- API extendidas de cliente, exportación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e7e8e6d71e4104d65336b131d0e15d5eaedd8b2fba4b7715f5e60aa6083544
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055505"
---
# <a name="exporting-compressed-content"></a>Exportar contenido comprimido

En esta sección se describe cómo exportar Windows multimedia protegido con DRM multimedia en un archivo Windows Media donde la aplicación recibe datos multimedia digitales comprimidos. Para ello, la aplicación debe realizar el descifrado en línea de todas las cargas cifradas Windows DRM multimedia en un archivo ASF.

> [!Note]  
> Se proporciona una biblioteca de análisis de ASF como parte del Windows de exportación de DRM multimedia.

 

Los pasos principales implicados en la exportación de contenido comprimido son:

1.  Realice la individualización de DRM, si es necesario.
2.  Compruebe que el esquema de protección de contenido de destino está permitido explícitamente.
3.  Cree un objeto descifrador para descifrar cada carga de ASF.
4.  El sistema DRM transcircue cada carga de ASF Windows DRM multimedia en RC4 antes de pasarla a la aplicación.

Si la aplicación cambia el tamaño de una carga de ASF durante la transcryption, también debe volver amultiplicar el archivo ASF.

Pase a la biblioteca de código auxiliar un Windows de aplicación de exportación de DRM multimedia. Se comprueba el certificado y, si es válido, el sistema DRM genera un vector de inicialización y lo cifra mediante RSA OAEP.

-   Se crea una clave de sesión RC4 para cada carga mediante la concatenación del vector de inicialización y un valor salt. Proporcione el valor salt a la API de descifrado y debe incrementarlo en un valor entero positivo distinto de cero para cada carga.

Microsoft le proporciona una herramienta como parte del contrato de exportación de DRM de Windows Media que le permitirá generar su propio par de claves rsa pública y privada. Enviará la clave pública a Microsoft, donde Microsoft la incorporará en un certificado Windows aplicación DRM multimedia firmado y lo devolverá.

Cada carga, después de descifrarse mediante la clave de descifrado RC4, debe cifrarse inmediatamente en la CPS de salida. Existen otras restricciones en el control de cargas sin cifrar que se describen en las reglas de solidez y cumplimiento, que acompañan al contrato de exportación de DRM de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Descifrado y nuevo cifrado de carga de ASF**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**Exportación de DRM**](drm-export.md)
</dt> <dt>

[**Realización de la individualización de DRM**](performing-drm-individualization.md)
</dt> <dt>

[**Comprobación e inicialización**](verification-and-initialization.md)
</dt> </dl>

 

 




