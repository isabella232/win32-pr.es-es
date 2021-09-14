---
description: El método SetPortInfo establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para una sesión.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: Método ITMedia::SetPortInfo (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160663"
---
# <a name="itmediasetportinfo-method"></a>ItMedia::SetPortInfo (método)

\[Los controles e interfaces de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SetPortInfo** establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para una sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartPort* \[ En\]
</dt> <dd>

Puerto de inicio. Puede ser un valor en el intervalo 0-65535.

</dd> <dt>

*NumPorts* \[ En\]
</dt> <dd>

Número de puertos. Puede ser un valor en el intervalo 0-65535.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro StartPort o NumPorts* no es válido.<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Esta función puede enviar datos a través de la conexión en formato sin cifrar; por lo tanto, es posible que alguien que intercepta en la red pueda leer los datos. Antes de usar este método, se debe tener en cuenta el riesgo de seguridad de enviar los datos en texto no especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> </dl>

 

 




