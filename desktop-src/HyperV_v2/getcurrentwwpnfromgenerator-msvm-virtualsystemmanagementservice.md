---
description: Proporciona la capacidad de obtener una vista previa del nombre de puerto world wide (WWPN) actual sin que el WWPN esté reservado.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Método GetCurrentWwpnFromGenerator de la Msvm_VirtualSystemManagementService clase
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
ms.openlocfilehash: 196ad781075128eab42c6daabf7d6ccd6906df1e67e348ebea0d9418cbb08c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393287"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetCurrentWwpnFromGenerator de la clase \_ VirtualSystemManagementService de Msvm

Proporciona la capacidad de obtener una vista previa del nombre de puerto world wide (WWPN) actual sin que el WWPN esté reservado. El WWPN se genera desde dentro del intervalo preconfigurado definido por las propiedades **MinimumWWPNAddress** y **MaximumWWPNAddress** de la clase [**Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md) Si se agota el intervalo definido por estas propiedades, el WWPN generado tendrá la entrada no válida "00000000000000000" y el valor devuelto indicará correcto (0).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CurrentWwpn* \[ out\]
</dt> <dd>

Cadena que tendrá el valor del WWPN actual tal y como lo usa el generador WWPN. Este será el mismo valor que será el primer WWPN generado por la llamada subsiguiente a [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md). Se le dará formato en forma de cadena como "01:23:45:67:89:ab:cd:ef".

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

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




