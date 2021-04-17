---
title: Trabajar con listas de revocación
description: Trabajar con listas de revocación
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- SDK de Windows Media Format, listas de revocación
- Advanced Systems Format (ASF), listas de revocación
- ASF (formato de sistemas avanzados), listas de revocación
- listas de revocación
- Administración de derechos digitales (DRM), listas de revocación
- DRM (administración de derechos digitales), listas de revocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532962"
---
# <a name="working-with-revocation-lists"></a>Trabajar con listas de revocación

Para responder a las infracciones de seguridad y asegurarse de que las aplicaciones del reproductor que se sabe que están interrumpidas o en peligro no pueden reproducir o usar archivos protegidos, cada licencia que se emite contiene una lista de revocación. Una lista de revocación contiene los certificados de aplicación de todas las aplicaciones de reproductor que se sabe que están dañados o están dañados. Cuando se recibe una nueva licencia, el componente DRM de la aplicación del reproductor comprueba si hay una lista de revocación. Si se encuentra una que es más reciente que la que hay actualmente en el equipo, se almacena la lista más reciente. La próxima vez que el consumidor reproduzca un archivo ASF protegido, el componente DRM comparará la aplicación de reproducción con la lista de revocación. Si se revoca la aplicación de reproducción, el componente DRM envía un mensaje de error a la aplicación.

Las aplicaciones de reproductor pueden recibir un mensaje de error de revocación en los escenarios siguientes:

-   El mensaje de error se recibe una vez que la aplicación llama al método [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) para un archivo protegido. Se produce un error en la llamada con el código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocado, que se proporciona a la función de devolución de llamada de **Estado** con el estado de la licencia de adquisición de WMT \_ \_ . Si se omite este código **HRESULT** , se seguirán produciendo errores.
-   El mensaje de error se recibe cuando la aplicación crea el lector habilitado para DRM y llama al método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) para un archivo protegido. Se produce un error en la llamada con el código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revocado, que se proporciona al método de devolución de llamada [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) con \_ estado abierto de WMT. Cuando una aplicación de reproducción recibe este mensaje de error, la aplicación debe notificar a los usuarios finales y proporcionar una manera de restaurar la funcionalidad de su reproductor. Por ejemplo, la aplicación puede abrir una dirección URL en la que los usuarios finales pueden descargar una actualización de la aplicación en peligro.

**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Control de eventos de adquisición de licencias**](handling-license-acquisition-events.md)
</dt> </dl>

 

 




