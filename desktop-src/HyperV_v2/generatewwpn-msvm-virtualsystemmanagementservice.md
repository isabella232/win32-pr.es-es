---
description: Genera un conjunto de nombres de Puerto WWPN (WWPN).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Método GenerateWwpn de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686897"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GenerateWwpn de la \_ clase VirtualSystemManagementService de MSVM

Genera un conjunto de nombres de Puerto WWPN (WWPN). Los WWPN se generan desde el intervalo preconfigurado definido por las propiedades **MinimumWWPNAddress** y **MaximumWWPNAddress** de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) . Si el número de WWPN válido que se puede generar es menor que el número solicitado, las entradas restantes de la matriz *GeneratedWwpn* tendrán la entrada no válida de "0000000000000000" y el valor devuelto indicará Success (0).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumberOfWwpns* \[ de\]
</dt> <dd>

Número de WWPN que se van a generar.

</dd> <dt>

*GeneratedWwpn* \[ enuncia\]
</dt> <dd>

Matriz de cadenas, cada una de las cuales contendrá un WWPN generado. Se le aplicará el formato de cadena como "01:23:45:67:89: AB: CD: EF".

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

 

 




