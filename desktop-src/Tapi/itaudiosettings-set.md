---
description: El método Set establece el valor de una propiedad de configuración de audio determinada.
ms.assetid: 3132e004-5543-4b21-878d-35197f7077d6
title: 'ITAudioSettings:: set (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf947c28d3b5270b3c5dabd4196d0e6b71f57911
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680911"
---
# <a name="itaudiosettingsset-method"></a>ITAudioSettings:: set (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **set** establece el valor de una [**propiedad de configuración de audio**](audiosettingsproperty.md)determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ de\]
</dt> <dd>

Miembro de la enumeración [**AudioSettingsProperty**](audiosettingsproperty.md) .

</dd> <dt>

valor *l* \[ de\]
</dt> <dd>

Valor deseado para la propiedad.

</dd> <dt>

*lFlags* \[ de\]
</dt> <dd>

Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controlará el valor de la *propiedad* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAudioSettings**](itaudiosettings.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioSettingsProperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




