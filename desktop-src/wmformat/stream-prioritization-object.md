---
title: Objeto de priorización de flujo
description: Objeto de priorización de flujo
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- SDK de Windows Media Format, objetos de priorización de secuencias
- Advanced Systems Format (ASF), objetos de priorización de secuencias
- ASF (formato de sistemas avanzados), objetos de priorización de secuencias
- objetos, objetos de priorización de secuencias
- objetos de priorización de flujo
- flujos, objetos de priorización de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105720128"
---
# <a name="stream-prioritization-object"></a>Objeto de priorización de flujo

Un objeto de priorización de flujo se utiliza para especificar un orden de importancia para las secuencias de un perfil. Cuando no es posible la reproducción completa debido a las limitaciones de velocidad de bits, las secuencias de prioridad más baja serán las primeras que se van a quitar.

Los objetos de priorización de flujo se pueden crear para los datos de priorización de flujo existentes en un perfil o se pueden crear vacíos, listos para recibir datos nuevos. Los objetos de priorización de flujo no pueden existir independientemente de un objeto de perfil. Para guardar el contenido de un objeto de priorización de flujo, debe llamar a [**IWMProfile3:: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Para crear un objeto de priorización de secuencia, use uno de los métodos siguientes.



| Método                                                                                          | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Crea un objeto de priorización de flujo sin datos.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Crea un objeto de priorización de flujo rellenado con datos del perfil. |



 

Ambos métodos de la tabla anterior establecen un puntero a una interfaz **IWMStreamPrioritization** . Esta es la única interfaz que admite el objeto de priorización de flujo.



| Interfaz                                                  | Descripción                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Administra la lista de secuencias en el objeto de priorización de flujo. |



 

## <a name="remarks"></a>Observaciones

Solo puede existir una priorización de flujo para un perfil determinado. Si crea una nueva priorización de flujo para un perfil que ya contiene una priorización de flujo, se eliminará la antigua.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> <dt>

[**Usar la priorización de flujos**](using-stream-prioritization.md)
</dt> </dl>

 

 




