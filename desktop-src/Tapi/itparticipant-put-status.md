---
description: El \_ método put status establece el estado de un participante.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: 'ITParticipant: método de ut_Status de:p (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690388"
---
# <a name="itparticipantput_status-method"></a>ITParticipant::p \_ método de estado UT

\[**colocar \_ El estado** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Put \_ status** establece el estado de un participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pITStream* \[ de\]
</dt> <dd>

Puntero a la interfaz [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*fEnable* \[ de\]
</dt> <dd>

VARIANT \_ true si el participante está habilitado en la secuencia, Variant \_ false si se va a deshabilitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Método no implementado.<br/>                                        |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pITStream* no es un puntero válido.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pITStream* no apunta a una interfaz válida.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>           |



 

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

[**obtener \_ Estado**](itparticipant-get-status.md)
</dt> </dl>

 

