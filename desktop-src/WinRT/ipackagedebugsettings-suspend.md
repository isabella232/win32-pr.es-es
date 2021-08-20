---
description: Suspende los procesos del paquete si se están ejecutando actualmente.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: IPackageDebugSettings::Suspend (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 0517ce3cca6a8e74f19b053897511062cefa252297d3a0e6633d4678c0deaa95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822818"
---
# <a name="ipackagedebugsettingssuspend-method"></a>IPackageDebugSettings::Suspend (Método)

Suspende los procesos del paquete si se están ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Suspend(
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

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                            | Descripción                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | La operación se realizó correctamente.<br/>              |
| <dl> <dt>**E \_ ILLEGAL \_ STATECHANGE**</dt> </dl> | El proceso no se está ejecutando actualmente.<br/> |



 

## <a name="remarks"></a>Comentarios

Cada proceso recibe el [**evento Suspending.**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) Puede ser útil para los desarrolladores ver cómo responden sus aplicaciones a este evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
