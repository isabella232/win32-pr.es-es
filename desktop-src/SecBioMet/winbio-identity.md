---
title: WINBIO_IDENTITY estructura (Winbio \_ types.h)
description: Contiene un valor de identificación asociado a una plantilla biométrica.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY estructura Windows API de Marco biométrico
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476528"
---
# <a name="winbio_identity-structure"></a>Estructura DE \_ WINBIO IDENTITY

La **estructura WINBIO \_ IDENTITY** contiene un valor de identificación asociado a una plantilla biométrica.

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



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Especifica el formato de la información de identidad contenida en esta estructura. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                                         | Significado                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**TIPO DE IDENTIFICADOR DE WINBIO \_ \_ \_ NULL**</dt> </dl>             | La plantilla no tiene ningún identificador asociado.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**CARÁCTER COMODÍN \_ DEL TIPO DE IDENTIFICADOR \_ DE WINBIO \_**</dt> </dl> | La estructura coincide con todas las identidades de plantilla.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**GUID DE TIPO \_ DE IDENTIFICADOR \_ \_ DE WINBIO**</dt> </dl>             | La estructura contiene un GUID asociado a la plantilla.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**SID DE \_ TIPO \_ DE IDENTIFICADOR \_ DE WINBIO**</dt> </dl>                | La estructura contiene el SID de cuenta asociado a la plantilla.<br/> |



 

</dd> <dt>

**Valor**
</dt> <dd>

Una unión que puede contener uno de los valores siguientes:

<dl> <dt>

**Null**
</dt> <dd>

Contiene 1 si el miembro **Type** es **WINBIO \_ ID TYPE \_ \_ NULL**.

</dd> <dt>

**Comodín**
</dt> <dd>

Contiene 1 si el miembro **Type** es **WINBIO \_ ID TYPE \_ \_ WILDCARD**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contiene un valor GUID de 128 bits que identifica la plantilla si el miembro **Type** es **WINBIO \_ ID TYPE \_ \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Estructura que contiene un SID de cuenta si el **miembro Type** es **WINBIO ID TYPE \_ \_ \_ SID**.

<dl> <dt>

**Tamaño**
</dt> <dd>

Número de caracteres del SID.

</dd> <dt>

**Data**
</dt> <dd>

Matriz de caracteres sin signo que contienen el SID. El tamaño máximo actual de la matriz es de 68 caracteres.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa en las funciones siguientes:

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
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> </dl>

 

 





