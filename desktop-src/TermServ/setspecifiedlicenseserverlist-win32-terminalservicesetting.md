---
title: Método SetSpecifiedLicenseServerList de la Win32_TerminalServiceSetting clase
description: Actualiza la lista de servidores de licencias especificados, reemplazando los servidores de licencias especificados existentes.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- Método SetSpecifiedLicenseServerList Servicios de Escritorio remoto
- Método SetSpecifiedLicenseServerList Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7591f26bb2678d6feefc69b46cc4380299347f7c59755b0721f329023e6f92bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127382"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Método SetSpecifiedLicenseServerList de la clase \_ TerminalServiceSetting de Win32

Actualiza la lista de servidores de licencias especificados, reemplazando los servidores de licencias especificados existentes.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SpecifiedLSList* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene la nueva lista de servidores de licencias especificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





