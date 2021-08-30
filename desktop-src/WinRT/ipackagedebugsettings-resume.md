---
description: Reanuda los procesos del paquete si están suspendidos actualmente.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: IPackageDebugSettings::Resume (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 6871aea0fc18ce64939fa1bba06946f8a3a1c260e341b1dfa500a71f273a883b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121585"
---
# <a name="ipackagedebugsettingsresume-method"></a>IPackageDebugSettings::Resume (Método)

Reanuda los procesos del paquete si están suspendidos actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packageFullName* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre completo del paquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Cada proceso recibe el [**evento Resuming.**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Puede ser útil para los desarrolladores ver cómo responden sus aplicaciones a este evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
