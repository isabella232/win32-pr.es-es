---
description: Solicita el Servicios de Escritorio remoto dispositivo virtual para iniciar una conexión de canalización con la máquina virtual.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Método EnableEndPoints de la clase Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275553"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a>Método EnableEndPoints de la \_ clase RdvComponent de MSVM

Solicita el Servicios de Escritorio remoto dispositivo virtual para iniciar una conexión de canalización con la máquina virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
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

**Memoria insuficiente** (32774)
</dt> <dt>

**No se encontró el archivo** (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> <dt>

 (32779)
</dt> <dt>

 (32780)
</dt> <dt>

 (32781)
</dt> <dt>

 (32782)
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

[**MSVM \_ RdvComponent**](msvm-rdvcomponent.md)
</dt> </dl>

 

 




