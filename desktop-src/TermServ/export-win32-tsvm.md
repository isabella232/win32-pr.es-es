---
title: Método Export de la clase Win32_TSVm
description: Recupera la información de supervisión de sesión de máquina virtual.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Método de exportación Servicios de Escritorio remoto
- Método de exportación Servicios de Escritorio remoto, Win32_TSVm clase)
- Win32_TSVm de clase Servicios de Escritorio remoto, método Export
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676643"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Método Export de la \_ clase Win32 TSVm

Recupera la información de supervisión de sesión de máquina virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ExportFolderPath* \[ de\]
</dt> <dd>

Ruta de acceso al lugar donde se exportará la máquina virtual.

</dd> <dt>

*ExportJobObjectPath* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve la ruta de acceso del objeto ConcreteJob de HyperV.

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

 

 





