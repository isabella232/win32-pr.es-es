---
description: El \_ método get NumPorts obtiene el número de puertos necesarios para la sesión. La sesión utiliza el número especificado de puertos a partir del valor devuelto por Get \_ StartPort.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'Método ITMedia:: get_NumPorts (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681218"
---
# <a name="itmediaget_numports-method"></a>ITMedia:: get \_ NumPorts (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ NumPorts** obtiene el número de puertos necesarios para la sesión. La sesión utiliza el número especificado de puertos a partir del valor devuelto por [**Get \_ StartPort**](itmedia-get-startport.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumPorts* \[ enuncia\]
</dt> <dd>

Puntero al número de puertos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pNumPorts* no es un puntero válido.<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> </dl>

 

 




