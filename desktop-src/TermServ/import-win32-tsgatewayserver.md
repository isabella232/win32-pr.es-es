---
title: Método Import de la clase Win32_TSGatewayServer
description: Importa una configuración determinada en el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Método de importación Servicios de Escritorio remoto
- Método de importación Servicios de Escritorio remoto, clase Win32_TSGatewayServer
- Servicios de Escritorio remoto de clase Win32_TSGatewayServer, método Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996602"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Método Import de la \_ clase Win32 TSGatewayServer

Importa una configuración determinada en el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ImportType* \[ de\]
</dt> <dd>

Contenido que se va a importar. Establezca el tipo de importación mediante el establecimiento de los bits correspondientes en el parámetro *ImportType* . Puede establecer varios tipos de importación. Por ejemplo, si se establece el bit 0, se importarán Servicios de Escritorio remoto las directivas de autorización de conexión (Cap de RD). Si se establece el 0 y el segundo bit, se importarán tanto las Cap de RD como las directivas de autorización de recursos de Servicios de Escritorio remoto (RAP de RD).

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importar todos los Cap** (1)


</dt> <dd>

Importe todas las Cap de RD.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importar todos los servidores RADIUS** (2)


</dt> <dd>

Importe una lista de todos los servidores NPS (servidor de directivas de redes).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importar todas las rap** (4)


</dt> <dd>

Importe todas las rap de RD.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importar todos los RGs** (8)


</dt> <dd>

Importe todos los grupos de recursos.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importar todos los servidores de equilibrio** (16)


</dt> <dd>

Importe una lista de todos los servidores de equilibrio de carga.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importar la configuración de todos los servidores** (32)


</dt> <dd>

Importe la configuración de todos los servidores relacionados con la puerta de enlace de escritorio remoto.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importar todas las directivas de mantenimiento** (64)


</dt> <dd>

Importe todas las directivas de mantenimiento.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: * *

Este valor no se admite antes de Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ de\]
</dt> <dd>

La configuración como una cadena XML.

</dd> <dt>

*MergeOrReplace* \[ de\]
</dt> <dd>

Indica si se deben combinar o reemplazar los datos cuando se produce un conflicto.

> [!Note]  
> La fusión mediante combinación no se ha implementado todavía. Por lo tanto, se omite este valor de parámetro.

 

</dd> <dt>

*LogString* \[ enuncia\]
</dt> <dd>

La información de registro que se genera durante la operación de importación.

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

 

