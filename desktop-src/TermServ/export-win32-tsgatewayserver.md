---
title: Método Export de la clase Win32_TSGatewayServer
description: Devuelve la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) como una cadena XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Método de exportación Servicios de Escritorio remoto
- Método de exportación Servicios de Escritorio remoto, Win32_TSGatewayServer clase)
- Win32_TSGatewayServer de clase Servicios de Escritorio remoto, método Export
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997154"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Método Export de la \_ clase Win32 TSGatewayServer

Devuelve la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) como una cadena XML.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ExportType* \[ de\]
</dt> <dd>

Contenido que se va a exportar. Establezca el tipo de exportación mediante el establecimiento de los bits correspondientes en el parámetro *ExportType* . Puede establecer varios tipos de exportación. Por ejemplo, si se establece el bit 0, se exportarán Servicios de Escritorio remoto las directivas de autorización de conexión (Cap de RD). Si se establece el 0 y el segundo bit, se exportarán tanto las Cap de RD como las directivas de autorización de recursos de Servicios de Escritorio remoto (RAP de RD).

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Exportar todos los Cap** (1)


</dt> <dd>

Exportar todas las Cap de RD.

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Exportar todos los servidores RADIUS** (2)


</dt> <dd>

Exporte una lista de todos los servidores NPS (servidor de directivas de redes).

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Exportar todas las rap** (4)


</dt> <dd>

Exportar todas las rap de RD.

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Exportar todos los RGs** (8)


</dt> <dd>

Exporte todos los grupos de recursos.

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Exportar todos los servidores de equilibrio** (16)


</dt> <dd>

Exporte una lista de todos los servidores de equilibrio de carga.

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Exportar toda la configuración del servidor** (32)


</dt> <dd>

Exporte todas las opciones del servidor relacionadas con la puerta de enlace de escritorio remoto.

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Exportar todas las directivas de mantenimiento** (64)


</dt> <dd>

Exporte todas las directivas de mantenimiento.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: * *

Este valor no se admite antes de Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ enuncia\]
</dt> <dd>

Cadena XML.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

