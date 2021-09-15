---
title: Objeto de configuración del flujo
description: Objeto de configuración del flujo
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows SDK de formato multimedia, objetos de configuración de secuencias
- Formato de sistemas avanzados (ASF), objetos de configuración de flujo
- ASF (formato de sistemas avanzados), objetos de configuración de flujo
- objects,stream configuration objects
- objetos de configuración de flujo
- streams,stream configuration objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574312"
---
# <a name="stream-configuration-object"></a>Objeto de configuración del flujo

Un objeto de configuración de flujo se usa para especificar las propiedades de una secuencia multimedia en un archivo ASF. Los objetos de configuración de flujo se pueden crear para secuencias existentes en un perfil o se pueden crear vacíos, listos para recibir nuevos datos. Los objetos de configuración de flujo no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de configuración de flujo, debe llamar a [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para agregar una nueva secuencia o [**AWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para guardar los cambios realizados en una secuencia existente.

Para crear un objeto de configuración de flujo, use uno de los métodos siguientes.



| Método                                                                | Descripción                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Crea un objeto de configuración de flujo sin datos.                                                                          |
| [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Crea un objeto de configuración de flujo rellenado con datos de un perfil. Usa el índice de secuencia para identificar la secuencia deseada.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Crea un objeto de configuración de flujo rellenado con datos de un perfil. Usa el número de secuencia para identificar la secuencia deseada. |



 

Todos los métodos de la tabla anterior establecen un puntero a una **interfaz IWMStreamConfig.** Las demás interfaces del objeto de configuración de flujo se pueden obtener llamando al **método QueryInterface.**

El objeto de configuración de flujo admite las interfaces siguientes.



| Interfaz                                        | Descripción                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Establece y recupera la estructura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Establece y recupera propiedades que no son necesarias para todas las secuencias, como la configuración de velocidad de bits variable (VBR).                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Establece y recupera toda la información básica sobre una secuencia.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Configura los tipos de extensiones de unidad de datos asociadas a la secuencia. Hereda todos los métodos de **IWMStreamConfig.** |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Establece y recupera el idioma de la secuencia. Hereda todos los métodos de **IWMStreamConfig** **e IWMStreamConfig2.** |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Administra las propiedades de una secuencia de vídeo. Se trata de una interfaz opcional y solo está disponible para secuencias de vídeo.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> </dl>

 

 




