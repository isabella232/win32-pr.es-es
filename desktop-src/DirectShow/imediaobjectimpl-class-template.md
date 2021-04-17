---
description: La plantilla de clase IMediaObjectImpl proporciona una implementación base para la interfaz IMediaObject. Para obtener más información sobre el uso de esta plantilla, vea uso de la plantilla de clase DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Plantilla de clase IMediaObjectImpl (Dmoimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680617"
---
# <a name="imediaobjectimpl-class-template"></a>Plantilla de clase IMediaObjectImpl

La `IMediaObjectImpl` plantilla de clase proporciona una implementación base para la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Para obtener más información sobre el uso de esta plantilla, vea [uso de la plantilla de clase DMO](using-the-dmo-class-template.md).

Esta `IMediaObjectImpl` plantilla expone los siguientes miembros.



| Clase anidada                              | Descripción                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | Clase auxiliar que bloquea y desbloquea DMO. |



 



| Método                                                                      | Descripción                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Determina si todas las secuencias no opcionales tienen tipos de medios. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Recupera el tipo de medio actual para un flujo de entrada especificado.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Consulta si el tipo de medio se estableció en un flujo de entrada.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Consulta si un flujo de entrada puede aceptar más entradas.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Consulta si un flujo de entrada puede aceptar un tipo de medio determinado.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Consulta si un flujo de salida puede aceptar un tipo de medio determinado.      |
| [**Lock**](/previous-versions/ms809100(v=msdn.10))                                       | Bloquea DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Recupera el tipo de medio actual para un flujo de salida especificado.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Consulta si el tipo de medio se estableció en un flujo de salida.          |
| [**Pulsa**](/previous-versions/ms809101(v=msdn.10))                                   | Desbloquea DMO                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de DMO](dmo-reference.md)
</dt> <dt>

[Uso de la plantilla de clase DMO](using-the-dmo-class-template.md)
</dt> </dl>

 

 
