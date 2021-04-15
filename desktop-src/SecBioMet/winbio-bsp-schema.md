---
title: Estructura de WINBIO_BSP_SCHEMA (Winbio \_ Types. h)
description: Describe las capacidades de un proveedor de servicios biométricos.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- Plataforma de biometría de Windows API de WINBIO_BSP_SCHEMA Structure
- PWINBIO_BSP_SCHEMA de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490768"
---
# <a name="winbio_bsp_schema-structure"></a>\_Estructura de esquema BSP de WINBIO \_

La estructura de **\_ \_ esquema BSP de WINBIO** describe las capacidades de un proveedor de servicios biométricos. La función [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) usa esta estructura.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Tipo de medida biométrica usada por este dispositivo. Actualmente, este debe ser **WINBIO \_ tipo de \_ huella digital**.

</dd> <dt>

**BspId**
</dt> <dd>

Valor que identifica de forma única este componente de proveedor de servicios biométricos.

</dd> <dt>

**Descripción**
</dt> <dd>

Una cadena Unicode terminada en **null** que contiene una descripción del proveedor de servicios biométricos.

</dd> <dt>

**Proveedor**
</dt> <dd>

Una cadena Unicode terminada en **null** que contiene el nombre del proveedor que proporciona el proveedor de servicios biométricos.

</dd> <dt>

**Versión**
</dt> <dd>

Una estructura de [**\_ versión de WINBIO**](winbio-version.md) que contiene la versión de software del componente de proveedor de servicios biométricos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





