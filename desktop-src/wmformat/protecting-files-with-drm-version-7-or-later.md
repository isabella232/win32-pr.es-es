---
title: Protección de archivos con DRM versión 7 o posterior
description: Protección de archivos con DRM versión 7 o posterior
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- SDK de Windows Media Format, crear archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, crear archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704915"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protección de archivos con DRM versión 7 o posterior

Para proteger archivos con Windows Media DRM versión 7 o posterior, use el método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) del objeto Writer para establecer los atributos DRM. Dado que la versión 7 de DRM y las versiones posteriores habilitan licencias únicas para cada archivo o conjunto de archivos protegido, la interfaz **IWMDRMWriter** también tiene métodos para crear claves. Estos métodos se proporcionan solo para su comodidad.

Para proteger los archivos ASF con DRM versión 7 o posterior, realice los pasos siguientes:

1.  Vincule a WMStubDRM. lib y, si es necesario, desvincule wmvcore. lib.
2.  Llame a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para crear el escritor DRM. El primer argumento está reservado y debe establecerse en **null**.
3.  Establezca un perfil para que lo use el escritor llamando a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Debe establecer un perfil en el escritor antes de establecer cualquier atributo DRM. DRM solo es compatible con los perfiles que usan los códecs Windows Media Audio o Windows Media Video
4.  Obtenga la interfaz [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) del objeto del escritor.
5.  Llame a [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y [**establezca \_ usar \_ DRM avanzada**](use-advanced-drm.md) en **true**.
6.  Si necesita generar un nuevo inicialización de clave, llame a [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). En la mayoría de los casos, volverá a usar una inicialización de clave que se generó anteriormente. Este valor debe ser secreto; no se escribe en el archivo.
7.  Llame a [**IWMDRMWriter:: GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) para crear un identificador de clave, que es el segundo valor que se usa para crear la clave real. A diferencia de la inicialización de clave, el identificador de clave es público y se escribe en el archivo del encabezado DRM en el borrado. Cree un nuevo ID. de clave para cada nuevo archivo que cree.
8.  Llame a **IWMDRMWriter:: GenerateSigningKeyPair** si es necesario para generar una clave pública y privada que se utilizará para firmar el objeto de encabezado ASF de DRM avanzado. Para obtener más información sobre estas claves, vea [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Si es necesario, obtenga los valores para rellenar el objeto de firma digital del encabezado DRM. Si no tiene una versión de trabajo de Windows Media Rights Manager instalada en el sistema, debe configurar el objeto de firma digital del encabezado de archivo ASF especificando los cuatro atributos siguientes, que se deben obtener de Microsoft:

    -   [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)
    -   [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)
    -   [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)
    -   [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)

    Si tiene instalado Windows Media Rights Manager, no es necesario establecer estos atributos en la aplicación. El componente DRM recuperará estos atributos y los usará para firmar el encabezado automáticamente. Si tiene una versión activada de Windows Media Rights Manager en otro equipo y desea volver a usar esos valores de objeto de firma digital, puede encontrarlos en el registro. El certificado del servidor de licencias se almacena en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert1 y el certificado raíz se almacena en \_ HKEY \_ local \\ Machine software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert2. Al proteger archivos con DRM versión 7, debe usar los valores de estas claves del registro. Para la **\_ propiedad LASignaturePrivKey de DRM**, use **GenerateSigningKeysEx** (a través del SDK de Windows Media Rights Manager) o bien vuelva a usar el valor instalado por Windows Media Rights Manager en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server: info \_ Cert0. Para la **propiedad \_ LASignatureCert de DRM** , use **GenerateSigningKeysEx** (a través del SDK de Windows Media Rights Manager) o bien el valor instalado por el administrador de derechos de Windows Media en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert0.

10. Llame a [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) tantas veces como sea necesario para configurar el objeto de escritor, que establecerá los atributos de encabezado DRM necesarios según sea necesario. Estas propiedades se conservan durante la vigencia del objeto escritor o hasta que se restablecen con un nuevo valor. No es necesario que se restablezcan para cada nuevo archivo que cree.

    El objeto escritor requiere las siguientes propiedades:

    -   [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)
    -   [**\_KEYSEED DRM**](drm-keyseed.md)
    -   [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)
    -   [**ID. de ID \_ de DRM**](drm-keyid.md)
    -   [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)

    Las siguientes propiedades son opcionales:

    -   [**ContentID de DRM \_**](drm-contentid.md)
    -   [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)

    Además, puede especificar atributos de archivo DRM definidos por el usuario directamente mediante el atributo base [**\_ DRMHeader de DRM**](drm-drmheader.md) . Puede agregar cualquier atributo adicional que desee, como "DRMHeader. RequireSAP", por ejemplo, como una forma de comunicar información adicional que usará el servidor de licencias para crear la licencia. El servidor de licencias debe ser consciente de las propiedades adicionales que agregue. No hay ninguna manera de detectar propiedades desconocidas mediante programación.

11. Escriba el archivo mediante los métodos de la interfaz [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) tal y como se describe en esta documentación. Para crear una secuencia de DRM dinámica, simplemente escriba en un receptor de red. También puede escribir en un receptor de inserciones.
12. Si es necesario, cree una licencia para el archivo mediante el administrador de derechos de Windows Media. Esta tarea también puede realizarla un servidor de licencias de terceros. En el caso de escenarios de DRM activo, los usuarios finales deberán obtener una licencia antes de que se inicie la secuencia o, en el momento en el que intenten conectarse a ella por primera vez.

**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Lista de atributos de DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Interfaz IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Leer archivos protegidos**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




