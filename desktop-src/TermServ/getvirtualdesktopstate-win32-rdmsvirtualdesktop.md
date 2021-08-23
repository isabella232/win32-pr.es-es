---
title: Método GetVirtualDesktopState de la Win32_RDMSVirtualDesktop clase
description: Recupera el estado del escritorio virtual.
ms.assetid: 176096ba-2b5f-428c-9216-02e3e97be64e
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopState Servicios de Escritorio remoto
- Método GetVirtualDesktopState Servicios de Escritorio remoto , Win32_RDMSVirtualDesktop clase
- Win32_RDMSVirtualDesktop clase Servicios de Escritorio remoto , método GetVirtualDesktopState
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb59cf90f436d3d44c20daa2a7f8146f688d012310253bafcf0185fe804b89fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059473"
---
# <a name="getvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopState de la clase \_ RDMSVirtualDesktop de Win32

Recupera el estado del escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVirtualDesktopState(
  [out] uint32 VMState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VMState* \[ out\]
</dt> <dd>

Recibe un valor que indica el estado de la máquina virtual.

Este parámetro puede establecerse en uno de los siguientes valores:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0 (valor predeterminado))


</dt> <dd>

No se pudo determinar el estado de la máquina virtual.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)


</dt> <dd>

La máquina virtual se está ejecutando.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)


</dt> <dd>

La máquina virtual está desactivada.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**En pausa** (32768)


</dt> <dd>

La máquina virtual está en pausa.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (32769)


</dt> <dd>

La máquina virtual está en un estado guardado.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partir** de (32770)


</dt> <dd>

La máquina virtual se está iniciando.

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Guardar** (32773)


</dt> <dd>

La máquina virtual está guardando su estado.

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (32774)


</dt> <dd>

La máquina virtual se está apagando.

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausar** (32776)


</dt> <dd>

La máquina virtual está en pausa.

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Reanudación** (32777)


</dt> <dd>

La máquina virtual se reanuda desde un estado en pausa.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RDMSVirtualDesktop de Win32 \_**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





