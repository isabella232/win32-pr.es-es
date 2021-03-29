---
description: 'La interfaz IEnumParticipant proporciona métodos de enumeración estándar de COM para la interfaz ITParticipant. El método ITParticipantControl:: EnumerateParticipants devuelve un puntero a IEnumParticipant.'
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interfaz IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680700"
---
# <a name="ienumparticipant-interface"></a>Interfaz IEnumParticipant

\[**IEnumParticipant** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **IEnumParticipant** proporciona métodos de enumeración estándar de com para la interfaz [**ITParticipant**](itparticipant.md) . El método [**ITParticipantControl:: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) devuelve un puntero a **IEnumParticipant**.

La interfaz **IEnumParticipant** se oculta en Visual Basic y en los lenguajes de scripting.

## <a name="members"></a>Miembros

La interfaz **IEnumParticipant** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumParticipant** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumParticipant** tiene estos métodos.



| Método                                  | Descripción                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumparticipant-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumparticipant-next.md)   | Obtiene el siguiente número de elementos especificado en la secuencia de enumeración.<br/>                 |
| [**Reset**](ienumparticipant-reset.md) | Se restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumparticipant-skip.md)   | Omite el siguiente número de elementos especificado en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

