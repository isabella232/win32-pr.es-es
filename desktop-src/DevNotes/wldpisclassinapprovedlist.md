---
description: Llama a la biblioteca para validar si es seguro llamar a un CLSID determinado.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Función WldpIsClassInApprovedList (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: ef4f6a719a1fe5146badbe59239dc16f9031f553ee8bba189c838dddcb641d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642045"
---
# <a name="wldpisclassinapprovedlist-function"></a>Función WldpIsClassInApprovedList

Llama a la biblioteca para validar si es seguro llamar a un **CLSID** determinado. La función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones LoadLibrary y GetProcAddress para vincular dinámicamente a wldp.dll.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Classid* 
</dt> <dd>

Identificador de clase COM para comprobar la aprobación.

</dd> <dt>

*hostInformation* \[ En\]
</dt> <dd>

Estructura [**DE INFORMACIÓN DE HOST \_ \_ DE WLDP**](wldp-host-information.md) que identifica el host que se va a evaluar.

</dd> <dt>

*isApproved* \[ out\]
</dt> <dd>

Si se completa correctamente, **contiene TRUE** si se aprueba el identificador de clase; de lo contrario, **FALSE**.

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ OK si se** realiza correctamente o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




