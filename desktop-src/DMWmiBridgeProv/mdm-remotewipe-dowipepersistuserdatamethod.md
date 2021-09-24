---
title: Método doWipePersistUserDataMethod de la MDM_RemoteWipe clase
description: Desencadena el dispositivo para iniciar el borrado remoto mientras se conservan las cuentas de usuario y los datos.
keywords:
- Método doWipePersistUserDataMethod
- Método doWipePersistUserDataMethod, MDM_RemoteWipe clase
- MDM_RemoteWipe, método doWipePersistUserDataMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipePersistUserDataMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 09/17/2021
ms.openlocfilehash: 00a9dd0ee93d71b2aeec3bb8b83a3b34bc044e05
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523990"
---
# <a name="dowipepersistuserdatamethod-method-of-the-mdm_remotewipe-class"></a>Método doWipePersistUserDataMethod de la MDM_RemoteWipe clase

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

Desencadena el dispositivo para iniciar el borrado remoto mientras se conservan las cuentas de usuario y los datos. Vea también [doWipePersistUserDataMethod](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Sintaxis

```mof
uint32 doWipePersistUserDataMethod(
  [in] string param
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*param* \[ En\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | DMMap \\ de MDM \\ de CIMv2 \\ raíz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MDM \_ RemoteWipe**](mdm-remotewipe.md)
</dt> <dt>

[Uso de scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>
