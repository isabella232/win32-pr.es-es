---
description: Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo Windows Image Acquisition (WIA) 2.0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: Método IWiaItem2::EnumDeviceCapabilities (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6748966beaa3bf16f668c4b8b0de60a4302ebcf514f06a3d588999d5faebaf3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450465"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>IWiaItem2::EnumDeviceCapabilities (método)

Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo Windows Image Acquisition (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica una marca que selecciona el tipo de funcionalidades que se enumerará. Es uno de los siguientes valores.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**COMANDOS DE \_ DISPOSITIVO \_ WIA**


</dt> <dd>

Enumerar comandos de dispositivo.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**EVENTOS DE \_ DISPOSITIVO \_ WIA**


</dt> <dd>

Enumerar eventos de dispositivo.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ DEV \_ CAPS* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Recibe un puntero a la [**interfaz \_ \_ CAPS de IEnumWIA DEV**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) creada por este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método se usa para crear un objeto enumerador para obtener el conjunto de comandos y eventos que admite un dispositivo WIA 2.0. El *parámetro lFlags* se usa para especificar qué tipos de funcionalidades de dispositivo se deben enumerar. El **método IWiaItem2::EnumDeviceCapabilities** almacena la dirección de la interfaz del objeto enumerador en el parámetro *PPIEnumWIA \_ DEV \_ CAPS.*

Solo se puede llamar a este método en el elemento raíz de [**objetos IWiaItem2**](-wia-iwiaitem2.md) de un árbol de dispositivos.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnumWIA \_ DEV \_ CAPS.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
