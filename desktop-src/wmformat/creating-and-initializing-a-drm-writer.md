---
title: Creación e inicialización de un sistema de escritura DRM
description: Creación e inicialización de un sistema de escritura DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows SDK de formato multimedia, escritores DRM
- administración de derechos digitales (DRM), creación de escritores DRM
- DRM (administración de derechos digitales), creación de escritores DRM
- administración de derechos digitales (DRM), inicialización de escritores DRM
- DRM (administración de derechos digitales), inicialización de escritores DRM
- API extendidas de cliente DRM, escritores DRM
- API extendidas de cliente, escritores DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24067e082de38bc396153be918025e2608246e39185c45eaa84bfe0e5c02407
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007055"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Creación e inicialización de un sistema de escritura DRM

Los pasos siguientes son necesarios para inicializar un objeto de escritor de ASF para importar ejemplos de medios cifrados Windows DRM multimedia.

1.  Siga los pasos 1 a 4 de [Importar licencias y material de clave.](importing-license-and-key-material.md)
2.  Cree e inicialice un objeto de sistema de escritura de ASF con el Windows de clave DRM multimedia adecuado. Para obtener más información, consulte [Habilitación de la compatibilidad con DRM.](enabling-drm-support.md)
3.  Establezca cada uno de los atributos siguientes llamando a [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):
    -   Encabezado \_ DRMSignPrivKey
    -   DRM \_ V1LicenseAcqURL
    -   DRM \_ KeyID
    -   DRM \_ LicenseAcqURL
4.  Si una versión con licencia de Windows Media Rights Manager no está instalada en el equipo que ejecuta el software, también se deben establecer los cuatro atributos siguientes:
    -   DRM \_ LASignatureRootCert
    -   DRM \_ LASignatureCert
    -   DRM \_ LASignatureLicSrvCert
    -   DRM \_ LASignaturePrivKey
    -   La aplicación para los certificados de cifrado necesarios se puede completar rellenando el Windows de licencias multimedia [(WMLA)](https://www.microsoft.com/licensing/default) en línea.
5.  Cree una clave de sesión y rellene una [**estructura WMDRM \_ IMPORT SESSION \_ \_ KEY.**](wmdrm-import-session-key.md) La clave de sesión se usará para cifrar una clave de contenido. Para obtener un ejemplo, vea [Create Session Key Example](create-session-key-example.md).
6.  Cree una clave de contenido a partir de un vector de inicialización RC4 aleatorio y rellene una estructura DE CLAVE DE [**CONTENIDO \_ DE IMPORTACIÓN \_ DE \_ WMDRM.**](wmdrm-import-content-key.md) La clave de contenido se usa para cifrar los ejemplos multimedia. Para obtener un ejemplo, vea [Create Content Key Example](create-content-key-example.md).
7.  Cifre la clave de contenido con la clave de sesión mediante el cifrado RC4.
8.  Extraiga la clave de recopilación de certificados de máquina. Para obtener un ejemplo, vea [Obtener el ejemplo de certificado de máquina.](get-machine-certificate-example.md)
9.  Cifre la clave de sesión con la clave pública extraída del certificado.
10. Rellene una estructura [**\_ \_ \_ STRUCT WMDRM IMPORT INIT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)
11. Llame al método [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) para notificar al SDK que los ejemplos que llegan al sistema de escritura ya están protegidos y deben enviarse directamente al cliente DRM de Windows Media para su importación.
12. Llame [**a IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Los pasos restantes para crear un archivo protegido con DRM se documentan en la guía Windows programación del SDK de formato multimedia. Para obtener más información, vea [Crear archivos protegidos.](creating-protected-files.md)

El siguiente paso consiste en recorrer en iteración cada ejemplo multimedia, cifrarlo y pasarlo al objeto de escritor. Para obtener más información, vea Los ejemplos [de cifrado e importación de medios](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




