---
title: Objeto de exclusión mutua
description: Objeto de exclusión mutua
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows SDK de formato multimedia, objetos de exclusión mutua
- Formato de sistemas avanzados (ASF), objetos de exclusión mutua
- ASF (formato de sistemas avanzados), objetos de exclusión mutua
- objects,mutual exclusion objects
- exclusión mutua, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360212"
---
# <a name="mutual-exclusion-object"></a>Objeto de exclusión mutua

Un objeto de exclusión mutua se usa para especificar una serie de flujos, de los cuales solo se puede entregar uno a la vez. Esto se puede usar de varias maneras, como proporcionar una secuencia de audio en varios idiomas como el autor de una secuencia de vídeo.

La exclusión mutua es una parte opcional de un perfil. Los objetos de exclusión mutua se pueden crear para la información de exclusión mutua existente en un perfil o se pueden crear vacíos, listos para recibir nuevos datos. Los objetos de exclusión mutua no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de exclusión mutua, debe llamar a [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

Para crear un objeto de exclusión mutua, use uno de los métodos siguientes.



| Método                                                                              | Descripción                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crea un objeto de exclusión mutua sin ningún dato.                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Crea un objeto de exclusión mutua rellenado con datos de un perfil. Usa el índice de exclusión mutua para identificar la información de exclusión mutua deseada. |



 

Ambos métodos de la tabla anterior establecen un puntero a una **interfaz IWMMutualExclusion.** **IWMMutualExclusion** hereda la interfaz IWMStreamList y nunca es necesario acceder directamente a la interfaz **IWMStreamList.** La otra interfaz del objeto de exclusión mutua se puede obtener llamando al **método QueryInterface.**

Cada objeto de exclusión mutua admite las interfaces siguientes.



| Interfaz                                          | Descripción                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Establece y recupera el tipo de exclusión mutua que se va a usar.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organiza los flujos en registros, que se pueden usar para crear escenarios complejos de exclusión mutua. Hereda todos los métodos de **IWMMutualExclusion.** |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Administra la lista de secuencias mutuamente excluyentes.                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Exclusión mutua**](mutual-exclusion.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> </dl>

 

 




