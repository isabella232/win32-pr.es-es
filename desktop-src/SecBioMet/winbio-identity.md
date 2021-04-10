---
title: Estructura de WINBIO_IDENTITY (Winbio \_ Types. h)
description: Contiene un valor de identificación asociado a una plantilla biométrica.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- Plataforma de biometría de Windows API de WINBIO_IDENTITY Structure
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150391"
---
# <a name="winbio_identity-structure"></a>Estructura de identidad de WINBIO \_

La estructura de **\_ identidad de WINBIO** contiene un valor de identificación asociado a una plantilla de biométrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Especifica el formato de la información de identidad incluida en esta estructura. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                                         | Significado                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**WINBIO \_ ID \_ Type \_ null**</dt> </dl>             | La plantilla no tiene ningún identificador asociado.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ carácter comodín de tipo de identificador WINBIO \_**</dt> </dl> | La estructura coincide con todas las identidades de plantilla.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_GUID de \_ tipo de identificador WINBIO \_**</dt> </dl>             | La estructura contiene un GUID asociado a la plantilla.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**identificador de WINBIO de \_ tipo ID. \_ \_**</dt> </dl>                | La estructura contiene el SID de la cuenta asociado a la plantilla.<br/> |



 

</dd> <dt>

**Valor**
</dt> <dd>

Unión que puede contener uno de los valores siguientes:

<dl> <dt>

**Null**
</dt> <dd>

Contiene 1 si el miembro de **tipo** es **WINBIO \_ ID \_ Type \_ null**.

</dd> <dt>

**Wildcard (Carácter comodín)**
</dt> <dd>

Contiene 1 si el miembro de **tipo** es **WINBIO \_ con el tipo de identificador \_ \_ comodín**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contiene un valor GUID de 128 bits que identifica la plantilla si el miembro de **tipo** es el **\_ identificador \_ \_ GUID de tipo WINBIO**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Una estructura que contiene un SID de cuenta si el miembro de **tipo** es el **tipo de \_ identificador WINBIO \_ \_ SID**.

<dl> <dt>

**Tamaño**
</dt> <dd>

Número de caracteres del SID.

</dd> <dt>

**Data**
</dt> <dd>

Matriz de caracteres sin signo que contiene el SID. El tamaño máximo actual de la matriz es de 68 caracteres.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa en las siguientes funciones:

-   [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> </dl>

 

 





