---
description: La interfaz ITLocalParticipant se expone en el objeto de secuencia cuando el MSP de IPConf admite la llamada.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interfaz ITLocalParticipant (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56448bae9b1f2e93afa901401bc48f46a93a0435c2f67dbea96b2cb7b72399d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060963"
---
# <a name="itlocalparticipant-interface"></a>Interfaz ITLocalParticipant

La **interfaz ITLocalParticipant** se expone en el objeto de secuencia cuando el MSP de IPConf admite la llamada. El MSP implementa métodos que permiten a una aplicación obtener y establecer la información del participante. La **interfaz ITLocalParticipant** se crea mediante una llamada **a QueryInterface** en [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

## <a name="members"></a>Miembros

La **interfaz ITLocalParticipant** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITLocalParticipant** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITLocalParticipant** tiene estos métodos.



| Método                                                                                     | Descripción                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**get \_ LocalParticipantTypedInfo**](itlocalparticipant-get-localparticipanttypedinfo.md) | Obtiene información del participante, como el nombre del correo electrónico o la ubicación geográfica.<br/> |
| [**put \_ LocalParticipantTypedInfo**](itlocalparticipant-put-localparticipanttypedinfo.md) | Establece la información del participante.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

