---
description: Quita los parámetros DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) de un puerto Canal de fibra sintético en una máquina virtual.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Método RemoveFibreChannelChap de la Msvm_VirtualSystemManagementService clase
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
ms.openlocfilehash: 9b934839f6d908594ee58f0838c884fdedc48f372de061482ddf2147123a351c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147798"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RemoveFibreChannelChap de la clase \_ VirtualSystemManagementService de Msvm

Quita los parámetros DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) de un puerto Canal de fibra sintético en una máquina virtual. Este método producirá un error si la máquina virtual se está ejecutando.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FcPortSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contienen una instancia incrustada de la clase [**\_ Msvm SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que definen los puertos Canal de fibra sintéticos de los que quitar los parámetros DH-CHAP. La **propiedad InstanceID** de cada una de estas instancias identifica los elementos que se deben modificar.

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

 

 




