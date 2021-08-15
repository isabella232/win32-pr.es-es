---
title: Objeto Stream Prioritization
description: Objeto Stream Prioritization
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows SDK de formato multimedia, objetos de priorización de secuencias
- Advanced Systems Format (ASF), objetos de priorización de secuencias
- ASF (formato de sistemas avanzados), objetos de priorización de secuencias
- objects,stream prioritization objects
- objetos de priorización de secuencias
- streams,stream prioritization objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0d8ce386dfa6d3eed64361d77326c515feadb2a6aa05eb697e402d120a55ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699972"
---
# <a name="stream-prioritization-object"></a>Objeto Stream Prioritization

Un objeto de priorización de secuencias se usa para especificar un orden de importancia para las secuencias de un perfil. Cuando la reproducción completa no es posible debido a limitaciones de velocidad de bits, las secuencias de prioridad más baja serán las primeras en descartarse.

Los objetos de priorización de secuencias se pueden crear para los datos de priorización de secuencias existentes en un perfil o se pueden crear vacíos, listos para recibir nuevos datos. Los objetos de priorización de secuencias no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de priorización de secuencias, debe llamar a [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Para crear un objeto de priorización de secuencias, use uno de los métodos siguientes.



| Método                                                                                          | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Crea un objeto de priorización de secuencias sin datos.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Crea un objeto de priorización de secuencia rellenado con datos del perfil. |



 

Ambos métodos de la tabla anterior establecen un puntero a una **interfaz IWMStreamPrioritization.** Esta es la única interfaz admitida por el objeto de priorización de secuencias.



| Interfaz                                                  | Descripción                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Administra la lista de secuencias dentro del objeto de priorización de secuencias. |



 

## <a name="remarks"></a>Observaciones

Solo puede existir una priorización de secuencias para un perfil determinado. Si crea una nueva priorización de secuencia para un perfil que ya contiene una priorización de secuencia, se eliminará la anterior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> <dt>

[**Uso de la priorización de secuencias**](using-stream-prioritization.md)
</dt> </dl>

 

 




