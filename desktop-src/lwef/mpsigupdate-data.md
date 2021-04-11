---
title: MPSIGUPDATE_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada de actualización de firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSIGUPDATE_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150572"
---
# <a name="mpsigupdate_data-structure"></a>\_Estructura de datos MPSIGUPDATE

Datos de notificación pasados a la función de devolución de llamada de actualización de firma.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwPercentComplete**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Una estimación del porcentaje en todas las actualizaciones que se han descargado o instalado.

</dd> <dt>

**dwTotalUpdates**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número total de actualizaciones para descargar o instalar.

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de índice de base cero que especifica qué actualización entre las necesarias se está descargando o instalando actualmente.

</dd> <dt>

**eType**
</dt> <dd>

Tipo: **MPSIGUPDATE \_ Type**

</dd> <dd>

Tipo de actualización. Uno de los siguientes valores posibles:



| Value                                                                                                                                                                                                                             | Significado                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ ninguno**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**\_tipo MPSIGUPDATE \_ administrado**</dt> </dl>                                   | Actualización de WSUS. La cancelación requiere derechos de administrador.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ http**</dt> </dl>                                            | Actualización HTTP. Derechos de administrador no necesarios para cancelar.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ http \_ SRV**</dt> </dl>                               | HTTP desde el servicio. La cancelación requiere derechos de administrador.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ UNC**</dt> </dl>                                               | Recurso compartido UNC. Derechos de administrador no necesarios para cancelar.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**tipo de MPSIGUPDATE \_ \_ no administrado**</dt> </dl>                             | Actualización de MU/WU. La cancelación requiere derechos de administrador.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**\_ \_ plataforma administrada de tipo MPSIGUPDATE \_**</dt> </dl>       | Actualización de WSUS para la plataforma. La cancelación requiere derechos de administrador.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**MPSIGUPDATE \_ tipo de \_ plataforma no administrada \_**</dt> </dl> | Actualización de MU/WU para la plataforma. La cancelación requiere derechos de administrador.<br/> |



 

</dd> <dt>

**Fase**
</dt> <dd>

Tipo: **\_ \_ fase de actualización del módulo de administración**

</dd> <dd>

Actualizar fase. Uno de los siguientes valores posibles:



| Value                                                                                                                                                                         | Significado                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**fase de MP \_ \_ desconocida**</dt> </dl>       | Fase de actualización desconocida.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**actualización de la búsqueda de MP \_ \_**</dt> </dl>       | Actualizar la fase de búsqueda.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**actualización de módulo de administración \_ \_**</dt> </dl> | Actualizar la fase de descarga.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**actualización de la instalación de MP \_ \_**</dt> </dl>    | Actualizar la fase de instalación.<br/>  |



 

</dd> <dt>

**Ruta de acceso**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Ruta de actualización.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





