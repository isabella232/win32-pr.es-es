---
title: WINBIO_UNIT_SCHEMA estructura (Winbio \_ types.h)
description: Describe las funcionalidades de una unidad biométrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA estructura Windows API de Marco biométrico
- PWINBIO_UNIT_SCHEMA puntero de estructura Windows API de Marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae91ae5353aa0e9c02414e90a8364d86bdc56c0cdcc4f4586656f28f92f100ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909174"
---
# <a name="winbio_unit_schema-structure"></a>Estructura DE \_ ESQUEMA DE UNIDAD \_ WINBIO

La **estructura DE ESQUEMA DE UNIDAD \_ \_ WINBIO** describe las funcionalidades de una unidad biométrica. Lo usa la [**función WinBioEnumBiometricUnits.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**UnitId**
</dt> <dd>

Valor que identifica la unidad biométrica.

</dd> <dt>

**PoolType**
</dt> <dd>

Valor **ULONG** que especifica el tipo de la unidad biométrica. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                            | Significado                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**GRUPO WINBIO \_ \_ DESCONOCIDO**</dt> </dl> | Se desconoce el tipo.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**SISTEMA DE \_ GRUPO WINBIO \_**</dt> </dl>    | La sesión se conecta a una colección compartida de unidades biométricas administradas por el proveedor de servicios.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ POOL \_ PRIVATE**</dt> </dl> | La sesión se conecta a una colección de unidades biométricas administradas por el autor de la llamada.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Valor que especifica el tipo de la unidad biométrica. Actualmente **solo se admite \_ WINBIO TYPE \_ FINGERPRINT.**

</dd> <dt>

**SensorSubType**
</dt> <dd>

Subtipo de sensor definido para el tipo biométrico especificado por el **miembro BiometricFactor.** Actualmente solo se admiten los tipos de huella digital **\_ \_ (WINBIO TYPE FINGERPRINT).** Los subtipos siguientes están definidos actualmente para las huellas digitales:

-   SUBTIPO DE SENSOR WINBIO \_ \_ \_ DESCONOCIDO
-   DESLIZAR RÁPIDAMENTE \_ EL \_ SUBTIPO DEL SENSOR FP \_ DE \_ WINBIO
-   WINBIO \_ FP \_ SENSOR \_ SUBTYPE \_ TOUCH

</dd> <dt>

**Capabilities**
</dt> <dd>

Máscara de bits de las funcionalidades del sensor biométrico. Puede ser un OR bit a bit **de** los valores siguientes:

-   SENSOR DE \_ FUNCIONALIDAD WINBIO \_
-   COINCIDENCIA DE \_ FUNCIONALIDAD DE \_ WINBIO
-   BASE DE DATOS \_ DE FUNCIONALIDAD DE \_ WINBIO
-   PROCESAMIENTO DE \_ FUNCIONALIDAD DE \_ WINBIO
-   CIFRADO DE \_ FUNCIONALIDAD WINBIO \_
-   NAVEGACIÓN POR \_ LA FUNCIONALIDAD \_ WINBIO
-   INDICADOR DE \_ FUNCIONALIDAD DE \_ WINBIO
-   SENSOR VIRTUAL \_ DE FUNCIONALIDAD \_ WINBIO \_
    > [!Note]  
    > La **constante \_ WINBIO CAPABILITY \_ VIRTUAL SENSOR \_ solo** se aplica Windows 10 y versiones posteriores.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Valor de cadena que contiene el identificador del dispositivo. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **NULL de** terminación.

</dd> <dt>

**Descripción**
</dt> <dd>

Valor de cadena que contiene una descripción de la unidad biométrica. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **NULL de** terminación.

</dd> <dt>

**Fabricante**
</dt> <dd>

Valor de cadena que contiene el nombre del fabricante. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **NULL de** terminación.

</dd> <dt>

**Modelo**
</dt> <dd>

Valor de cadena que contiene el número de modelo de la unidad biométrica. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **NULL de** terminación.

</dd> <dt>

**SerialNumber**
</dt> <dd>

Cadena Unicode terminada en **NULL** que contiene el número de serie de la unidad biométrica. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **NULL de** terminación.

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Estructura [**DE VERSIÓN \_ DE WINBIO**](winbio-version.md) que contiene los números de versión principal y secundaria de la unidad biométrica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





