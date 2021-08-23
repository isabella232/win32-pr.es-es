---
description: Agrega parámetros DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) a un puerto Canal de fibra sintético en una máquina virtual.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Método AddFibreChannelChap de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26a9f99826e92a35462f0c42e8fce723168799177e96e0ae429aad45c99de928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562368"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddFibreChannelChap de la clase Msvm \_ VirtualSystemManagementService

Agrega parámetros DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) a un puerto Canal de fibra sintético en una máquina virtual. Este método producirá un error si la máquina virtual se está ejecutando.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FcPortSettings* \[ En\]
</dt> <dd>

Matriz de cadenas que contienen una instancia incrustada de la clase [**\_ Msvm SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que describe la configuración de los puertos Canal de fibra sintéticos para las máquinas virtuales. La **propiedad InstanceID** de cada una de estas instancias identifica los elementos que se deben modificar.

</dd> <dt>

*SecretEncoding* \[ En\]
</dt> <dd>

Especifica el tipo de codificación para el secreto compartido.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**ASCII imprimible** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binario** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SharedSecret* \[ En\]
</dt> <dd>

Especifica el secreto compartido.

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

**El sistema no está disponible** (32777)
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

 

 




