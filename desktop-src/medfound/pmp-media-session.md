---
description: Sesión multimedia de PMP
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: Sesión multimedia de PMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf2cb1ff173d6fd085f6e98dd4608c84ff40200
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580236"
---
# <a name="pmp-media-session"></a>Sesión multimedia de PMP

Una aplicación puede crear la [sesión multimedia en](media-session.md) un proceso independiente denominado proceso de ruta [de](protected-media-path.md) acceso multimedia protegida (PMP). El propósito principal del proceso de PMP es habilitar la reproducción de contenido protegido mediante la administración de derechos digitales (DRM). De forma predeterminada, el proceso PMP se crea dentro de un entorno protegido (PE). Solo se pueden cargar componentes firmados de confianza dentro de un PE. Una ventaja secundaria del proceso de PMP es que aísla el proceso de aplicación de la canalización multimedia. Para obtener más información sobre el proceso de PMP, vea [Protected Media Path](protected-media-path.md).

Para crear la sesión multimedia dentro del proceso PMP, llame a la [**función MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) Opcionalmente, puede pasar la marca **MFPMPSESSION \_ UNPROTECTED \_ PROCESS.** Si se establece esta marca, el proceso PMP se crea dentro de un proceso no protegido y no en un proceso PE. El proceso no protegido no se puede usar para la reproducción drm, pero proporciona las ventajas del aislamiento de procesos.

La [**función MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) devuelve un puntero a un objeto proxy para la sesión multimedia. La aplicación se comunica con la sesión multimedia a través del proxy.

![ilustración de la sesión multimedia dentro del proceso pmp](images/pmp01.png)

De forma predeterminada, cuando la aplicación crea una topología, el origen multimedia se crea dentro del proceso de aplicación. Se crea un proxy para el origen de medios dentro del proceso PMP. El origen multimedia puede crear objetos dentro del proceso PMP mediante la interfaz [**DEFMPHost.**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) Por ejemplo, para admitir DRM, un origen multimedia crea un objeto denominado autoridad *de confianza de entrada* (ITA). El ITA debe crearse dentro del proceso de PMP. (Para obtener más información sobre las ITA, vea [Ruta de acceso de medios protegidos).](protected-media-path.md) Para usar la [**interfaz DEHOSTPMPHost,**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) haga lo siguiente:

1.  El origen de medios debe implementar la [**interfaz IMFPMPClient.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient)
2.  Durante la resolución de la topología, el proxy de sesión multimedia llama al método [**IMFPMPClient::SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) en el origen multimedia.
3.  El origen del medio llama [**a ALPMPHost::CreateObjectByCLSID para**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) crear el objeto dentro del proceso PMP. El objeto debe tener un CLSID registrado. Además, para cargar dentro del PE, el objeto debe ser de confianza y estar firmado digitalmente. Para obtener información sobre la firma de código de componentes multimedia protegidos, vea las white paper Code Signing for Protected Media Components in Windows Vista (Firma de código para componentes multimedia protegidos [en Windows Vista).](/windows-hardware/test/hlk/)

En la ilustración siguiente se muestra el origen multimedia creado en el proceso de aplicación.

![ilustración de un origen multimedia en el proceso de aplicación.](images/pmp02.png)

Otra alternativa es crear el origen de medios dentro de la sesión PMP.

1.  Establezca el [**atributo MF SESSION REMOTE SOURCE \_ \_ \_ \_ MODE**](mf-session-remote-source-mode-attribute.md) al crear la sesión multimedia. Los atributos de configuración se especifican en el *parámetro pConfiguration* de la [**función MFCreatePMPMediaSession.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)
2.  Llame [**a MFGetService en**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) la sesión multimedia para obtener un puntero a la interfaz [**DESPMPHost.**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) El identificador de servicio **es MF \_ PMP \_ SERVICE.**
3.  Llame [**a MFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) con el identificador de clase **CLSID \_ MFSourceResolver** para crear la resolución de origen dentro del proceso PMP. El método devuelve un puntero a un proxy para la resolución de origen.
4.  Llame [**a IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) o [**ASESOURCESourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) para crear el origen multimedia.
    > [!Note]  
    > En este caso, debe usar las versiones asincrónicas de estos métodos, porque las versiones sincrónicas no son remotables.

     

En la ilustración siguiente se muestra el origen multimedia creado en el proceso PMP.

![ilustración de un origen multimedia en el proceso pmp.](images/pmp03.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)
</dt> <dt>

[Sesión multimedia](media-session.md)
</dt> <dt>

[Ruta de acceso multimedia protegida](protected-media-path.md)
</dt> </dl>

 

 
