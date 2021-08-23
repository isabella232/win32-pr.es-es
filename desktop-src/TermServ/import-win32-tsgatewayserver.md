---
title: Método import de la Win32_TSGatewayServer clase
description: Importa una configuración determinada al servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Importación de métodos Servicios de Escritorio remoto
- Método import Servicios de Escritorio remoto , Win32_TSGatewayServer clase
- Win32_TSGatewayServer clase Servicios de Escritorio remoto , Método Import
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
ms.openlocfilehash: 2629e8e44acd0f617e86a846cc127ab77250673c8612f2d2f53ab8c0238d9f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574575"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Método import de la clase TSGatewayServer de Win32 \_

Importa una configuración determinada al servidor Escritorio remoto Gateway (puerta de enlace de Escritorio remoto).

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

*ImportType* \[ En\]
</dt> <dd>

Contenido que se importará. Establezca el tipo de importación estableciendo los bits correspondientes en *el parámetro ImportType.* Puede establecer varios tipos de importación. Por ejemplo, si se establece el bit 0, Servicios de Escritorio remoto directivas de autorización de conexión (CAP de Escritorio remoto) se importarán. Si se establecen los dos bits 0 y 2, se importarán las CAP de Escritorio remoto y Servicios de Escritorio remoto de autorización de recursos (RAP de Escritorio remoto).

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importar todas las CAP** (1)


</dt> <dd>

Importe todas las CAP de Escritorio remoto.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importar todos los servidores Radius** (2)


</dt> <dd>

Importe una lista de todos los servidores de Servidor de directivas de red (NPS).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importar todas las RAP** (4)


</dt> <dd>

Importe todos los RAP de Escritorio remoto.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importar todos los RG** (8)


</dt> <dd>

Importe todos los grupos de recursos.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importar todos los servidores de equilibrio de** carga (16)


</dt> <dd>

Importe una lista de todos los servidores de equilibrio de carga.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importar todos los servidores Configuración** (32)


</dt> <dd>

Importe toda la configuración del servidor relacionada con la puerta de enlace de Escritorio remoto.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importar todas las directivas de mantenimiento** (64)


</dt> <dd>

Importe todas las directivas de mantenimiento.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: **

Este valor no se admite antes de Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ En\]
</dt> <dd>

La configuración como una cadena XML.

</dd> <dt>

*MergeOrReplace* \[ En\]
</dt> <dd>

Indica si se deben combinar o reemplazar datos cuando se produce un conflicto.

> [!Note]  
> La combinación aún no se ha implementado. Por lo tanto, este valor de parámetro se omite.

 

</dd> <dt>

*LogString* \[ out\]
</dt> <dd>

Información de registro que se genera durante la operación de importación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayServer de Win32 \_**](win32-tsgatewayserver.md)
</dt> </dl>

 

