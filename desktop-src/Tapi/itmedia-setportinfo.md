---
description: El método SetPortInfo establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para una sesión.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'ITMedia:: SetPortInfo (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690980"
---
# <a name="itmediasetportinfo-method"></a>ITMedia:: SetPortInfo (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SetPortInfo** establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para una sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartPort* \[ de\]
</dt> <dd>

Puerto de inicio. Puede ser un valor comprendido en el intervalo de 0-65535.

</dd> <dt>

*NumPorts* \[ de\]
</dt> <dd>

Número de puertos. Puede ser un valor comprendido en el intervalo de 0-65535.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *StartPort o NumPorts* no es válido.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.

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

 

 




