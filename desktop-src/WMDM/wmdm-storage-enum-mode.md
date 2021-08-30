---
title: WMDM_STORAGE_ENUM_MODE enumeración
description: El tipo de enumeración WMDM STORAGE ENUM MODE define cómo se enumerará el \_ \_ contenido del \_ almacenamiento. IWMDMStorage3 SetEnumPreference usa esta enumeración.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE enumeración windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8b524618ebc0c5d40f9f4e9f0ad0871b7c8c39a0919d594a39248bc2d6dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004775"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>Enumeración \_ WMDM STORAGE \_ ENUM \_ MODE

El **tipo de \_ enumeración WMDM STORAGE \_ ENUM \_ MODE** define cómo se enumerará el contenido del almacenamiento. [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)usa esta enumeración.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**MODO ENUM \_ \_ RAW**
</dt> <dd>

Enumera el contenido del almacenamiento tal como se organiza en el sistema de archivos del almacenamiento.

**ENUM \_ MODE \_ USE \_ DEVICE \_ PREF**

Enumera el contenido del almacenamiento en función de la preferencia del dispositivo, tal como se indica en el parámetro de dispositivo *UseMetadataViews.*

**VISTAS DE \_ METADATOS DEL MODO \_ ENUM \_**

Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM \_ MODE \_ USE \_ DEVICE \_ PREF**
</dt> <dd>

Enumera el contenido del almacenamiento en función de la preferencia del dispositivo, tal como se indica en el parámetro de dispositivo *UseMetadataViews.*

**VISTAS DE \_ METADATOS DEL MODO \_ ENUM \_**

Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**VISTAS DE \_ METADATOS DEL MODO \_ ENUM \_**
</dt> <dd>

Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





