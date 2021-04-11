---
description: Llama a la biblioteca para validar si se puede llamar a un CLSID determinado.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Función WldpIsClassInApprovedList (WLDP. h)
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
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152781"
---
# <a name="wldpisclassinapprovedlist-function"></a>WldpIsClassInApprovedList función)

Llama a la biblioteca para validar si se puede llamar a un **CLSID** determinado. La función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones LoadLibrary y GetProcAddress para vincular dinámicamente a wldp.dll.

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

*classID* 
</dt> <dd>

IDENTIFICADOR de clase COM cuya aprobación se va a comprobar.

</dd> <dt>

*hostInformation* \[ de\]
</dt> <dd>

Una estructura de [**\_ \_ información del host de WLDP**](wldp-host-information.md) que identifica el host que se va a evaluar.

</dd> <dt>

*isApproved* \[ enuncia\]
</dt> <dd>

Si se completa correctamente, contiene **true** si se aprueba el identificador de clase; en caso contrario, **false**.

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




