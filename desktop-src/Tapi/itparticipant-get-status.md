---
description: El método get \_ Status devuelve un VARIANT \_ BOOL que indica el estado del participante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: Método ITParticipant::get_Status (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160643"
---
# <a name="itparticipantget_status-method"></a>ItParticipant::get \_ (método)

\[**get \_ El** estado no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Status** devuelve un VARIANT \_ BOOL que indica el estado del participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pITStream* \[ En\]
</dt> <dd>

Puntero a [**la interfaz ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> <dt>

*pStatus* \[ out\]
</dt> <dd>

VARIANT \_ TRUE si el participante está habilitado en la secuencia, VARIANT FALSE si está \_ deshabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Método no implementado.<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>           |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pITStream* no es un puntero válido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pITStream* no apunta a una interfaz válida.<br/> |



 

## <a name="remarks"></a>Observaciones

Habilitar o deshabilitar el estado de un participante en una secuencia permite a una aplicación silenciar esencialmente un participante determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**put \_ Status**](itparticipant-put-status.md)
</dt> </dl>

 

