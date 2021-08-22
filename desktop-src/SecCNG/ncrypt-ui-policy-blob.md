---
description: Se usa con la propiedad \_ NCRYPT UI \_ POLICY PROPERTY para contener información de interfaz de usuario para una \_ clave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: NCRYPT_UI_POLICY_BLOB estructura (Ncrypt \_ provider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: 21f9f6c0f6956ffa89da45c9dcd23727c0b3cea2d4f31131713f9ed5a0c3a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907605"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>Estructura blob de \_ directiva de interfaz de usuario \_ \_ de NCRYPT

La estructura blob de directiva de interfaz de usuario NCRYPT se usa con la propiedad [**NCRYPT \_ UI POLICY \_ \_ PROPERTY**](key-storage-property-identifiers.md) para contener información de interfaz de usuario para una clave. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Número de versión de la estructura. Este miembro debe contener 1.

</dd> <dt>

**dwFlags**
</dt> <dd>

Conjunto de marcas que proporcionan información o requisitos adicionales de la interfaz de usuario.



| Value                                                                                                                                                                                                                                                                                                  | Significado                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ Ui \_ PROTECT KEY FLAG \_ \_ 0x00000001**</dt> <dt></dt> </dl>                                | Muestre la interfaz de usuario de clave segura según sea necesario.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ UI \_ FORCE HIGH PROTECTION FLAG \_ \_ \_ 0x00000002**</dt> <dt></dt> </dl> | Fuerce la alta protección.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

Longitud, en bytes, del título de creación. El título de creación es una cadena Unicode terminada en null que especifica el texto que se usa como título del cuadro de diálogo de clave segura cuando se completa la clave. El título de creación debe colocarse inmediatamente después de la estructura blob de directiva de interfaz de **\_ usuario \_ de \_ NCRYPT.** Si el valor del miembro **cbCreationTitle** se establece en 0, se usa un título de creación predeterminado para el título del cuadro de diálogo de clave segura. Este miembro solo se usa en la finalización de claves.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

Longitud, en bytes, del nombre descriptivo de la clave. El nombre descriptivo es una cadena Unicode terminada en null que contiene el texto que se muestra en el cuadro de diálogo de clave segura como nombre de la clave. El nombre descriptivo debe colocarse inmediatamente después del título de creación en este BLOB. Si el valor del miembro **cbFriendlyName** se establece en 0, se usa un nombre predeterminado en el cuadro de diálogo de clave segura. Este miembro se usa tanto cuando se completa la clave como cuando se usa la clave.

</dd> <dt>

**cbDescription**
</dt> <dd>

Longitud, en bytes, de la descripción de la clave. La descripción de la clave es una cadena Unicode terminada en null que contiene el texto que se muestra en el cuadro de diálogo de clave segura como la descripción de la clave. El valor de descripción debe colocarse inmediatamente después del nombre descriptivo de este BLOB. Si el valor del miembro **cbDescription** se establece en 0, se usa una descripción predeterminada en el cuadro de diálogo de clave segura. Este miembro se usa tanto cuando se completa la clave como cuando se usa la clave.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se incluye en el encabezado \_ provider.h de Ncrypt. Para usar la estructura , debe descargar el [Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) de desarrollo del proveedor de servicios criptográficos de Microsoft Conectar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                          |
| Header<br/>                   | <dl> <dt>Ncrypt \_ provider.h</dt> </dl> |



 

