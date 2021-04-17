---
title: Creación e inicialización de un escritor DRM
description: Creación e inicialización de un escritor DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- SDK de Windows Media Format, escritores de DRM
- Administración de derechos digitales (DRM), creación de escritores DRM
- DRM (administración de derechos digitales), creación de escritores DRM
- Administración de derechos digitales (DRM), inicializando escritores de DRM
- DRM (administración de derechos digitales), inicializar escritores de DRM
- API extendidas del cliente DRM, escritores de DRM
- API extendidas de cliente, escritores de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105705063"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Creación e inicialización de un escritor DRM

Los pasos siguientes son necesarios para inicializar un objeto de escritor ASF para importar ejemplos de medios cifrados en Windows Media DRM.

1.  Siga los pasos del 1 al 4 de importación de la [licencia y el material de clave](importing-license-and-key-material.md).
2.  Cree e inicialice un objeto de escritura ASF con el material de clave DRM de Windows Media adecuado. Para obtener más información, consulte [Habilitar la compatibilidad con DRM](enabling-drm-support.md).
3.  Establezca cada uno de los atributos siguientes llamando a [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):
    -   \_HEADERSIGNPRIVKEY DRM
    -   \_V1LICENSEACQURL DRM
    -   ID. de ID \_ de DRM
    -   \_LICENSEACQURL DRM
4.  Si una versión con licencia de Windows Media Rights Manager no está instalada en el equipo que ejecuta el software, también se deben establecer los cuatro atributos siguientes:
    -   \_LASIGNATUREROOTCERT DRM
    -   \_LASIGNATURECERT DRM
    -   \_LASIGNATURELICSRVCERT DRM
    -   \_LASIGNATUREPRIVKEY DRM
    -   La aplicación para los certificados de cifrado necesarios se puede completar rellenando el [contrato de licencia de Windows Media (WMLA)](https://www.microsoft.com/licensing/default) en línea.
5.  Cree una clave de sesión y rellene una estructura de claves de la [**\_ sesión de importación de \_ \_ WMDRM**](wmdrm-import-session-key.md) . La clave de sesión se utilizará para cifrar una clave de contenido. Para obtener un ejemplo, consulte el ejemplo de cómo [crear una clave de sesión](create-session-key-example.md).
6.  Cree una clave de contenido a partir de un vector de inicialización de RC4 aleatorio y rellene una estructura de [**clave de contenido de importación de WMDRM \_ \_ \_**](wmdrm-import-content-key.md) . La clave de contenido se usa para cifrar los ejemplos de medios. Para obtener un ejemplo, consulte el ejemplo de creación de una [clave de contenido](create-content-key-example.md).
7.  Cifre la clave de contenido con la clave de sesión mediante el cifrado RC4.
8.  Extraiga la clave de la colección de certificados de la máquina. Para obtener un ejemplo, consulte [Get Machine Certificate example](get-machine-certificate-example.md).
9.  Cifre la clave de sesión con la clave pública extraída del certificado.
10. Rellene una estructura de struct de la [**\_ importación del \_ inicializador \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .
11. Llame al método [**IWMDRMWriter3:: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) para notificar al SDK que los ejemplos que entran en el escritor ya están protegidos y deben enviarse directamente al cliente DRM de Windows Media para la importación.
12. Llame a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

El resto de los pasos para crear un archivo protegido con DRM se documentan en la guía de programación del SDK de Windows Media Format. Para obtener más información, vea [crear archivos protegidos](creating-protected-files.md).

El siguiente paso consiste en recorrer en iteración cada ejemplo multimedia, cifrarlo y pasarlo al objeto escritor. Para obtener más información, consulte los [ejemplos de cifrado e importación de medios](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




