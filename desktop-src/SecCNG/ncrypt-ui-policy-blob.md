---
description: Se usa con la \_ \_ \_ propiedad de la propiedad de directiva de interfaz de usuario NCRYPT para contener información de la interfaz de usuario para una clave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Estructura de NCRYPT_UI_POLICY_BLOB (ncrypt \_ Provider. h)
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
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544995"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>\_Estructura de \_ BLOB de directiva de interfaz de usuario NCRYPT \_

La estructura de **\_ \_ \_ blobs** de la Directiva de la interfaz de usuario de ncrypt se usa con la propiedad de la propiedad de directiva de interfaz de usuario ncrypt para contener información de la interfaz de usuario [**\_ \_ \_**](key-storage-property-identifiers.md)

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
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ \_Marca de \_ clave \_ de protección de IU**</dt> <dt>0x00000001</dt> </dl>                                | Muestre la interfaz de usuario de clave segura según sea necesario.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ Marca de IU \_ forzada de \_ alta \_ protección \_**</dt> <dt>0x00000002</dt> </dl> | Forzar la alta protección.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

La longitud, en bytes, del título de creación. El título de creación es una cadena Unicode terminada en null que especifica el texto que se utiliza como título del cuadro de diálogo clave segura cuando se completa la clave. El título de creación debe colocarse inmediatamente después de la estructura de BLOB de la **Directiva de interfaz de usuario de NCRYPT \_ \_ \_** . Si el valor del miembro **cbCreationTitle** se establece en 0, se usa un título de creación predeterminado para el título del cuadro de diálogo clave segura. Este miembro solo se usa en la finalización de la clave.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

Longitud, en bytes, del nombre descriptivo de la clave. El nombre descriptivo es una cadena Unicode terminada en null que contiene el texto que se muestra en el cuadro de diálogo clave segura como el nombre de la clave. El nombre descriptivo debe colocarse inmediatamente después del título de creación en este BLOB. Si el valor del miembro **cbFriendlyName** se establece en 0, se usa un nombre predeterminado en el cuadro de diálogo clave segura. Este miembro se usa cuando se completa la clave y cuando se usa la clave.

</dd> <dt>

**cbDescription**
</dt> <dd>

La longitud, en bytes, de la descripción de la clave. La descripción de la clave es una cadena Unicode terminada en null que contiene el texto que se muestra en el cuadro de diálogo clave segura como la descripción de la clave. El valor de descripción debe colocarse inmediatamente después del nombre descriptivo de este BLOB. Si el valor del miembro **cbDescription** se establece en 0, se usa una descripción predeterminada en el cuadro de diálogo clave segura. Este miembro se usa cuando se completa la clave y cuando se usa la clave.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se incluye en el \_ encabezado del proveedor ncrypt. h. Para usar la estructura, debe descargar el [Kit de desarrollo de proveedores de servicios criptográficos](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) de Microsoft Connect.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                          |
| Encabezado<br/>                   | <dl> <dt>Ncrypt \_ Provider. h</dt> </dl> |



 

