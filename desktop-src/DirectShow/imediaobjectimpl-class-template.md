---
description: La plantilla de clase IMediaObjectImpl proporciona una implementación base para la interfaz IMediaObject. Para obtener más información sobre el uso de esta plantilla, vea Using the DMO Class Template.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Plantilla de clase IMediaObjectImpl (Dmoimpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b166836ff4da6100f61fca5d3a0c2887462b37adcbdd2ec61abeb919553a59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015583"
---
# <a name="imediaobjectimpl-class-template"></a>Plantilla de clase IMediaObjectImpl

La `IMediaObjectImpl` plantilla de clase proporciona una implementación base para la interfaz [**IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Para obtener más información sobre el uso de esta plantilla, vea [Using the DMO Class Template](using-the-dmo-class-template.md).

Esta `IMediaObjectImpl` plantilla expone los miembros siguientes.



| Clase anidada                              | Descripción                                  |
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[DMO Referencia](dmo-reference.md)
</dt> <dt>

[Uso de la DMO de clase](using-the-dmo-class-template.md)
</dt> </dl>

 

 
