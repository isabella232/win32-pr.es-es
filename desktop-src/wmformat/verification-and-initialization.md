---
title: Comprobación e inicialización
description: Comprobación e inicialización
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, comprobación
- SDK de Windows Media Format, inicialización
- Administración de derechos digitales (DRM), comprobación
- DRM (administración de derechos digitales), comprobación
- Administración de derechos digitales (DRM), inicialización
- DRM (administración de derechos digitales), inicialización
- API extendidas del cliente DRM, comprobación
- API extendidas del cliente, comprobación
- API extendidas del cliente DRM, inicialización
- API extendidas de cliente, inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358698"
---
# <a name="verification-and-initialization"></a>Comprobación e inicialización

Debe realizar los pasos siguientes para comprobar que se permite el descifrado e inicializar un objeto que descifrará el contenido:

1.  Si ya tiene el identificador de clave para el contenido, vaya al paso 5.
2.  Llame a la función [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) para crear un objeto de editor de metadatos y obtener una instancia de la interfaz [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) de ese objeto.
3.  Llame a **IWMMetadataEditor:: QueryInterface** para obtener una instancia de la interfaz [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .
4.  Llame a [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) para obtener la propiedad de ID. de la **\_ DRMHeader \_ de DRM** .
5.  Inicialice las API extendidas del cliente DRM de Windows Media mediante una llamada a la función [**WMDRMStartup**](wmdrmstartup.md) .
6.  Llame a la función [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) para crear un objeto de proveedor seguro y obtener una instancia de la interfaz [**IWMDRMProvider**](iwmdrmprovider.md) de ese objeto.
7.  Llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md) para crear un objeto de administración de licencias y obtener una instancia de su interfaz [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .
8.  Llame a [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), pasando el identificador de clave y el derecho que rige las acciones que se van a llevar a cabo con el contenido después de que se haya transcifrado. Esta llamada recuperará una instancia de la interfaz [**IWMDRMLicense**](iwmdrmlicense.md) que se puede usar para enumerar a través de las licencias coincidentes.
9.  Llame a [**IWMDRMLicense:: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) para recuperar la lista de sistemas de protección de contenido (CPS) autorizados según lo especificado por el emisor de la licencia.
10. Analice la lista de inclusión para confirmar que la licencia permite el GUID de la CPS de salida.
11. Si el GUID de exportación deseado no está en la lista de inclusión, llame a [**IWMDRMLicense:: Getnext**](iwmdrmlicense-getnext.md) para obtener la siguiente licencia aplicable (si existe) y repita los pasos 9 y 10. Si ninguna licencia tiene el GUID deseado en su lista de inclusión, no se puede realizar la exportación.
12. Llame a [**IWMDRMLicense:: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) para crear un objeto descifrador. Pase el certificado de la aplicación de exportación. Esta llamada proporcionará un puntero a una instancia de la interfaz [**IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto descifrador y un objeto binario que contiene el valor de inicialización. En este momento solo se admite la constante **RC4 del \_ tipo de protección \_ \_ DRM** de Windows Media como argumento para el parámetro *dwFlags* .
13. Use el esquema de cifrado RSA OAEP para descifrar el vector de inicialización.
14. Use la biblioteca de análisis de ASF proporcionada por Microsoft al entrar en el contrato de exportación de DRM de Windows Media para buscar el desplazamiento en bytes para cada carga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Exportar contenido comprimido**](exporting-compressed-content.md)
</dt> </dl>

 

 




