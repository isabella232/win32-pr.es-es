---
title: Estructura de WINBIO_BIR_HEADER (Winbio \_ Types. h)
description: Contiene el encabezado de un registro de información biométrica (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- Plataforma de biometría de Windows API de WINBIO_BIR_HEADER Structure
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150292"
---
# <a name="winbio_bir_header-structure"></a>WINBIO \_ \_ estructura de encabezado Bir

La estructura del **\_ \_ encabezado WINBIO Bir** contiene el encabezado de un registro de información biométrica (BIR).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ValidFields**
</dt> <dd>

Máscara de máscara que especifica los campos de esta estructura válidos. Para obtener más información, [**consulte \_ \_ constantes de campo WINBIO Bir**](winbio-bir-field-constants.md).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Una constante de la **\_ \_ versión de WINBIO Bir** que especifica la versión del encabezado. Los números de versión son valores de 8 bits en los que los cuatro bits superiores especifican el número principal y los cuatro bits inferiores especifican el número de versión secundaria. Actualmente, esta debe ser WINBIO \_ CBEFF \_ Header \_ version (0x11).

</dd> <dt>

**PatronHeaderVersion**
</dt> <dd>

Una constante de la **\_ \_ versión de WINBIO Bir** que especifica la versión del encabezado. Los números de versión son valores de 8 bits en los que los cuatro bits superiores especifican el número principal y los cuatro bits inferiores especifican el número de versión secundaria. Actualmente, este debe ser WINBIO de la versión de encabezado de un \_ patrocinador \_ \_ (0x11).

</dd> <dt>

**Marcadores de la**
</dt> <dd>

Valor que especifica el formato de los datos de encabezado. Puede ser **una operación OR bit a bit** de las siguientes marcas de nivel de procesamiento y de seguridad. Para obtener más información, vea [**WINBIO \_ Bir \_ Data \_ Flags constantes**](winbio-bir-data-flags-constants.md).



| Value                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ Privacidad de marca de datos**</dt> <dt>((UCHAR) 0x02)</dt> </dl>                                       | Los datos se cifran.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Integridad**</dt> de la marca de datos <dt>((UCHAR) 0x01)</dt> </dl>                                 | Los datos están firmados digitalmente o protegidos por un código de autenticación de mensajes (MAC).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ firmada**</dt> <dt>((UCHAR) 0x04)</dt> </dl>                                          | Si se establece esta marca y la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , los datos se firman. Si no se establece esta marca pero se establece la marca de integridad de la **\_ marca de datos \_ \_ WINBIO** , se calcula un equipo Mac a través de los datos.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ sin formato**</dt> <dt>((UCHAR) 0x20)</dt> </dl>                                                   | Los datos están en el formato con el que se capturaron.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ intermedia**</dt> <dt>((UCHAR) 0x40)</dt> </dl>                        | Los datos no son sin procesar, pero no se han procesado completamente.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ Marca de datos \_ \_ procesada**</dt> <dt>((UCHAR) 0x80)</dt> </dl>                                 | Se han procesado los datos.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Máscara de opción de marca de datos \_ \_ \_ \_ presente**</dt> <dt>((UCHAR) 0x08)</dt> </dl> | Este valor siempre es 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Tipo**
</dt> <dd>

Un \_ \_ valor de tipo biométrico WINBIO que especifica el tipo de datos biométricos a los que se hace referencia en el registro de información biométrico. Actualmente solo se admite la **\_ \_ huella digital de tipo WINBIO** . Para obtener más información, [**vea \_ constantes de \_ tipo biométrico WINBIO**](winbio-biometric-type-constants.md).

</dd> <dt>

**Subtype**
</dt> <dd>

Valor **de \_ \_ subtipo biométrico WINBIO** que especifica el subfactor asociado a los datos biométricos. Para obtener más información, vea comentarios y [**WINBIO las \_ constantes de \_ subtipo biométrico**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Propósito**
</dt> <dd>

Una máscara de **\_ \_ propósito de WINBIO Bir** que especifica el uso previsto de los datos. Puede ser **una operación OR bit a bit** de los valores siguientes. Para obtener más información, consulte [**WINBIO \_ Bir \_ purpose Constant**](winbio-bir-purpose-constants.md).

-   \_comprobación de propósito de WINBIO \_
-   \_identificación de propósito de WINBIO \_
-   \_inscripción de propósito de WINBIO \_
-   WINBIO \_ propósito \_ inscribirse \_ para la \_ comprobación
-   WINBIO \_ propósito \_ inscribirse \_ para \_ identificación
-   \_Auditoría de propósito de WINBIO \_

</dd> <dt>

**Calidad de los**
</dt> <dd>

Valor que especifica la calidad relativa de los datos biométricos en el registro de información biométrica (BIR). Puede ser un entero comprendido entre 0 y 100 o uno de los valores siguientes. Para obtener más información, vea [**WINBIO \_ Bir \_ Quality constantes**](winbio-bir-quality-constants.md).



| Value                                                                                                                                                                                                                                                                                                        | Significado                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ Calidad de datos \_ \_ no \_ establecida**</dt> <dt>((WINBIO \_ Bir \_ Quality)-1)</dt> </dl>                   | El creador de BIR admite las medidas de calidad, pero no se establece ningún valor en BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Calidad de datos \_ \_ no \_ admitida**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt> </dl> | El creador de BIR no admite las medidas de calidad.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

Fecha y hora, en hora universal coordinada (hora del meridiano de Greenwich), a la que se creó el BIR.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Período para el que el BIR es válido.

<dl> <dt>

**BeginDate**
</dt> <dd>

Fecha y hora, en hora universal coordinada, a la que comienza el período de validez.

</dd> <dt>

**EndDate**
</dt> <dd>

Fecha y hora, en hora universal coordinada, a la que el BIR deja de ser válido.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Estructura [**de \_ \_ formato registrada WINBIO**](winbio-registered-format.md) que especifica el formato de datos del bloque de datos estándar en la estructura [**\_ Bir de WINBIO**](winbio-bir.md) . Los miembros de **\_ \_ formato registrados WINBIO** no pueden ser cero. Puede utilizar las siguientes constantes para simplificar la comprobación de errores.



| Value                                                                                                                                                                                                                                                                                      | Significado                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ NO hay ningún \_ propietario de formato \_ \_ disponible**</dt> <dt>((USHORT) 0)</dt> </dl> | No se ha especificado ningún valor de propietario asignado IBIA (Asociación del sector biométrico internacional).<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ NO hay ningún \_ tipo de formato \_ \_ disponible**</dt> <dt>((USHORT) 0)</dt> </dl>    | No se ha especificado ningún tipo de formato.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Estructura [**de \_ \_ formato registrada en WINBIO**](winbio-registered-format.md) que especifica el identificador de producto del componente que generó el bloque de datos estándar en el Bir. Los miembros de **\_ \_ formato registrados WINBIO** pueden ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El parámetro *SubType* especifica el subfactor asociado a los datos biométricos. Actualmente, el Plataforma de biometría de Windows (WBF) solo admite la captura de huellas digitales y usa las siguientes constantes para representar información de subtipos:

-   WINBIO \_ ANSI \_ 381 \_ pos \_ desconocido
-   \_Thumb WINBIO ANSI \_ 381 \_ pos \_ RH \_
-   \_Dedo de \_ \_ \_ \_ índice RH \_ de WINBIO ANSI 381 pos
-   \_Dedo central de WINBIO ANSI \_ 381 \_ pos \_ dcha \_ \_
-   \_Dedo de \_ \_ \_ \_ anillo RH \_ de WINBIO ANSI 381 pos
-   \_ \_ \_ \_ \_ Pequeño \_ dedo de WINBIO ANSI 381 pos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Thumb
-   WINBIO \_ de \_ Índice de LH de pdv ANSI 381 \_ pos \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ central \_
-   WINBIO \_ el \_ \_ dedo de \_ anillo de LH ANSI 381 pos \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ cuatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ cuatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ dos \_ Thumbs

> [!IMPORTANT]
>
> No intente validar el valor proporcionado para el valor del parámetro de *subtipo* . El servicio biométrico de Windows validará el valor proporcionado antes de pasarlo a su implementación. Si el valor es **WINBIO \_ SubType \_ no \_ Information** o **WINBIO \_ SubType \_ any**, valide cuando sea necesario.

 

Si se declara alguno de los bits siguientes, la estructura **del \_ \_ encabezado WINBIO Bir** no tiene el formato correcto.


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



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

[**WINBIO \_ constantes de \_ subtipo de biométrico**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_Constantes de \_ marcadores de datos de WINBIO Bir \_**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**WINBIO \_ \_ constantes de campo Bir**](winbio-bir-field-constants.md)
</dt> <dt>

[**\_Constantes WINBIO Bir \_ purpose**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**Constantes de calidad de WINBIO \_ Bir \_**](winbio-bir-quality-constants.md)
</dt> <dt>

[**Constantes de versión de WINBIO \_ Bir \_**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





