---
description: Llama a la biblioteca para obtener el estado de seguridad relativo al host, y el script o MSI que se va a usar.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Función WldpGetLockdownPolicy (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538751"
---
# <a name="wldpgetlockdownpolicy-function"></a>WldpGetLockdownPolicy función)

Llama a la biblioteca para obtener el estado de seguridad relativo al host, y el script o MSI que se va a usar. La función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones LoadLibrary y GetProcAddress para vincular dinámicamente a wldp.dll.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hostInformation* \[ en, opcional\]
</dt> <dd>

Estructura [**de \_ \_ información de host de WLDP**](wldp-host-information.md) que identifica el host y el archivo de origen que se van a evaluar.

</dd> <dt>

*lockdownState* \[ enuncia\]
</dt> <dd>

Proporciona el valor seguro de la Directiva resultante. Cuando! WLDP_LOCKDOWN_IS_OFF, UMCI está habilitado. También puede comprobar WLDP_LOCKDOWN_IS_AUDIT y WLDP_LOCKDOWN_IS_ENFORCE para determinar si una directiva está en modo de auditoría o de aplicación.
</dd> <dt>

*lockdownFlags* \[ de\]
</dt> <dd>

Se definen los siguientes valores de marca \_ WLDP \_ SKIPSIGNATUREVALIDATION 0x00000100: cuando se establece, se omite la validación de SaferIdentifyLevel, que omitirá si un script está firmado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve S \_ correcto si es correcto o un código de error en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se llama con \_ la información de host de WLDP \_ . SZSOURCE = null, se devuelve la Directiva genérica para el host.

Cuando se llama con la información de host de WLDP \_ \_ . DWHOSTID = WLDP ID. de \_ host \_ \_ global, WLDP \_ información de host \_ . szSource debe ser NULL y la función devolverá la directiva global del sistema.

DwFlag WLDP \_ Flags \_ SKIPSIGNATUREVALIDATION se puede usar para omitir la validación SaferIdentifyLevel (), que omitirá si un script está firmado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WLDP. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




