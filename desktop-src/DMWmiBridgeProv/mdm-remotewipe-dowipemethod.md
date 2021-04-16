---
title: método doWipeMethod de la clase MDM_RemoteWipe
description: Desencadena el dispositivo para iniciar el borrado remoto.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- método doWipeMethod
- método doWipeMethod, clase MDM_RemoteWipe
- Clase MDM_RemoteWipe, método doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489178"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>método doWipeMethod de la \_ clase RemoteWipe de MDM

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Desencadena el dispositivo para iniciar el borrado remoto. Vea [también.](/windows/client-management/mdm/remotewipe-csp)

## <a name="syntax"></a>Sintaxis


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*parámetro* \[ de\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | DMMap de MDM raíz de \\ CIMv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RemoteWipe de MDM \_**](mdm-remotewipe.md)
</dt> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

