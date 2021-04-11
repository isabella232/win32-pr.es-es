---
title: Objeto de configuración del flujo
description: Objeto de configuración del flujo
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- SDK de Windows Media Format, objetos de configuración de secuencia
- Advanced Systems Format (ASF), stream Configuration Objects
- ASF (formato de sistemas avanzados), objetos de configuración de secuencia
- objetos, objetos de configuración de secuencias
- objetos de configuración de secuencia
- flujos, objetos de configuración de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149127"
---
# <a name="stream-configuration-object"></a>Objeto de configuración del flujo

Un objeto de configuración de secuencia se utiliza para especificar las propiedades de una secuencia de medios en un archivo ASF. Los objetos de configuración de secuencia se pueden crear para los flujos existentes en un perfil o se pueden crear vacíos, listos para recibir datos nuevos. Los objetos de configuración de secuencia no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de configuración de secuencia, debe llamar a [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para agregar una nueva secuencia o [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para guardar los cambios realizados en una secuencia existente.

Para crear un objeto de configuración de secuencia, use uno de los métodos siguientes.



| Método                                                                | Descripción                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Crea un objeto de configuración de secuencia sin datos.                                                                          |
| [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Crea un objeto de configuración de secuencia que se rellena con datos de un perfil. Usa el índice de la secuencia para identificar el flujo deseado.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Crea un objeto de configuración de secuencia que se rellena con datos de un perfil. Utiliza el número de secuencia para identificar el flujo deseado. |



 

Todos los métodos de la tabla anterior establecen un puntero a una interfaz **IWMStreamConfig** . Las demás interfaces del objeto de configuración de la secuencia se pueden obtener llamando al método **QueryInterface** .

El objeto de configuración de la secuencia admite las siguientes interfaces.



| Interfaz                                        | Descripción                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Establece y recupera la estructura [**de \_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Establece y recupera propiedades que no son necesarias para todas las secuencias, como la configuración de velocidad de bits variable (VBR).                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Establece y recupera toda la información básica sobre una secuencia.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Configura los tipos de extensiones de unidad de datos asociados a la secuencia. Hereda todos los métodos de **IWMStreamConfig**. |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Establece y recupera el idioma de la secuencia. Hereda todos los métodos de **IWMStreamConfig** y **IWMStreamConfig2**. |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Administra las propiedades de una secuencia de vídeo. Se trata de una interfaz opcional y solo está disponible para las secuencias de vídeo.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> </dl>

 

 




