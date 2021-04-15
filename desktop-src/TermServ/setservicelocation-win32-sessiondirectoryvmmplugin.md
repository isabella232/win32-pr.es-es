---
title: Método SetServiceLocation de la clase Win32_SessionDirectoryVMMPlugin
description: Establece la ubicación del servicio para el complemento.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Método SetServiceLocation Servicios de Escritorio remoto
- Método SetServiceLocation Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método SetServiceLocation
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534551"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetServiceLocation de la \_ clase SessionDirectoryVMMPlugin de Win32

Establece la ubicación del servicio para el complemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sServiceLocation* \[ de\]
</dt> <dd>

La ubicación del servicio en la que debe ponerse en contacto el complemento.

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

 

 





