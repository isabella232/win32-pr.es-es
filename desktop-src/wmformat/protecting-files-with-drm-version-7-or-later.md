---
title: Protección de archivos con DRM versión 7 o posterior
description: Protección de archivos con DRM versión 7 o posterior
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows SDK de formato multimedia, creación de archivos protegidos
- Windows SDK de formato multimedia, archivos protegidos
- Formato de sistemas avanzados (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Formato de sistemas avanzados (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Formato de sistemas avanzados (ASF),WMStubDRM.lib
- ASF (formato de sistemas avanzados),WMStubDRM.lib
- WMStubDRM.lib, crear archivos protegidos
- WMStubDRM.lib,archivos protegidos
- digital rights management (DRM),WMStubDRM.lib
- DRM (administración de derechos digitales),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466688"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protección de archivos con DRM versión 7 o posterior

Para proteger los archivos con Windows Drm multimedia versión 7 o posterior, use el método [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) del objeto de escritura para establecer atributos DRM. Dado que la versión 7 y posteriores de DRM habilitan licencias únicas para cada archivo o conjunto de archivos protegidos, la interfaz **IWMDRMWriter** también tiene métodos para crear claves. Estos métodos solo se proporcionan para mayor comodidad.

Para proteger los archivos ASF mediante DRM versión 7 o posterior, realice los pasos siguientes:

1.  Vincule a WMStubDRM.lib y, si es necesario, desvincule wmvcore.lib.
2.  Llame a [**la función WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para crear el sistema de escritura DRM. El primer argumento está reservado y debe establecerse en **NULL.**
3.  Establezca un perfil para que el escritor lo use mediante una llamada a [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Debe establecer un perfil en el sistema de escritura antes de establecer los atributos drm. DRM solo se admite para perfiles que usan los códecs Windows Media Audio o Windows Media Video
4.  Obtenga la interfaz [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) del objeto de escritura.
5.  Llame [**a IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) y establezca [**Usar DRM \_ \_ avanzado**](use-advanced-drm.md) en **TRUE.**
6.  Si necesita generar un nuevo valor de ed. de clave, llame a [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). En la mayoría de los casos, volverá a usar un valor de ed. de clave que se generó anteriormente. Este valor debe permanecer como secreto; no se escribe en el archivo.
7.  Llame [**a IWMDRMWriter::GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) para crear un identificador de clave, que es el segundo valor usado para crear la clave real. A diferencia del valor de ed. de clave, el identificador de clave es público y se escribe en el archivo en el encabezado DRM sin borrar. Cree un nuevo identificador de clave para cada nuevo archivo que cree.
8.  Llame a **IWMDRMWriter::GenerateSigningKeyPair** si es necesario para generar una clave pública y privada que se usará para firmar el objeto de encabezado ASF de DRM avanzado. Para obtener más información sobre estas claves, vea [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Si es necesario, obtenga los valores para rellenar el objeto de firma digital del encabezado DRM. Si no tiene una versión de trabajo de Windows Media Rights Manager instalada en el sistema, debe configurar el objeto de firma digital del encabezado de archivo de ASF especificando los cuatro atributos siguientes, que todos deben obtenerse de Microsoft:

    -   [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)
    -   [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)
    -   [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)
    -   [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)

    Si tiene instalado Windows Media Rights Manager, no es necesario establecer estos atributos en la aplicación. El componente DRM recuperará estos atributos y los usará para firmar el encabezado automáticamente. Si tiene una versión activada de Windows Media Rights Manager en otro equipo y desea reutilizar esos valores de objeto de firma digital, puede encontrarlos en el Registro. El certificado del servidor de licencias se almacena en HKEY LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server Certs:cert1 y el certificado raíz se almacena en \_ \_ \\ \\ \\ \\ \\ HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert2. Al proteger archivos con DRM versión 7, debe usar los valores de estas claves del Registro. Para la propiedad **\_ DRM LASignaturePrivKey**, use **GenerateSigningKeysEx** (a través del SDK de Media Rights Manager de Windows) o bien reutilice el valor instalado por Windows Media Rights Manager en HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License \_ \\ \\ \\ \\ Server:Info \_ Cert0. Para la propiedad **\_ DRM LASignatureCert,** use **GenerateSigningKeysEx** (a través del SDK de Windows Media Rights Manager) o bien el valor instalado por Windows Media Rights Manager en HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert0.

10. Llame [**a IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) tantas veces como sea necesario para configurar el objeto de escritor, lo que establecerá los atributos de encabezado DRM necesarios según sea necesario. Estas propiedades se conservan durante la duración del objeto de escritor o hasta que se restablecen con un nuevo valor. No es necesario restablecerlo para cada archivo nuevo que cree.

    El objeto de escritor requiere las siguientes propiedades:

    -   [**Encabezado \_ DRMSignPrivKey**](drm-headersignprivkey.md)
    -   [**DRM \_ KeySeed**](drm-keyseed.md)
    -   [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)
    -   [**DRM \_ KeyID**](drm-keyid.md)
    -   [**Licencia \_ de DRMAcqURL**](drm-licenseacqurl.md)

    Las siguientes propiedades son opcionales:

    -   [**ContentID de DRM \_**](drm-contentid.md)
    -   [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)

    Además, puede especificar atributos de archivo DRM definidos por el usuario directamente mediante el atributo base [**\_ DRMHeader de DRM.**](drm-drmheader.md) Puede agregar cualquier atributo adicional que desee, como "DRMHeader.RequireSAP", por ejemplo, como una manera de comunicar información adicional que usará el servidor de licencias al crear la licencia. El servidor de licencias debe tener en cuenta de antemano las propiedades adicionales que agregue. No hay ninguna manera de detectar propiedades desconocidas mediante programación.

11. Escriba el archivo mediante los métodos [**de interfaz IWMWriter,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) como se describe en otra parte de esta documentación. Para crear una secuencia DRM en vivo, simplemente escriba en un receptor de red. También puede escribir en un receptor de inserción.
12. Si es necesario, cree una licencia para el archivo mediante Windows Media Rights Manager. Esta tarea también la puede realizar un servidor de licencias de terceros. En escenarios de DRM en vivo, los usuarios finales tendrán que obtener una licencia antes de que comience la secuencia o, de lo contrario, en el momento en que intenten conectarse por primera vez a ella.

**Nota** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**IWMDRMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Lectura de archivos protegidos**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




