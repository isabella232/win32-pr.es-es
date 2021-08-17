---
title: WINBIO_BIR_HEADER estructura (Winbio \_ types.h)
description: Contiene el encabezado de un registro de información biométrica (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER estructura Windows API de Marco biométrico
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
ms.openlocfilehash: d2166a206dd1590f83e16bc67482d3b42e24717efae4c44e54a99b9aa7d83b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911088"
---
# <a name="winbio_bir_header-structure"></a>Estructura DE ENCABEZADO \_ DE WINBIO BIR \_

La **estructura WINBIO \_ BIR \_ HEADER** contiene el encabezado de un registro de información biométrica (BIR).

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

Máscara de bits que especifica qué campos de esta estructura son válidos. Para obtener más información, [**vea WINBIO \_ BIR FIELD \_ Constants**](winbio-bir-field-constants.md).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Constante **WINBIO \_ BIR \_ VERSION** que especifica la versión del encabezado. Los números de versión son valores de 8 bits donde los cuatro bits superiores especifican el número principal y los cuatro bits inferiores especifican el número de versión secundaria. Actualmente, debe ser WINBIO \_ CBEFF \_ HEADER \_ VERSION (versión 0x11).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Constante **WINBIO \_ BIR \_ VERSION** que especifica la versión del encabezado. Los números de versión son valores de 8 bits donde los cuatro bits superiores especifican el número principal y los cuatro bits inferiores especifican el número de versión secundaria. En la actualidad, debe ser WINBIO \_ VERSION DEL ENCABEZADO DE WINBIO \_ \_ (0x11).

</dd> <dt>

**DataFlags**
</dt> <dd>

Valor que especifica el formato de los datos de encabezado. Puede ser un OR bit a bit **de** las siguientes marcas de nivel de procesamiento y seguridad. Para obtener más información, [**vea WINBIO \_ BIR DATA \_ \_ FLAGS Constants**](winbio-bir-data-flags-constants.md)(Constantes de MARCAS DE DATOS DE WINBIO BIR).



| Value                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ PRIVACIDAD \_ DE \_ LA MARCA**</dt> DE DATOS <dt>((UCHAR)0x02)</dt> </dl>                                       | Los datos se cifran.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ INTEGRIDAD \_ DE \_ LA MARCA**</dt> DE DATOS <dt>((UCHAR)0x01)</dt> </dl>                                 | Los datos están firmados digitalmente o protegidos por un código de autenticación de mensajes (MAC).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ MARCA \_ DE \_ DATOS FIRMADA**</dt> <dt>((UCHAR)0x04)</dt> </dl>                                          | Si se establecen esta marca y la marca INTEGRIDAD DE LA MARCA DE DATOS **\_ \_ \_ WINBIO,** los datos se firman. Si esta marca no está establecida pero la marca INTEGRIDAD DE LA MARCA DE DATOS WINBIO está establecida, se calcula un MAC a través de los datos. **\_ \_ \_**<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ RAW**</dt> <dt>((UCHAR)0x20)</dt> </dl>                                                   | Los datos tienen el formato con el que se capturaron.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ MARCA \_ DE \_ DATOS INTERMEDIA**</dt> <dt>((UCHAR)0x40)</dt> </dl>                        | Los datos no son sin procesar, pero no se han procesado por completo.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ MARCA \_ DE \_ DATOS PROCESADA**</dt> <dt>((UCHAR)0x80)</dt> </dl>                                 | Los datos se han procesado.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ MÁSCARA \_ DE OPCIÓN DE MARCA DE \_ \_ \_ DATOS**</dt> <dt>PRESENTE ((UCHAR)0x08)</dt> </dl> | Este valor siempre es 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Type**
</dt> <dd>

Valor DE TIPO BIOMÉTRICO DE WINBIO que especifica el tipo de datos biométricos a los que se hace referencia \_ en el registro de información \_ biométrica. Actualmente solo **se admite WINBIO \_ TYPE \_ FINGERPRINT.** Para obtener más información, [**vea WINBIO \_ BIOMETRIC \_ TYPE Constants**](winbio-biometric-type-constants.md).

</dd> <dt>

**Subtipo**
</dt> <dd>

Valor **DE \_ \_ SUBTIPO BIOMÉTRICO DE WINBIO** que especifica el subfactor asociado a los datos biométricos. Para obtener más información, vea Comentarios y [**constantes \_ DE \_ SUBTIPO BIOMETRIC DE WINBIO**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Propósito**
</dt> <dd>

Máscara **WINBIO \_ BIR \_ PURPOSE** que especifica el uso previsto de los datos. Puede ser un OR bit a bit **de** los valores siguientes. Para obtener más información, [**vea WinBIO \_ BIR PURPOSE \_ Constants**](winbio-bir-purpose-constants.md).

-   COMPROBACIÓN DE \_ PROPÓSITO DE \_ WINBIO
-   IDENTIFICACIÓN DE \_ PROPÓSITO DE \_ WINBIO
-   INSCRIPCIÓN DE PROPÓSITO DE WINBIO \_ \_
-   INSCRIPCIÓN DE PROPÓSITO DE WINBIO \_ \_ PARA LA \_ \_ COMPROBACIÓN
-   INSCRIPCIÓN DE PROPÓSITO DE WINBIO \_ \_ PARA \_ \_ IDENTIFICACIÓN
-   AUDITORÍA DE \_ PROPÓSITO DE \_ WINBIO

</dd> <dt>

**DataQuality**
</dt> <dd>

Valor que especifica la calidad relativa de los datos biométricos en el registro de información biométrica (BIR). Puede ser un entero de 0 a 100 o uno de los valores siguientes. Para obtener más información, [**vea CONSTANTES DE CALIDAD \_ \_ DE WINBIO BIR**](winbio-bir-quality-constants.md).



| Value                                                                                                                                                                                                                                                                                                        | Significado                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ CALIDAD \_ DE DATOS NO \_ \_ ESTABLECIDA**</dt> <dt>((WINBIO \_ BIR \_ QUALITY)-1)</dt> </dl>                   | El creador de BIR admite las medidas de calidad, pero no se establece ningún valor en la BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ CALIDAD \_ DE DATOS NO \_ \_ ADMITIDA**</dt> <dt>((WINBIO \_ BIR \_ QUALITY)-2)</dt> </dl> | Las medidas de calidad no son compatibles con el creador de BIR.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

Fecha y hora, en hora universal coordinada (hora media de Greenwich), que se creó la BIR.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Período para el que la BIR es válida.

<dl> <dt>

**BeginDate**
</dt> <dd>

Fecha y hora, en hora universal coordinada, que inicia el período de validez.

</dd> <dt>

**EndDate**
</dt> <dd>

Fecha y hora, en hora universal coordinada, en la que la BIR deja de ser válida.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Estructura [**DE FORMATO REGISTRADO \_ \_ DE WINBIO**](winbio-registered-format.md) que especifica el formato de datos del bloque de datos estándar en la [**estructura BIR \_ de WINBIO.**](winbio-bir.md) Los **miembros \_ DE WINBIO REGISTERED \_ FORMAT** no pueden ser cero. Puede usar las constantes siguientes para simplificar la comprobación de errores.



| Value                                                                                                                                                                                                                                                                                      | Significado                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ NO \_ HAY PROPIETARIO DE \_ \_ FORMATO**</dt> <dt>DISPONIBLE ((USHORT)0)</dt> </dl> | No se ha especificado ningún valor de propietario asignado de IBIA (Asociación internacional del sector biométrico).<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ NO \_ HAY NINGÚN TIPO DE \_ \_ FORMATO**</dt> <dt>DISPONIBLE ((USHORT)0)</dt> </dl>    | No se ha especificado ningún tipo de formato.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Estructura [**DE FORMATO REGISTRADO \_ \_ DE WINBIO**](winbio-registered-format.md) que especifica el identificador de producto del componente que generó el bloque de datos estándar en bir. Los **miembros \_ DE WINBIO REGISTERED \_ FORMAT** pueden ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El *parámetro Subtype* especifica el subfactor asociado a los datos biométricos. Actualmente, Windows Biometric Framework (WBF) solo admite la captura de huellas digitales y usa las siguientes constantes para representar información de subtipo:

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   DEDO ÍNDICE RH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   DEDO MEDIO DE WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_
-   DEDO ANILLO DE WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   DEDO ÍNDICE DE LH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   DEDO MEDIO DE LH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   DEDO ANILLO DE LH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> No intente validar el valor proporcionado para el *valor del parámetro Subtype.* El Windows Biometrics Service validará el valor proporcionado antes de pasarlo a la implementación. Si el valor es **WINBIO \_ SUBTYPE \_ NO INFORMATION \_ o** **WINBIO \_ SUBTYPE \_ ANY**, valide cuando corresponda.

 

Si se declara cualquiera de los bits siguientes, la **estructura WINBIO \_ BIR \_ HEADER** no tiene el formato correcto.


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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**Constantes \_ DE \_ SUBTIPO BIOMÉTRICO DE WINBIO**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**Constantes DE \_ MARCAS DE DATOS DE WINBIO BIR \_ \_**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**Constantes DE \_ CAMPO BIR DE WINBIO \_**](winbio-bir-field-constants.md)
</dt> <dt>

[**Constantes WINBIO \_ BIR \_ PURPOSE**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**Constantes DE \_ CALIDAD DE WINBIO BIR \_**](winbio-bir-quality-constants.md)
</dt> <dt>

[**Constantes WINBIO \_ BIR \_ VERSION**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





