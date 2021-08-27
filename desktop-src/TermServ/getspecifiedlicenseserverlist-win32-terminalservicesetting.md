---
title: Método GetSpecifiedLicenseServerList de la Win32_TerminalServiceSetting clase
description: Recupera la lista de servidores de licencias especificados.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Método GetSpecifiedLicenseServerList Servicios de Escritorio remoto
- Método GetSpecifiedLicenseServerList Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 359d348dc759534d1f3ca070f443f4207aa8ddba0c73ab989d0fa8c0ab5397fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033755"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Método GetSpecifiedLicenseServerList de la clase TerminalServiceSetting de Win32 \_

Recupera la lista de servidores de licencias especificados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SpecifiedLSList* \[ out\]
</dt> <dd>

Matriz de cadenas que recibe la lista de servidores de licencias. Si no hay servidores de licencias, esta matriz estará vacía.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





