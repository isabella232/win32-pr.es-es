---
title: MPSIGUPDATE_DATA estructura (MpClient.h)
description: Datos de notificación pasados a la función de devolución de llamada de actualización de firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA estructura heredada de Windows environment
- PMPSIGUPDATE_DATA puntero de estructura Legacy Windows Environment Features
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252572"
---
# <a name="mpsigupdate_data-structure"></a>Estructura DE DATOS MPSIGUPDATE \_

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



## <a name="members"></a>Members

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

Número total de actualizaciones que se descargarán o instalarán.

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de índice de base cero que especifica qué actualización de las necesarias se está descargando o instalando actualmente.

</dd> <dt>

**eType**
</dt> <dd>

Tipo: **MPSIGUPDATE \_ TYPE**

</dd> <dd>

Tipo de actualización. Uno de los siguientes valores posibles:



| Value                                                                                                                                                                                                                             | Significado                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ TIPO \_ NONE**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ ADMINISTRADO**</dt> </dl>                                   | Actualización de WSUS. Cancelar requiere derechos de administrador.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE, \_ TIPO \_ HTTP**</dt> </dl>                                            | Actualización HTTP. No se necesitan derechos de administrador para cancelar.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE, \_ TIPO \_ HTTP \_ SRV**</dt> </dl>                               | HTTP desde el servicio. Cancelar requiere derechos de administrador.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**MPSIGUPDATE \_ TYPE \_ UNC**</dt> </dl>                                               | Recurso compartido UNC. No se necesitan derechos de administrador para cancelar.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ NO ADMINISTRADO**</dt> </dl>                             | Actualización de MU/WU. Cancelar requiere derechos de administrador.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**PLATAFORMA ADMINISTRADA DE TIPO MPSIGUPDATE \_ \_ \_**</dt> </dl>       | Actualización de WSUS para PLATFORM. Cancelar requiere derechos de administrador.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**MPSIGUPDATE, \_ TIPO \_ PLATAFORMA NO \_ ADMINISTRADA**</dt> </dl> | Actualización de MU/WU para PLATFORM. Cancelar requiere derechos de administrador.<br/> |



 

</dd> <dt>

**Fase**
</dt> <dd>

Tipo: **FASE DE ACTUALIZACIÓN DE \_ \_ MP**

</dd> <dd>

Fase de actualización. Uno de los siguientes valores posibles:



| Value                                                                                                                                                                         | Significado                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**FASE \_ DE MP \_ DESCONOCIDA**</dt> </dl>       | Fase de actualización desconocida.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**ACTUALIZACIÓN \_ DE LA BÚSQUEDA DE \_ MP**</dt> </dl>       | Actualice la fase de búsqueda.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**ACTUALIZACIÓN \_ DE DESCARGA DE \_ MP**</dt> </dl> | Actualizar la fase de descarga.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**ACTUALIZACIÓN \_ DE INSTALACIÓN DE \_ MP**</dt> </dl>    | Actualice la fase de instalación.<br/>  |



 

</dd> <dt>

**Path**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Ruta de acceso de actualización.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





