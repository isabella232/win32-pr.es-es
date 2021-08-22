---
description: El método Get recupera el valor de una propiedad de configuración de audio determinada.
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: ItAudioSettings::Get (método) (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34cdf6fdf0e243f5d50ac758d8110c64cdd8287809512ebe59489635416d58e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865588"
---
# <a name="itaudiosettingsget-method"></a>ITAudioSettings::Get (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Get** recupera el valor de una propiedad de configuración de audio [**determinada.**](audiosettingsproperty.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ En\]
</dt> <dd>

Miembro de la [**enumeración AudioSettingsProperty.**](audiosettingsproperty.md)

</dd> <dt>

*plValue* \[ out\]
</dt> <dd>

Valor de la propiedad *de entrada*.

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Valor de la [**enumeración TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el *valor* property.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioSettings**](itaudiosettings.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioSettingsProperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




