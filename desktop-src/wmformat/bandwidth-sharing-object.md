---
title: Objeto de uso compartido de ancho de banda
description: Objeto de uso compartido de ancho de banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows SDK de formato multimedia, objetos de uso compartido de ancho de banda
- Formato de sistemas avanzados (ASF), objetos de uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), objetos de uso compartido de ancho de banda
- objects,bandwidth sharing objects
- uso compartido de ancho de banda, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251577"
---
# <a name="bandwidth-sharing-object"></a>Objeto de uso compartido de ancho de banda

Un objeto de uso compartido de ancho de banda se usa para indicar que dos o más secuencias, independientemente de sus velocidades de bits individuales, nunca usarán más de una cantidad especificada de ancho de banda entre ellas. Se trata de un objeto puramente informativo; las velocidades de bits establecidas en él no se aplican mediante programación por ningún objeto de este SDK.

La información de uso compartido de ancho de banda es una parte opcional de un perfil. Los objetos de uso compartido de ancho de banda se pueden crear para la información de uso compartido de ancho de banda existente en un perfil o se pueden crear vacíos, listos para recibir nuevos datos. Los objetos de uso compartido de ancho de banda no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de uso compartido de ancho de banda, debe llamar a [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).

Para crear un objeto de uso compartido de ancho de banda, llame a uno de los métodos siguientes.



| Método                                                                                  | Descripción                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Crea un objeto de uso compartido de ancho de banda sin datos.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Crea un objeto de uso compartido de ancho de banda rellenado con datos de un perfil. Usa el índice de uso compartido de ancho de banda para identificar la información de uso compartido de ancho de banda deseada. |



 

Ambos métodos de la tabla anterior establecen un puntero a una **interfaz IWMBandwidthSharing.** **IWMBandwidthSharing** hereda la interfaz **IWMStreamList,** por lo que no es necesario llamar a **QueryInterface** con este objeto.

Cada objeto de uso compartido de ancho de banda admite las interfaces siguientes.



| Interfaz                                          | Descripción                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Administra las propiedades de un grupo de secuencias que compartirán ancho de banda. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Administra la lista de secuencias que compartirán ancho de banda.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso compartido de ancho de banda**](bandwidth-sharing.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> <dt>

[**Objeto De perfil**](profile-object.md)
</dt> </dl>

 

 




