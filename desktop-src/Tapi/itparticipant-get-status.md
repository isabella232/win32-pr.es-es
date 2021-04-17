---
description: El \_ método get status devuelve una variante \_ bool que indica el estado del participante.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'Método ITParticipant:: get_Status (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680173"
---
# <a name="itparticipantget_status-method"></a>ITParticipant:: get \_ status (método)

\[**obtener \_ El estado** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ status** devuelve una variante \_ bool que indica el estado del participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pITStream* \[ de\]
</dt> <dd>

Puntero a la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*pStatus* \[ enuncia\]
</dt> <dd>

VARIANT \_ true si el participante está habilitado en la secuencia, Variant \_ false si está deshabilitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Método no implementado.<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>           |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pITStream* no es un puntero válido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pITStream* no apunta a una interfaz válida.<br/> |



 

## <a name="remarks"></a>Observaciones

Habilitar o deshabilitar el estado de un participante en un flujo permite a una aplicación silenciar esencialmente a un participante determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**Estado de put \_**](itparticipant-put-status.md)
</dt> </dl>

 

