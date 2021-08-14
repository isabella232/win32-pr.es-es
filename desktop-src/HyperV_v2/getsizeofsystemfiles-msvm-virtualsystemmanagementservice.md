---
description: Recupera el tamaño total de los archivos del sistema de la máquina virtual.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Método GetSizeOfSystemFiles de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 385235e407cac2dd67f3dade99e4d1c834d082dfe59b541020a4548e8eea383c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392908"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetSizeOfSystemFiles de la clase Msvm \_ VirtualSystemManagementService

Recupera el tamaño total de los archivos del sistema de la máquina virtual. Estos incluyen la configuración y los archivos de estado guardados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Vssd* \[ En\]
</dt> <dd>

Referencia a la instancia [**de CIM \_ VirtualSystemSettingData cuyo**](/previous-versions//cc136954(v=vs.85)) tamaño de archivos del sistema se va a recuperar. Esta instancia puede representar la creación de instancias actual de la máquina virtual o una instancia de una instantánea de máquina virtual.

</dd> <dt>

*Tamaño* \[ out\]
</dt> <dd>

Tamaño total, en bytes, de los archivos del sistema.

</dd> </dl>

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

 

