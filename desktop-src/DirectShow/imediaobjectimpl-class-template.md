---
description: La plantilla de clase IMediaObjectImpl proporciona una implementación base para la interfaz IMediaObject. Para obtener más información sobre el uso de esta plantilla, vea Using the DMO Class Template.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Plantilla de clase IMediaObjectImpl (Dmoimpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886812"
---
# <a name="imediaobjectimpl-class-template"></a>Plantilla de clase IMediaObjectImpl

La `IMediaObjectImpl` plantilla de clase proporciona una implementación base para la interfaz [**IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Para obtener más información sobre el uso de esta plantilla, vea [Using the DMO Class Template](using-the-dmo-class-template.md).

Esta `IMediaObjectImpl` plantilla expone los miembros siguientes.



| Nested (Clase)                              | Descripción                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | Clase auxiliar que bloquea y desbloquea el DMO. |



 



| Método                                                                      | Descripción                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Determina si todas las secuencias no opcionales tienen tipos de medios. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Recupera el tipo de medio actual para un flujo de entrada especificado.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Consulta si el tipo de medio se estableció en un flujo de entrada.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Consulta si un flujo de entrada puede aceptar más entradas.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Consulta si un flujo de entrada puede aceptar un tipo de medio determinado.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Consulta si un flujo de salida puede aceptar un tipo de medio determinado.      |
| [**Lock**](/previous-versions/ms809100(v=msdn.10))                                       | Bloquea el DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Recupera el tipo de medio actual para un flujo de salida especificado.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Consulta si el tipo de medio se estableció en un flujo de salida.          |
| [**Desbloquear**](/previous-versions/ms809101(v=msdn.10))                                   | Desbloquea el DMO                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dmoimpl.h</dt> </dl>                                                                     |
| Biblioteca<br/> | <dl> <dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DMO Referencia](dmo-reference.md)
</dt> <dt>

[Uso de la plantilla DMO clase](using-the-dmo-class-template.md)
</dt> </dl>

 

 
