---
title: MPSIGUPDATE_DATA estructura (MpClient.h)
description: Datos de notificación pasados a la función de devolución de llamada de actualización de firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA estructura heredada de Windows environment
- PMPSIGUPDATE_DATA puntero de estructura heredado de Windows environment
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
ms.openlocfilehash: d3c117b92882a24a825aee5c5b008e10721c40b8a93d26a9a677bb79858635c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476257"
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



## <a name="members"></a>Miembros

<dl> <dt>

**dwPercentComplete**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Una estimación del porcentaje de todas las actualizaciones que se han descargado o instalado.

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

Tipo: **MPSIGUPDATE \_ TYPE**

</dd> <dd>

Tipo de actualización. Uno de los siguientes valores posibles:



| Valor                                                                                                                                                                                                                             | Significado                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ TIPO \_ NONE**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ ADMINISTRADO**</dt> </dl>                                   | Actualización de WSUS. Cancelar requiere derechos de administrador.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE, \_ TIPO \_ HTTP**</dt> </dl>                                            | Actualización HTTP. No se necesitan derechos de administrador para cancelar.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE, \_ TIPO \_ HTTP \_ SRV**</dt> </dl>                               | HTTP desde el servicio. Cancelar requiere derechos de administrador.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**TIPO \_ UNC DE MPSIGUPDATE \_**</dt> </dl>                                               | Recurso compartido UNC. No se necesitan derechos de administrador para cancelar.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ NO ADMINISTRADO**</dt> </dl>                             | Actualización de MU/WU. Cancelar requiere derechos de administrador.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**PLATAFORMA ADMINISTRADA DE TIPO MPSIGUPDATE \_ \_ \_**</dt> </dl>       | Actualización de WSUS para PLATFORM. Cancelar requiere derechos de administrador.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**PLATAFORMA NO ADMINISTRADA DE TIPO MPSIGUPDATE \_ \_ \_**</dt> </dl> | Actualización de MU/WU para PLATFORM. Cancelar requiere derechos de administrador.<br/> |



 

</dd> <dt>

**Fase**
</dt> <dd>

Tipo: **FASE DE ACTUALIZACIÓN DE \_ \_ MP**

</dd> <dd>

Fase de actualización. Uno de los siguientes valores posibles:



| Valor                                                                                                                                                                         | Significado                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**FASE \_ DE MP \_ DESCONOCIDA**</dt> </dl>       | Fase de actualización desconocida.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**ACTUALIZACIÓN \_ DE LA BÚSQUEDA DE \_ MP**</dt> </dl>       | Actualizar la fase de búsqueda.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**ACTUALIZACIÓN \_ DE DESCARGA DE \_ MP**</dt> </dl> | Actualizar la fase de descarga.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**ACTUALIZACIÓN \_ DE INSTALACIÓN DE \_ MP**</dt> </dl>    | Actualizar la fase de instalación.<br/>  |



 

</dd> <dt>

**Ruta de acceso**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Actualizar ruta de acceso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





