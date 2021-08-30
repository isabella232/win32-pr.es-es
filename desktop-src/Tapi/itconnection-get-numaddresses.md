---
description: El método \_ get NumAddresses obtiene el número de direcciones que se usarán para la sesión.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: Método ITConnection::get_NumAddresses (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13a2bae08e4d989b0ce9a64b651e777d3c9b1cb0744f63798f06bf182aede58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991895"
---
# <a name="itconnectionget_numaddresses-method"></a>ItConnection::get \_ NumAddresses (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método \_ get NumAddresses** obtiene el número de direcciones que se usarán para la sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Número de direcciones de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pNumAddresse* s no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




