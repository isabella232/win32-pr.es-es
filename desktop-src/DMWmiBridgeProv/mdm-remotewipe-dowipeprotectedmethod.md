---
title: Método doWipeProtectedMethod de la MDM_RemoteWipe clase
description: Desencadena el dispositivo para iniciar el borrado remoto en el dispositivo y limpiar completamente la unidad interna. En algunas configuraciones de dispositivo, este comando podría dejar que el dispositivo no pueda arrancar.
keywords:
- Método doWipeProtectedMethod
- Método doWipeProtectedMethod, MDM_RemoteWipe clase
- MDM_RemoteWipe, método doWipeProtectedMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeProtectedMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 09/17/2021
ms.openlocfilehash: 792d4e412b8a16869bbfa33229abe541be1c952e
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523988"
---
# <a name="dowipeprotectedmethod-method-of-the-mdm_remotewipe-class"></a>Método doWipeProtectedMethod de la MDM_RemoteWipe clase

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

Desencadena el dispositivo para iniciar el borrado remoto en el dispositivo y limpiar completamente la unidad interna. En algunas configuraciones de dispositivo, este comando podría dejar que el dispositivo no pueda arrancar. Vea también [doWipePersistProvisionedDataMethod](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Sintaxis

```mof
uint32 doWipeProtectedMethod(
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
