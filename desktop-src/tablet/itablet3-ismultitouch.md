---
description: Determina si un dispositivo de entrada admite multitouch.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: ITablet3::IsMultiTouch (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579468"
---
# <a name="itablet3ismultitouch-method"></a>ITablet3::IsMultiTouch (método)

Determina si un dispositivo de entrada admite multitouch.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsMultiTouch* \[ out\]
</dt> <dd>

Indica si el dispositivo es multitouch.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S OK si \_ se** ejecuta correctamente; de lo contrario, devuelve un código de error como **E \_ FAIL.**

## <a name="remarks"></a>Observaciones

Después de determinar a través de [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) o **ITablet3::IsMultiTouch** que multitouch está disponible, una aplicación puede optar por participar en los mensajes de entrada multitouch. Encontrará información adicional sobre el filtrado de métodos multitouch en la sección de la propiedad **IRealTimeStylus3::MultiTouchEnabled.**

## <a name="examples"></a>Ejemplos


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




