---
title: WINBIO_BSP_SCHEMA estructura (Winbio \_ types.h)
description: Describe las funcionalidades de un proveedor de servicios biométricos.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA estructura Windows API de Marco biométrico
- PWINBIO_BSP_SCHEMA puntero de estructura Windows BIOMETRIC Framework API
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160781"
---
# <a name="winbio_bsp_schema-structure"></a>Estructura DE \_ ESQUEMA BSP de WINBIO \_

La **estructura DEL ESQUEMA \_ BSP \_ de WINBIO** describe las funcionalidades de un proveedor de servicios biométricos. La función [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) usa esta estructura.

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



## <a name="members"></a>Members

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Tipo de medida biométrica usada por este dispositivo. Actualmente, debe ser **WINBIO \_ TYPE \_ FINGERPRINT**.

</dd> <dt>

**BspId**
</dt> <dd>

Valor que identifica de forma única este componente del proveedor de servicios biométricos.

</dd> <dt>

**Descripción**
</dt> <dd>

Cadena Unicode terminada en **NULL** que contiene una descripción del proveedor de servicios biométricos.

</dd> <dt>

**Proveedor**
</dt> <dd>

Cadena Unicode terminada en **NULL** que contiene el nombre del proveedor que proporciona el proveedor de servicios biométricos.

</dd> <dt>

**Versión**
</dt> <dd>

Una [**estructura VERSION \_ de WINBIO**](winbio-version.md) contiene la versión de software del componente del proveedor de servicios biométricos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





