---
description: Reanuda los procesos del paquete si están suspendidos.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'IPackageDebugSettings:: resume (método)'
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
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715152"
---
# <a name="ipackagedebugsettingsresume-method"></a>IPackageDebugSettings:: resume (método)

Reanuda los procesos del paquete si están suspendidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packageFullName* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre completo del paquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cada proceso recibe el evento [**RESUMING**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Puede ser útil para los desarrolladores recorrer el modo en que sus aplicaciones responden a este evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
