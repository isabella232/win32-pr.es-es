---
title: Método doWipePersistProvisionedDataMethod de la MDM_RemoteWipe secundaria
description: Desencadena el dispositivo para realizar una copia de seguridad de los datos de aprovisionamiento en una ubicación persistente y realizar un borrado remoto en el dispositivo. La información de la que se ha hecho una copia de seguridad se restaurará y se aplicará al dispositivo cuando se reanude.
keywords:
- Método doWipePersistProvisionedDataMethod
- Método doWipePersistProvisionedDataMethod, MDM_RemoteWipe clase
- MDM_RemoteWipe, método doWipePersistProvisionedDataMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipePersistProvisionedDataMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f346b520499c6a6d0eb5c181f8fd9b5dcd0208b
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523989"
---
# <a name="dowipepersistprovisioneddatamethod-method-of-the-mdm_remotewipe-class"></a>Método doWipePersistProvisionedDataMethod de la MDM_RemoteWipe secundaria

> [!NOTE]
> Parte de la información está relacionada con el producto publicado previamente, que se puede modificar considerablemente antes de **su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información proporcionada aquí.** 
 ![ Imagen](https://user-images.githubusercontent.com/31261191/133865694-1fae8e8b-c3ba-41a9-bcba-dbb67a6e2130.png)

Desencadena el dispositivo para realizar una copia de seguridad de los datos de aprovisionamiento en una ubicación persistente y realizar un borrado remoto en el dispositivo. La información de la que se ha hecho una copia de seguridad se restaurará y se aplicará al dispositivo cuando se reanude. Vea también [doWipePersistProvisionedDataMethod](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Sintaxis

```mof
uint32 doWipePersistProvisionedDataMethod(
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
