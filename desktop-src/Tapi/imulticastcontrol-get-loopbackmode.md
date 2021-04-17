---
description: El \_ método get LoopbackMode obtiene el modo de bucle invertido de multidifusión.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Método IMulticastControl:: get_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690316"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>IMulticastControl:: get \_ LoopbackMode (método)

\[**obtener \_ LoopbackMode** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ LoopbackMode** obtiene el modo de bucle invertido de multidifusión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMode* \[ enuncia\]
</dt> <dd>

Puntero al descriptor del [**\_ \_ modo de bucle invertido de multidifusión**](multicast-loopback-mode.md) del modo de bucle invertido actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Significado                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se realizó correctamente.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *pMode* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




