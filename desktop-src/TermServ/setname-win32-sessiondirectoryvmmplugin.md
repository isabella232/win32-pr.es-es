---
title: Método SetName de la clase Win32_SessionDirectoryVMMPlugin
description: Establece el nombre del complemento.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- SetName (método) Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Clase Win32_SessionDirectoryVMMPlugin Servicios de Escritorio remoto, método SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359731"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetName de la \_ clase SessionDirectoryVMMPlugin de Win32

Establece el nombre del complemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ de\]
</dt> <dd>

Nombre del complemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





