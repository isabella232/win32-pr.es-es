---
description: Suspende los procesos del paquete si se están ejecutando actualmente.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'IPackageDebugSettings:: Suspend (método)'
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
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809770"
---
# <a name="ipackagedebugsettingssuspend-method"></a>IPackageDebugSettings:: Suspend (método)

Suspende los procesos del paquete si se están ejecutando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Suspend(
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

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                            | Descripción                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | La operación se realizó correctamente.<br/>              |
| <dl> <dt>**E \_ STATECHANGE no válido \_**</dt> </dl> | El proceso no se está ejecutando actualmente.<br/> |



 

## <a name="remarks"></a>Observaciones

Cada proceso recibe el evento de [**suspensión**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) . Puede ser útil para los desarrolladores recorrer el modo en que sus aplicaciones responden a este evento.

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

 

 
