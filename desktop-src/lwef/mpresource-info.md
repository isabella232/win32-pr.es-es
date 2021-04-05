---
title: MPRESOURCE_INFO estructura (MpClient. h)
description: Estructura de información de recursos.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPRESOURCE_INFO características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996660"
---
# <a name="mpresource_info-structure"></a>Estructura de información de MPRESOURCE \_

Estructura de información de recursos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Regímenes**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Identificador del esquema de recursos como "File" o "dir".

</dd> <dt>

**Ruta de acceso**
</dt> <dd>

Type: **MP \_ MIDL \_ String LPWStr**

</dd> <dd>

Ruta de acceso absoluta del recurso, basándose en el **esquema**.

</dd> <dt>

**Clase**
</dt> <dd>

Type: **\_ clase MPRESOURCE**

</dd> <dd>

Este campo se establece cuando el recurso se identifica como parte de la amenaza. Especifica la clase de recurso, principalmente concreta frente a latente. Puede ser una combinación de estos valores posibles:



| Value                                                                                                                                                                                                                                                                        | Significado                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**Módulo de administración \_ Clase de recursos \_ \_ desconocida**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**Módulo de administración \_ Clase de recurso 0x0001 \_ \_ concreta**</dt> <dt></dt> </dl>           | Es mutuamente excluyente con la **clase de recursos del módulo de administración \_ \_ \_ latente**.<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**Módulo de administración \_ Clase de recurso \_ \_ lated**</dt> <dt>0x0002</dt> </dl>                 | Es mutuamente excluyente con la **clase de recursos del módulo de administración \_ \_ \_ concreta**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**Módulo de administración \_ \_Archivo de \_ ejemplo \_ de clase de recursos**</dt> <dt>0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**Módulo de administración \_ 0x0100 \_ \_ compartido de clase de recurso**</dt> <dt></dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





