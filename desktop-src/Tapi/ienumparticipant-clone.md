---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual. Este método está oculto de Visual Basic y lenguajes de scripting.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: Método IEnumParticipant::Clone (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccd4bd29442daa01e632ae83510a87eebb06cb72beafc206b04d47c3dd761db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140498"
---
# <a name="ienumparticipantclone-method"></a>IEnumParticipant::Clone (Método)

\[**Clone** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual. Este método está oculto de Visual Basic y lenguajes de scripting.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Puntero a la [**nueva interfaz IEnumParticipant.**](ienumparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppEnum* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Error por motivos desconocidos.<br/>                          |



 

## <a name="remarks"></a>Comentarios

TAPI llama al [**método AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la [**interfaz IEnumParticipant devuelta**](ienumparticipant.md) por **IEnumParticipant::Clone**. La aplicación debe llamar [**a Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la **interfaz IEnumParticipant** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

