---
description: Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2:: EnumDeviceCapabilities (método) (WIA. h)'
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
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541982"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>IWiaItem2:: EnumDeviceCapabilities (método)

Crea un enumerador que se usa para determinar los comandos y eventos que admite un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica una marca que selecciona el tipo de funcionalidad que se va a enumerar. Es uno de los valores siguientes.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_comandos de dispositivo WIA \_**


</dt> <dd>

Enumerar comandos de dispositivo.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_eventos de dispositivo WIA \_**


</dt> <dd>

Enumerar eventos de dispositivo.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ DISP \_* . de desarrollo \[\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Recibe un puntero a la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) creada por este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método se usa para crear un objeto de enumerador para obtener el conjunto de comandos y eventos que admite un dispositivo WIA 2,0. El parámetro *lFlags* se usa para especificar los tipos de funcionalidades de dispositivo que se van a enumerar. El método **IWiaItem2:: EnumDeviceCapabilities** almacena la dirección de la interfaz del objeto enumerador en el parámetro *ppIEnumWIA \_ dev \_ caps* .

Solo se puede llamar a este método en el elemento raíz de los objetos [**IWiaItem2**](-wia-iwiaitem2.md) de un árbol de dispositivos.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnumWIA \_ dev \_ caps* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
