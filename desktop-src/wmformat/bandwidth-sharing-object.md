---
title: Objeto de uso compartido de ancho de banda
description: Objeto de uso compartido de ancho de banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- SDK de formato de Windows Media, objetos de uso compartido de ancho de banda
- Advanced Systems Format (ASF), ancho de banda Sharing Objects
- ASF (formato de sistemas avanzados), objetos de uso compartido de ancho de banda
- objetos, uso compartido de ancho de banda
- uso compartido de ancho de banda, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420289"
---
# <a name="bandwidth-sharing-object"></a>Objeto de uso compartido de ancho de banda

Un objeto de uso compartido de ancho de banda se usa para indicar que dos o más secuencias, independientemente de sus velocidades de bits individuales, nunca usarán más de una cantidad de ancho de banda especificada entre ellas. Se trata de un objeto meramente informativo; los objetos de este SDK no aplican mediante programación las velocidades de bits establecidas dentro de ella.

La información de uso compartido de ancho de banda es una parte opcional de un perfil. Se pueden crear objetos de uso compartido de ancho de banda para la información de uso compartido de ancho de banda existente en un perfil o se pueden crear vacíos, listos para recibir datos nuevos. Los objetos de uso compartido de ancho de banda no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de uso compartido de ancho de banda, debe llamar a [**IWMProfile3:: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).

Para crear un objeto de uso compartido de ancho de banda, llame a uno de los métodos siguientes.



| Método                                                                                  | Descripción                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Crea un objeto de uso compartido de ancho de banda sin datos.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Crea un objeto de uso compartido de ancho de banda rellenado con datos de un perfil. Usa el índice de uso compartido de ancho de banda para identificar la información de uso compartido de ancho de banda deseada. |



 

Ambos métodos de la tabla anterior establecen un puntero a una interfaz **IWMBandwidthSharing** . **IWMBandwidthSharing** hereda la interfaz **IWMStreamList** , por lo que no es necesario llamar a **QueryInterface** con este objeto.

Cada objeto de uso compartido de ancho de banda admite las siguientes interfaces.



| Interfaz                                          | Descripción                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Administra las propiedades de un grupo de secuencias que compartirán el ancho de banda. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Administra la lista de secuencias que compartirán el ancho de banda.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso compartido de ancho de banda**](bandwidth-sharing.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> </dl>

 

 




