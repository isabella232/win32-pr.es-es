---
description: Crea un enumerador de información de propiedad para cada dispositivo de adquisición de imágenes de Windows (WIA) 2,0 disponible.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2:: EnumDeviceInfo (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810778"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>IWiaDevMgr2:: EnumDeviceInfo (método)

Crea un enumerador de información de propiedad para cada dispositivo de adquisición de imágenes de Windows (WIA) 2,0 disponible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica el tipo de dispositivos WIA 2,0 que se va a enumerar.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**\_ \_ enumeración local de la DevInfo de WIA \_**


</dt> <dd>

Solo se enumeran los dispositivos de analizador activos conectados localmente.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**\_ \_ enumeración todo en la DevInfo de WIA \_**


</dt> <dd>

Todos los dispositivos se enumeran, tanto de forma local como remota, incluidos los dispositivos inactivos (desconectados) y los dispositivos solo de STI heredados.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Recibe la dirección de un puntero a la interfaz de [**\_ \_ información de desarrollo de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El método **IWiaDevMgr2:: EnumDeviceInfo** crea un objeto de enumerador que admite la interfaz de [**información de \_ desarrollo \_ de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . El método almacena un puntero a la interfaz **IEnumWIA \_ dev \_ info** en el parámetro *ppIEnum*. Las aplicaciones pueden usar el puntero de la interfaz de **IEnumWIA \_ dev \_ info** para enumerar las propiedades de cada dispositivo WIA 2,0 conectado al equipo del usuario.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
