---
description: El método get \_ LoopbackMode obtiene el modo de bucle recuperación de multidifusión.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: Método IMulticastControl::get_LoopbackMode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a3f9a600ea64bacf7cafdc5071df264d79079adfefd4a771eea9569fcbb092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013025"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a>IMulticastControl::get \_ LoopbackMode (método)

\[**get \_ LoopbackMode** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ LoopbackMode** obtiene el modo de bucle recuperación de multidifusión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMode* \[ out\]
</dt> <dd>

Puntero al descriptor [**MULTICAST \_ LOOPBACK \_ MODE**](multicast-loopback-mode.md) del modo de bucle recuperación actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Significado                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se realizó correctamente.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro pMode* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




