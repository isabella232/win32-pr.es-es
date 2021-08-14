---
title: Trabajar con listas de revocación
description: Trabajar con listas de revocación
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows SDK de formato multimedia, listas de revocación
- Formato de sistemas avanzados (ASF), listas de revocación
- ASF (formato de sistemas avanzados), listas de revocación
- listas de revocación
- administración de derechos digitales (DRM), listas de revocación
- DRM (administración de derechos digitales), listas de revocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d022b9b55a1a14b147d76d289efeac956bae8f1858d155f138efa579d533fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194890"
---
# <a name="working-with-revocation-lists"></a>Trabajar con listas de revocación

Para responder a las infracciones de seguridad y asegurarse de que las aplicaciones de reproductor que se sabe que están rotas o en peligro no pueden reproducir o usar archivos protegidos, cada licencia que se emite contiene una lista de revocación. Una lista de revocación contiene los certificados de aplicación de todas las aplicaciones de reproductor que se sabe que están rotas o dañadas. Cuando se recibe una nueva licencia, el componente DRM de la aplicación de reproductor comprueba si hay una lista de revocación. Si se encuentra una que es más reciente que la que se encuentra actualmente en el equipo, se almacena la lista más reciente. La próxima vez que el consumidor reproduce un archivo ASF protegido, el componente DRM compara la aplicación del reproductor con la lista de revocación. Si se revoca la aplicación del reproductor, el componente DRM envía un mensaje de error a la aplicación.

Las aplicaciones de reproductor pueden recibir un mensaje de error de revocación en los escenarios siguientes:

-   El mensaje de error se recibe después de que la aplicación llame al [**método IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) para un archivo protegido. Se produce un error en la llamada con el código **HRESULT** NS \_ E DRM APPCERT REVOKED, que se proporciona a la función de devolución de llamada OnStatus con el estado \_ \_ \_  \_ WMT ACQUIRE \_ LICENSE. Si se omite este código **HRESULT,** se seguirán producir errores.
-   El mensaje de error se recibe cuando la aplicación crea el lector habilitado para DRM y llama al método [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) para un archivo protegido. Se produce un error en la llamada con el código **HRESULT** NS E DRM APPCERT REVOKED, que se proporciona al método de devolución de llamada \_ \_ \_ \_ [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) con el estado WMT \_ OPENED. Cuando una aplicación de reproductor recibe este mensaje de error, la aplicación debe notificar a los usuarios finales y proporcionar una manera de restaurar la funcionalidad a su reproductor. Por ejemplo, la aplicación puede abrir una dirección URL donde los usuarios finales pueden descargar una actualización de la aplicación en peligro.

**Nota** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Control de eventos de adquisición de licencias**](handling-license-acquisition-events.md)
</dt> </dl>

 

 




