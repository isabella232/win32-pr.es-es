---
description: El método get recupera el valor de una propiedad de calidad de flujo especificada.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'ITStreamQualityControl:: get (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690474"
---
# <a name="itstreamqualitycontrolget-method"></a>ITStreamQualityControl:: get (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get** recupera el valor de una propiedad de [**calidad de flujo**](streamqualityproperty.md)especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Propiedad* \[ de\]
</dt> <dd>

Miembro de la enumeración [**StreamQualityProperty**](streamqualityproperty.md) .

</dd> <dt>

*plValue* \[ enuncia\]
</dt> <dd>

Valor de la *propiedad* de entrada.

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

[**ITStreamQualityControl**](itstreamqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**StreamQualityProperty**](streamqualityproperty.md)
</dt> </dl>

 

 




