---
description: El método GetRange obtiene el intervalo de valores válidos para una propiedad de calidad de llamada determinada.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'ITCallQualityControl:: GetRange (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690404"
---
# <a name="itcallqualitycontrolgetrange-method"></a>ITCallQualityControl:: GetRange (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **GetRange** obtiene el intervalo de valores válidos para una [propiedad de calidad de llamada](callqualityproperty.md)determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ de\]
</dt> <dd>

Miembro de la enumeración [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*plMin* \[ enuncia\]
</dt> <dd>

Valor mínimo válido para la propiedad de entrada.

</dd> <dt>

*plMax* \[ enuncia\]
</dt> <dd>

Valor máximo válido para la propiedad de entrada.

</dd> <dt>

*plSteppingDelta* \[ enuncia\]
</dt> <dd>

Incremento por el que se puede aumentar o disminuir el valor de la propiedad.

</dd> <dt>

*plDefault* \[ enuncia\]
</dt> <dd>

Valor predeterminado del parámetro *Property* .

</dd> <dt>

*plFlags* \[ enuncia\]
</dt> <dd>

Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .

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

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




