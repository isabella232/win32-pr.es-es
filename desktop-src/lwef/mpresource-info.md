---
title: MPRESOURCE_INFO estructura (MpClient.h)
description: Estructura de información de recursos.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO estructura heredada de Windows environment
- PMPRESOURCE_INFO puntero de estructura heredado Windows características del entorno
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170206"
---
# <a name="mpresource_info-structure"></a>Estructura DE \_ INFORMACIÓN DE MPRESOURCE

Estructura de información de recursos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Scheme**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Identificador del esquema de recursos, como "file" o "dir".

</dd> <dt>

**Path**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Ruta de acceso absoluta del recurso, en función del **esquema**.

</dd> <dt>

**Clase**
</dt> <dd>

Tipo: **MPRESOURCE \_ (CLASE)**

</dd> <dd>

Este campo se establece cuando el recurso se identifica como parte de la amenaza. Especifica la clase de recurso, principalmente concreta frente a latente. Puede ser una combinación de estos valores posibles:



| Value                                                                                                                                                                                                                                                                        | Significado                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ CLASE \_ DE RECURSO \_ UNKNOWN**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS \_ CONCRETE**</dt> <dt>0x0001</dt> </dl>           | Mutuamente excluyente con **MP \_ RESOURCE CLASS \_ \_ LATENT**.<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS \_ LATENT**</dt> <dt>0x0002</dt> </dl>                 | Mutuamente excluyente con **MP \_ RESOURCE CLASS \_ \_ CONCRETE**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ ARCHIVO \_ DE EJEMPLO DE CLASE \_ \_ DE**</dt> <dt>RECURSO 0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS \_ SHARED**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





