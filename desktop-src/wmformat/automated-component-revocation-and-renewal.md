---
title: Revocación y renovación automatizadas de componentes
description: Revocación y renovación automatizadas de componentes
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows SDK de formato multimedia, revocación y renovación automatizadas
- Windows SDK de formato multimedia, revocación
- Windows SDK de formato multimedia, renovación
- administración de derechos digitales (DRM), revocación y renovación automatizadas
- DRM (administración de derechos digitales), revocación y renovación automatizadas
- administración de derechos digitales (DRM), revocación
- DRM (administración de derechos digitales), revocación
- administración de derechos digitales (DRM),renovación
- DRM (administración de derechos digitales), renovación
- API extendidas de cliente DRM, revocación y renovación automatizadas
- API extendidas de cliente, revocación y renovación automatizadas
- API extendidas de cliente DRM, revocación
- API extendidas de cliente, revocación
- API extendidas de cliente DRM, renovación
- API extendidas de cliente, renovación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebc8fd9a9b01d14e859afa88844bb98bd1c3e2cdda00fb1d14d0135612203b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705201"
---
# <a name="automated-component-revocation-and-renewal"></a>Revocación y renovación automatizadas de componentes

Microsoft puede revocar las aplicaciones de software o los componentes que se consideran en peligro. La API extendida Windows media format client proporciona un mecanismo para la revocación y renovación automatizadas de componentes.

Los componentes revocados se enumeran en una lista de revocación de certificados, publicada por Microsoft. Cuando se revoca un componente, su certificado se agrega a la lista de revocación de certificados y el blob de información de revocación (REV INFO) se actualiza en \_ los servidores de Microsoft.

Para realizar la revocación y renovación automatizadas cuando un usuario intenta procesar Windows contenido protegido con DRM multimedia, la aplicación debe hacer lo siguiente:

1.  Extraiga la versión \_ de REV INFO de la licencia. El número de \_ versión de REV INFO se encuentra en la siguiente ubicación en una licencia XMR:
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

    

2.  Compare el número de versión de REV INFO de la licencia con el número de versión de REV INFO en el almacén local mediante una llamada al método \_ \_ [**IWMDRMSecurity::GetRevocationDataVersion.**](iwmdrmsecurity-getrevocationdataversion.md)
3.  Si la versión de REV INFO no está actualizada, llame al método \_ [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) y pase la marca WMDRM SECURITY PERFORM REVOCATION REFRESH en el \_ \_ parámetro \_ \_ *dwFlags.*
4.  Recupere la lista de revocación de certificados del almacén local llamando al [**método IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)
5.  Analice la lista de revocación y compruebe si hay Windows drm multimedia. Para obtener más información, vea [Comprobar la revocación de certificados.](checking-certificate-revocation.md)
6.  Si hay alguna revocación Windows DRM multimedia:
    1.  Cree un habilitador de contenido para renovar los componentes revocados mediante una llamada al método [**IWMDRMSecurity::GetContentEnablersForRevocations.**](iwmdrmsecurity-getcontentenablersforrevocations.md)
    2.  Llame **a IMFContentEnabler::AutomaticEnable,** que dirige al usuario a una dirección URL que contiene información de renovación de componentes. Este método se documenta en el SDK [Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .
        > [!Note]  
        > Debe aclarar este proceso al usuario mediante el uso de una declaración de privacidad porque el proceso de actualización envía información desde el equipo cliente a un sitio web de Microsoft.

         

    3.  Si es posible, el usuario renovará el componente desde la dirección URL, ya sea automáticamente o siguiendo instrucciones específicas. Habrá algunas situaciones en las que no se puede renovar el componente.
    4.  Intente acceder al contenido de nuevo hasta que no haya más revocaciones o el proceso se detenga por algún motivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 