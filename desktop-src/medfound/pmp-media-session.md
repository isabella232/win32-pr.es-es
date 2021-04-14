---
description: .
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: Sesión de medios de PMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e14d9e403620d273bb4aeb3347cba523f304b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361834"
---
# <a name="pmp-media-session"></a>Sesión de medios de PMP

Una aplicación puede crear la [sesión multimedia](media-session.md) en un proceso independiente denominado el proceso de la [ruta de acceso a medios protegidos](protected-media-path.md) (PMP). El propósito principal del proceso de PMP es habilitar la reproducción de contenido protegido con administración de derechos digitales (DRM). De forma predeterminada, el proceso de PMP se crea dentro de un entorno protegido (PE). Solo los componentes firmados de confianza se pueden cargar dentro de un PE. Una ventaja secundaria del proceso de PMP es que aísla el proceso de aplicación de la canalización multimedia. Para obtener más información sobre el proceso de PMP, vea [ruta de acceso a medios protegidos](protected-media-path.md).

Para crear la sesión multimedia dentro del proceso de PMP, llame a la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) . Opcionalmente, puede pasar la marca de **\_ \_ proceso sin protección de MFPMPSESSION** . Si se establece esta marca, el proceso de PMP se crea dentro de un proceso sin protección y no en un proceso de PE. El proceso sin protección no se puede usar para la reproducción de DRM, pero ofrece las ventajas del aislamiento de procesos.

La función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) devuelve un puntero a un objeto proxy para la sesión multimedia. La aplicación se comunica con la sesión multimedia a través del proxy.

![Ilustración de la sesión multimedia dentro del proceso de PMP](images/pmp01.png)

De forma predeterminada, cuando la aplicación crea una topología, el origen de medios se crea dentro del proceso de la aplicación. En el proceso de PMP se crea un proxy para el origen de medios. El origen de medios puede crear objetos dentro del proceso de PMP mediante la interfaz [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) . Por ejemplo, para admitir DRM, un origen multimedia crea un objeto denominado *autoridad de confianza de entrada* (ITA). La ITA debe crearse dentro del proceso de PMP. (Para obtener más información sobre ITAs, vea [ruta de acceso de medios protegidos](protected-media-path.md)). Para usar la interfaz [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , haga lo siguiente:

1.  El origen del medio debe implementar la interfaz [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) .
2.  Durante la resolución de la topología, el proxy de la sesión multimedia llama al método [**IMFPMPClient:: SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) en el origen del medio.
3.  El origen multimedia llama a [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) para crear el objeto dentro del proceso de PMP. El objeto debe tener un CLSID registrado. Además, para cargar dentro del PE, el objeto debe ser de confianza y estar firmado digitalmente. Para obtener información acerca de los componentes multimedia protegidos de la firma de código, consulte las notas del producto [firma de código para componentes multimedia protegidos en Windows Vista](/windows-hardware/test/hlk/) .

En la ilustración siguiente se muestra el origen de medios creado en el proceso de la aplicación.

![Ilustración de un origen multimedia en el proceso de la aplicación.](images/pmp02.png)

Otra alternativa es crear el origen de medios dentro de la sesión de PMP.

1.  Establezca el atributo de [**\_ \_ \_ \_ modo de origen remoto de la sesión MF**](mf-session-remote-source-mode-attribute.md) cuando cree la sesión multimedia. Los atributos de configuración se especifican en el parámetro *pConfiguration* de la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .
2.  Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) en la sesión de medios para obtener un puntero a la interfaz [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) . El identificador del servicio es **MF \_ PMP \_ Service**.
3.  Llame a [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) con el identificador de clase **CLSID \_ MFSourceResolver** para crear la resolución de origen dentro del proceso de PMP. El método devuelve un puntero a un proxy para la resolución de origen.
4.  Llame a [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) o [**IMFSourceResolver:: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) para crear el origen de medios.
    > [!Note]  
    > En este caso, debe utilizar las versiones asincrónicas de estos métodos, ya que las versiones sincrónicas no son remotas.

     

En la ilustración siguiente se muestra el origen de medios creado en el proceso de PMP.

![Ilustración de un origen multimedia en el proceso de PMP.](images/pmp03.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)
</dt> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Ruta de acceso a medios protegidos](protected-media-path.md)
</dt> </dl>

 

 
