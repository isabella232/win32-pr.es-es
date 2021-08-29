---
description: La interfaz IEnumParticipant proporciona métodos de enumeración com estándar para la interfaz ITParticipant. El método ITParticipantControl::EnumerateParticipants devuelve un puntero a IEnumParticipant.
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interfaz IEnumParticipant (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ba6deb232b03a7923c8ea47e9e200f3d3ea9beb5bddcd0572e3cac4c2b6269
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003583"
---
# <a name="ienumparticipant-interface"></a>Interfaz IEnumParticipant

\[**IEnumParticipant** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz IEnumParticipant proporciona métodos** de enumeración com estándar para la [**interfaz ITParticipant.**](itparticipant.md) El [**método ITParticipantControl::EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) devuelve un puntero a **IEnumParticipant**.

La **interfaz IEnumParticipant** está oculta de Visual Basic y lenguajes de scripting.

## <a name="members"></a>Miembros

La **interfaz IEnumParticipant** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumParticipant** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumParticipant** tiene estos métodos.



| Método                                  | Descripción                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clon**](ienumparticipant-clone.md) | Crea otro enumerador que contiene el mismo estado de enumeración que el actual.<br/> |
| [**Next**](ienumparticipant-next.md)   | Obtiene el siguiente número especificado de elementos de la secuencia de enumeración.<br/>                 |
| [**Restablecer**](ienumparticipant-reset.md) | Restablece al principio de la secuencia de enumeración.<br/>                                    |
| [**Omitir**](ienumparticipant-skip.md)   | Omite el siguiente número especificado de elementos en la secuencia de enumeración.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

