---
description: Crea un enumerador de información de propiedades para cada dispositivo Windows adquisición de imágenes (WIA) 2.0 disponible.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: Método IWiaDevMgr2::EnumDeviceInfo (Wia.h)
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
ms.openlocfilehash: 8b646c494d9793986373d45db2d89dfde91e744196d86d28aceab35874f504d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208727"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>IWiaDevMgr2::EnumDeviceInfo (método)

Crea un enumerador de información de propiedades para cada dispositivo Windows adquisición de imágenes (WIA) 2.0 disponible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica el tipo de dispositivos WIA 2.0 que se enumerará.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DEVINFO \_ ENUM \_ LOCAL**


</dt> <dd>

Solo se enumeran los dispositivos de escáner activo conectados localmente.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ ENUM \_ ALL**


</dt> <dd>

Todos los dispositivos se enumeran, tanto de forma local como remota, incluidos los dispositivos inactivos (desconectados) y los dispositivos heredados solo DESER.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Recibe la dirección de un puntero a la interfaz INFO de [**IEnumWIA \_ \_ DEV.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **método IWiaDevMgr2::EnumDeviceInfo** crea un objeto enumerador que admite la [**interfaz INFO de IEnumWIA \_ DEV. \_**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) El método almacena un puntero a la **interfaz INFO de IEnumWIA \_ DEV \_** en el parámetro *ppIEnum*. Las aplicaciones pueden usar el puntero de interfaz INFO de **IEnumWIA \_ \_ DEV** para enumerar las propiedades de cada dispositivo WIA 2.0 conectado al equipo del usuario.

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
