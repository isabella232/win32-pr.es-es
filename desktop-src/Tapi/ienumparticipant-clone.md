---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual. Este método está oculto en Visual Basic y en los lenguajes de scripting.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'IEnumParticipant:: Clone (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681141"
---
# <a name="ienumparticipantclone-method"></a>IEnumParticipant:: Clone (método)

\[**Clone** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual. Este método está oculto en Visual Basic y en los lenguajes de scripting.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ enuncia\]
</dt> <dd>

Puntero a la nueva interfaz [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppEnum* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Error por razones desconocidas.<br/>                          |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la interfaz [**IEnumParticipant**](ienumparticipant.md) devuelta por **IEnumParticipant:: Clone**. La aplicación debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la interfaz **IEnumParticipant** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

