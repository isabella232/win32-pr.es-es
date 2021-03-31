---
title: Método GetTStoLSConnectivityStatus de la clase Win32_TerminalServiceSetting
description: Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Método GetTStoLSConnectivityStatus Servicios de Escritorio remoto
- Método GetTStoLSConnectivityStatus Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetTStoLSConnectivityStatus
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491339"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Método GetTStoLSConnectivityStatus de la \_ clase TerminalServiceSetting de Win32

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

*NombreDeServidor* \[ de\]
</dt> <dd>

Nombre del servidor de licencias para comprobar el estado de conectividad.

</dd> <dt>

*TStoLSConnectivityStatus* \[ enuncia\]
</dt> <dd>

Valor que indica el estado de Conectividad del servidor de licencias. Puede ser uno de los valores siguientes.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_ CONNECTable \_ Unknown** (0)


</dt> <dd>

No se puede determinar el estado de conectividad.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_ \_ \_ WS08R2 válido y conectable** (1)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias de Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_ \_ \_ WS08 válido y conectable** (2)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias de Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_ \_ \_ \_ No coincide la versión RTM de beta conectable** (3)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero uno de los servidores está ejecutando una versión beta del sistema operativo.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_ \_ \_ Versión más antigua conectable** (4)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero hay una incompatibilidad entre el servidor de licencias y el servidor host de Servicios de Escritorio remoto.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_ CONNECTable \_ no está \_ en \_ TSCGROUP** (5)


</dt> <dd>

La Directiva de grupo de seguridad está habilitada en el servidor de licencias, pero Servicios de Escritorio remoto no es parte de la Directiva de grupo.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_ NO \_ conectable** (6)


</dt> <dd>

Servicios de Escritorio remoto no se puede conectar al servidor de licencias.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_ \_ \_ Validez desconocida conectable** (7)


</dt> <dd>

El servidor de licencias puede conectarse a, pero no se puede determinar la validez de la conexión.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_ CONNECTable \_ pero \_ acceso \_ denegado** (8)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero la cuenta de usuario no tiene privilegios de administrador en el servidor de licencias.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_ CONNECTable \_ \_ WS08R2 válido \_** (9)


</dt> <dd>

Servicios de Escritorio remoto puede conectarse al servidor de infraestructura de escritorio virtual (VDI) de Windows Server 2008 R2.

**Windows Server 2008 R2:** Este valor no se admite antes de Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_ No se \_ \_ \_ admite la característica conectable** (10)


</dt> <dd>

No se admite la característica.

**Windows server 2008 R2 y Windows server 2008 R2 con SP1:** Este valor no se admite antes de Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_ CONNECTable \_ válido \_ LS** (11)


</dt> <dd>

El servidor de licencias es válido.

**Windows server 2008 R2 y Windows server 2008 R2 con SP1:** Este valor no se admite antes de Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





