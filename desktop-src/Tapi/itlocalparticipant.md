---
description: La interfaz ITLocalParticipant se expone en el objeto de secuencia cuando IPConf MSP admite la llamada.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interfaz ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690647"
---
# <a name="itlocalparticipant-interface"></a>Interfaz ITLocalParticipant

La interfaz **ITLocalParticipant** se expone en el objeto de secuencia cuando IPConf MSP admite la llamada. El MSP implementa métodos que permiten a una aplicación obtener y establecer la información de los participantes. La interfaz **ITLocalParticipant** se crea llamando a **QueryInterface** en [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).

## <a name="members"></a>Miembros

La interfaz **ITLocalParticipant** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITLocalParticipant** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITLocalParticipant** tiene estos métodos.



| Método                                                                                     | Descripción                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**obtener \_ LocalParticipantTypedInfo**](itlocalparticipant-get-localparticipanttypedinfo.md) | Obtiene la información de los participantes, como el nombre de correo electrónico o la ubicación geográfica.<br/> |
| [**Put \_ LocalParticipantTypedInfo**](itlocalparticipant-put-localparticipanttypedinfo.md) | Establece la información del participante.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

