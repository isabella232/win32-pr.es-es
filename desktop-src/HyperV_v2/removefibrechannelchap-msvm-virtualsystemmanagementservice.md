---
description: Quita los parámetros DH-CHAP (Diffie Hellman-desafío de autenticación por desafío mutuo) de un puerto de Canal de fibra sintético en una máquina virtual.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Método RemoveFibreChannelChap de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686929"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RemoveFibreChannelChap de la \_ clase VirtualSystemManagementService de MSVM

Quita los parámetros DH-CHAP (Diffie Hellman-desafío de autenticación por desafío mutuo) de un puerto de Canal de fibra sintético en una máquina virtual. Este método producirá un error si la máquina virtual se está ejecutando.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FcPortSettings* \[ de\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que define los puertos canal de fibra sintéticos de los que se van a quitar los parámetros DH-CHAP. La propiedad **InstanceID** de cada una de estas instancias identifica los elementos que se van a modificar.

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

 

 




