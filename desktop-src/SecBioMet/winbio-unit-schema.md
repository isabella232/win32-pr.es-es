---
title: Estructura de WINBIO_UNIT_SCHEMA (Winbio \_ Types. h)
description: Describe las capacidades de una unidad biométrica.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- Plataforma de biometría de Windows API de WINBIO_UNIT_SCHEMA Structure
- PWINBIO_UNIT_SCHEMA de puntero de estructura Plataforma de biometría de Windows API
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
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997079"
---
# <a name="winbio_unit_schema-structure"></a>Estructura de esquema de \_ unidad WINBIO \_

La estructura de **\_ \_ esquema de unidad WINBIO** describe las capacidades de una unidad biométrica. Lo utiliza la función [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .

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

Valor **ULong** que especifica el tipo de la unidad biométrica. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                            | Significado                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**Grupo de WINBIO \_ \_ desconocido**</dt> </dl> | Se desconoce el tipo.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_sistema de grupo de WINBIO \_**</dt> </dl>    | La sesión se conecta a una colección compartida de unidades biométricas administradas por el proveedor de servicios.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**Grupo de WINBIO \_ \_ privado**</dt> </dl> | La sesión se conecta a una colección de unidades biométricas administradas por el autor de la llamada.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Valor que especifica el tipo de unidad biométrica. Actualmente solo se admite la **\_ \_ huella digital de tipo WINBIO** .

</dd> <dt>

**SensorSubType**
</dt> <dd>

Un subtipo de sensor definido para el tipo biométrico especificado por el miembro **BiometricFactor** . Actualmente solo se admiten los tipos de huellas digitales (WINBIO de tipo de huella **\_ \_ digital**). Los siguientes subtipos están definidos actualmente para huellas digitales:

-   subtipo de sensor de WINBIO \_ \_ \_ desconocido
-   WINBIO \_ de \_ subtipo de sensor FP \_ \_
-   \_toque de \_ subtipo de sensor FP \_ \_ de WINBIO

</dd> <dt>

**Capabilities**
</dt> <dd>

Una máscara de la funcionalidad del sensor biométrico. Puede ser **una operación OR bit a bit** de los siguientes valores:

-   \_sensor de capacidad de WINBIO \_
-   coincidencia de la \_ funcionalidad WINBIO \_
-   base de datos de \_ capacidad WINBIO \_
-   procesamiento de la capacidad de WINBIO \_ \_
-   \_cifrado de capacidad de WINBIO \_
-   navegación por la \_ funcionalidad WINBIO \_
-   \_indicador de capacidad de WINBIO \_
-   \_ \_ sensor virtual de capacidad de WINBIO \_
    > [!Note]  
    > La constante del **\_ \_ \_ sensor virtual de la funcionalidad WINBIO** solo se aplica a Windows 10 y versiones posteriores.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Valor de cadena que contiene el identificador del dispositivo. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.

</dd> <dt>

**Descripción**
</dt> <dd>

Valor de cadena que contiene una descripción de la unidad biométrica. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.

</dd> <dt>

**Le**
</dt> <dd>

Valor de cadena que contiene el nombre del fabricante. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.

</dd> <dt>

**Modelo**
</dt> <dd>

Valor de cadena que contiene el número de modelo de la unidad biométrica. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.

</dd> <dt>

**SerialNumber**
</dt> <dd>

Una cadena Unicode terminada en **null** que contiene el número de serie de la unidad biométrica. La cadena puede contener hasta 256 caracteres Unicode, incluido un carácter **nulo** de terminación.

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Una estructura de [**\_ versión de WINBIO**](winbio-version.md) que contiene los números de versión principal y secundaria para la unidad biométrica.

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

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





