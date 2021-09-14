---
title: Método GetTStoLSConnectivityStatus de la Win32_TerminalServiceSetting clase
description: Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Método GetTStoLSConnectivityStatus Servicios de Escritorio remoto
- Método GetTStoLSConnectivityStatus Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374734"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Método GetTStoLSConnectivityStatus de la clase \_ TerminalServiceSetting de Win32

Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ServerName* \[ En\]
</dt> <dd>

Nombre del servidor de licencias del que se comprobará el estado de conectividad.

</dd> <dt>

*TStoLSConnectivityStatus* \[ out\]
</dt> <dd>

Valor que indica el estado de conectividad del servidor de licencias. Puede ser uno de los siguientes valores.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_ CONNECTABLE \_ UNKNOWN** (0)


</dt> <dd>

No se puede determinar el estado de conectividad.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_ \_ \_ WS08R2** VÁLIDO CONECTABLE (1)


</dt> <dd>

Servicios de Escritorio remoto conectarse al servidor de licencias Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_ \_ \_ WS08 VÁLIDO CONECTABLE** (2)


</dt> <dd>

Servicios de Escritorio remoto conectarse al servidor de licencias Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_ ERROR DE \_ COINCIDENCIA DE RTM DE LA VERSIÓN BETA \_ \_ CONECTABLE** (3)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero uno de los servidores ejecuta una versión beta del sistema operativo.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_ VERSIÓN INFERIOR \_ \_ CONECTABLE** (4)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero hay una incompatibilidad entre el servidor de licencias y el Servicios de Escritorio remoto host.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_ CONNECTABLE \_ NOT \_ IN \_ TSCGROUP** (5)


</dt> <dd>

La directiva de grupo de seguridad está habilitada en el servidor de licencias, Servicios de Escritorio remoto no forma parte de la directiva de grupo.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_ NO \_ CONECTABLE** (6)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_ VALIDEZ DESCONOCIDA \_ \_ CONECTABLE** (7)


</dt> <dd>

El servidor de licencias se puede conectar a , pero no se puede determinar la validez de la conexión.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_ ACCESO CONECTABLE \_ \_ PERO \_ DENEGADO** (8)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero la cuenta de usuario no tiene privilegios de administrador en el servidor de licencias.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_ \_ \_ WS08R2 \_ VDI** VÁLIDO CONECTABLE (9)


</dt> <dd>

Servicios de Escritorio remoto conectarse al servidor Windows Server 2008 R2 Infraestructura de escritorio virtual (VDI).

**Windows Server 2008 R2:** Este valor no se admite antes de Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_ CARACTERÍSTICA \_ CONECTABLE \_ NO \_ ADMITIDA** (10)


</dt> <dd>

No se admite la característica .

**Windows Server 2008 R2 y Windows Server 2008 R2 con SP1:** Este valor no se admite antes de Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_ LS \_ VÁLIDO \_ CONECTABLE** (11)


</dt> <dd>

El servidor de licencias es válido.

**Windows Server 2008 R2 y Windows Server 2008 R2 con SP1:** Este valor no se admite antes de Windows Server 2012.

</dd> </dl> </dd> </dl>

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
</dt> </dl>

 

 





