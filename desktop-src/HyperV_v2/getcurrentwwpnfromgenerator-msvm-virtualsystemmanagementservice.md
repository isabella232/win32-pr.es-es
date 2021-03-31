---
description: Proporciona la capacidad de obtener una vista previa del nombre de Puerto WWPN (WWPN) actual sin reservar el WWPN.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Método GetCurrentWwpnFromGenerator de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetCurrentWwpnFromGenerator
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 88e1fd8f19b4a0542744cbfff7058ed7e69a421d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001240"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetCurrentWwpnFromGenerator de la \_ clase VirtualSystemManagementService de MSVM

Proporciona la capacidad de obtener una vista previa del nombre de Puerto WWPN (WWPN) actual sin reservar el WWPN. El WWPN se genera desde el intervalo preconfigurado definido por las propiedades **MinimumWWPNAddress** y **MaximumWWPNAddress** de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) . Si se agota el intervalo definido por estas propiedades, el WWPN generado tendrá la entrada no válida "0000000000000000" y el valor devuelto indicará Success (0).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CurrentWwpn* \[ enuncia\]
</dt> <dd>

Una cadena que tendrá el valor del WWPN actual tal como lo usa el generador de WWPN. Será el mismo valor que será el primer WWPN generado por la siguiente llamada a [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md). Se le aplicará el formato de cadena como "01:23:45:67:89: AB: CD: EF".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




