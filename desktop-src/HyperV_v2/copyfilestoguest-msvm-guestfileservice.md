---
description: Copia los archivos del host de Hyper-V en la máquina virtual.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: Msvm_GuestFileService::CopyFilesToGuest (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e027d71faf8dda5769962d3c71d1fcfb5958c61c91993cf17fbf472d93aff50f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980485"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>Método \_ GuestFileService::CopyFilesToGuest de Msvm

Copia los archivos del host de Hyper-V en la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CopyFileToGuestSettings* \[ En\]
</dt> <dd>

Matriz de instancias de la clase [**\_ CopyFileToGuestSettingData de Msvm**](msvm-copyfiletoguestsettingdata.md) que representa un trabajo de operación del servicio de archivos invitado.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

> [!Note]  
> Este parámetro se agregó en Windows 10.

 

</dd> <dt>

*ParentPools* \[ out, opcional\]
</dt> <dd>

Matriz opcional de referencias [**\_ copyFileToGuestJob de Msvm**](msvm-copyfiletoguestjob.md) que se usan para supervisar el progreso de la operación. **CopyFilesToGuest** usa *ParentPools* si no se puede ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

> [!Note]  
> Este parámetro se quitó en Windows 10.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un valor de error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método activados: trabajo iniciado** (4096)
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
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ GuestFileService**](msvm-guestfileservice.md)
</dt> </dl>

 

 




