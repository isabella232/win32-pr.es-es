---
title: Método QueryOfflineInformation de la clase Win32_TSVm
description: Recupera las propiedades del servidor de escritorio virtual (VDS) actual, pero solo cuando el servidor está sin conexión.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Método QueryOfflineInformation Servicios de Escritorio remoto
- Método QueryOfflineInformation Servicios de Escritorio remoto, clase Win32_TSVm
- Win32_TSVm de clase Servicios de Escritorio remoto, método QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905380"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Método QueryOfflineInformation de la \_ clase TSVm de Win32

Recupera las propiedades del servidor de escritorio virtual (VDS) actual, pero solo cuando el servidor está sin conexión.

## <a name="syntax"></a>Sintaxis


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Compilación* \[ de enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve la versión de compilación de VDS.

</dd> <dt>

*CurrentVersion* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve la versión actual de VDS.

</dd> <dt>

*InstallationType* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve el tipo de instalación de VDS.

</dd> <dt>

*EditionId* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve el ID. de edición del VDS.

</dd> <dt>

*SysPrepImageState* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve el estado de la imagen de preparación del sistema de VDS.

</dd> <dt>

*SysPrepMode* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve el modo de preparación del sistema del VDS.

</dd> <dt>

*ProcArch* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve un valor que indica la arquitectura del procesador.

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

AMD64

</dd> </dl> </dd> <dt>

*fIsVmbusCapable* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente, indica si el sistema es compatible con VMBus.

</dd> <dt>

*fIsRdvIcInstalled* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente, indica si RDVIC está instalado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSVm**](win32-tsvm.md)
</dt> </dl>

 

 





