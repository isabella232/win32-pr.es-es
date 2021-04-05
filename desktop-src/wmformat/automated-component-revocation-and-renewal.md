---
title: Revocación y renovación de componentes automatizados
description: Revocación y renovación de componentes automatizados
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- SDK de Windows Media Format, revocación automatizada y renovación
- SDK de Windows Media Format, revocación
- SDK de Windows Media Format, renovación
- Administración de derechos digitales (DRM), revocación automatizada y renovación
- DRM (administración de derechos digitales), revocación automatizada y renovación
- Administración de derechos digitales (DRM), revocación
- DRM (administración de derechos digitales), revocación
- Administración de derechos digitales (DRM), renovación
- DRM (administración de derechos digitales), renovación
- API extendidas del cliente DRM, revocación automatizada y renovación
- API extendidas de cliente, revocación automatizada y renovación
- API extendidas del cliente DRM, revocación
- API extendidas de cliente, revocación
- API extendidas del cliente DRM, renovación
- API extendidas de cliente, renovación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359262"
---
# <a name="automated-component-revocation-and-renewal"></a>Revocación y renovación de componentes automatizados

Microsoft puede revocar las aplicaciones o los componentes de software considerados en peligro. La API extendida cliente de Windows Media Format proporciona un mecanismo para la revocación automatizada y la renovación de componentes.

Los componentes revocados se enumeran en una lista de revocación de certificados, publicada por Microsoft. Cuando se revoca un componente, su certificado se agrega a la lista de revocación de certificados y se actualiza el BLOB de información de revocación ( \_ información de revisión) en los servidores de Microsoft.

Para realizar la revocación y renovación automatizadas cuando un usuario intenta procesar contenido protegido con DRM de Windows Media, la aplicación debe hacer lo siguiente:

1.  Extraiga la \_ versión de la información de Rev de la licencia. El número de versión de la información de REV \_ se encuentra en la siguiente ubicación en una licencia de XMR:
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  Compare el \_ número de versión de la información de revisión de la licencia con el \_ número de versión de la información de revisión en el almacén local llamando al método [**IWMDRMSecurity:: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .
3.  Si la versión de la información de REV \_ no está actualizada, llame al método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , pasando la \_ \_ \_ \_ marca de actualización de revocación de la ejecución de WMDRM Security en el parámetro *dwFlags* .
4.  Recupere la lista de revocación de certificados del almacén local llamando al método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
5.  Analice la lista de revocación y compruebe si hay revocación de DRM de Windows Media. Para obtener más información, consulte Comprobación de la [revocación de certificados](checking-certificate-revocation.md).
6.  Si hay alguna revocación de DRM de Windows Media:
    1.  Cree un habilitador de contenido para renovar los componentes revocados llamando al método [**IWMDRMSecurity:: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .
    2.  Llame a **IMFContentEnabler:: AutomaticEnable** , que dirige al usuario a una dirección URL que contiene información sobre la renovación de componentes. Este método se documenta en el [SDK de Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .
        > [!Note]  
        > Debe aclarar este proceso al usuario mediante el uso de una declaración de privacidad, ya que el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.

         

    3.  Si es posible, el usuario renovará el componente desde la dirección URL, ya sea de forma automática o mediante instrucciones específicas. Habrá algunas situaciones en las que el componente no se puede renovar.
    4.  Intente obtener acceso al contenido de nuevo hasta que no haya más revocación o se detenga el proceso por alguna razón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 