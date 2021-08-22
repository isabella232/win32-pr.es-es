---
description: Genera un conjunto de nombres de puertos world wide (WWPN).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Método GenerateWwpn de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1952954d107185fdcc31634b9d0e19bd4cd3450db5a63d78aa3ef823cdf38afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532525"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GenerateWwpn de la clase Msvm \_ VirtualSystemManagementService

Genera un conjunto de nombres de puertos world wide (WWPN). Los WWPN se generan desde dentro del intervalo preconfigurado definido por las propiedades **MinimumWWPNAddress** y **MaximumWWPNAddress** de la clase [**Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md) Si el número válido de WWPN que se pueden generar es menor que el número solicitado, las entradas restantes de la matriz *GeneratedWwpn* tendrán la entrada no válida "000000000000000000" y el valor devuelto indicará que se ha hecho correctamente (0).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumberOfWwpns* \[ En\]
</dt> <dd>

Número de WWPN que se generarán.

</dd> <dt>

*GeneratedWwpn* \[ out\]
</dt> <dd>

Matriz de cadenas, cada una de las cuales contendrá un WWPN generado. Se le dará formato en forma de cadena como "01:23:45:67:89:ab:cd:ef".

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




