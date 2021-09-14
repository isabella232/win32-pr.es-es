---
title: WINBIO_EVENT estructura (Tipos de \_ Winbio.h)
description: Contiene información de estado enviada a la rutina de devolución de llamada cuando se genera un aviso de evento.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT estructura Windows API de marco biométrico
- PWINBIO_EVENT puntero de estructura Windows API de marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160766"
---
# <a name="winbio_event-structure"></a>Estructura DE \_ EVENTOS WINBIO

La **estructura EVENT \_ de WINBIO** contiene información de estado enviada a la rutina de devolución de llamada cuando se genera un aviso de evento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Valor que especifica el tipo de aviso de evento del proveedor de servicios que se ha producido. El único proveedor admitido actualmente es el sensor de huella digital. Este sensor admite las marcas siguientes.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED** (El sensor detectó un deslizamiento de dedo no solicitado por la aplicación o por la ventana que actualmente tiene el foco). El Windows Biometric Framework llama a la función de devolución de llamada para indicar que se ha producido un deslizamiento de dedo, pero no intenta identificar la huella digital).
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED \_ IDENTIFY** (El sensor detectó un deslizamiento de dedo no solicitado por la aplicación o por la ventana que actualmente tiene el foco). El Windows Biometric Framework intenta identificar la huella digital y pasa el resultado de ese proceso a la función de devolución de llamada).
</dt> </dl> </dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

**Sin reclamación**
</dt> <dd>

Estructura devuelta para la captura de muestras biométricas.

<dl> <dt>

**UnitId**
</dt> <dd>

Unidad biométrica que generó el ejemplo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valor **ULONG que** contiene información adicional sobre el error al capturar una muestra biométrica. Si una captura se realiza correctamente, este parámetro se establece en cero. Se definen los siguientes valores para la captura de huellas digitales:

-   WINBIO \_ FP \_ TOO \_ HIGH
-   WINBIO \_ FP \_ TOO \_ LOW
-   WINBIO \_ FP \_ TOO \_ LEFT
-   WINBIO \_ FP \_ TOO \_ RIGHT
-   WINBIO \_ FP \_ TOO \_ FAST
-   WINBIO \_ FP \_ DEMASIADO \_ LENTO
-   WINBIO \_ FP DE BAJA \_ \_ CALIDAD
-   WINBIO \_ FP \_ DEMASIADO \_ SESGADO
-   WINBIO \_ FP \_ TOO \_ SHORT
-   ERROR DE COMBINACIÓN \_ DE FP \_ DE \_ WINBIO

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Estructura devuelta para la captura e identificación biométricas. La identificación determina si una muestra se puede asociar a una plantilla biométrica existente.

<dl> <dt>

**UnitId**
</dt> <dd>

Unidad biométrica que generó el ejemplo.

</dd> <dt>

**Identidad**
</dt> <dd>

Estructura [**DE \_ WINBIO IDENTITY**](winbio-identity.md) que contiene el GUID o SID del usuario que proporciona la muestra biométrica.

</dd> <dt>

**SubFactor**
</dt> <dd>

Valor [**DE \_ \_ SUBTIPO BIOMÉTRICO DE WINBIO**](winbio-biometric-subtype-constants.md) que especifica el subfactor asociado a una muestra biométrica. El Windows Biometric Framework (WBF) actualmente solo admite la captura de huellas digitales y usa las siguientes constantes para representar información de subtipo.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   DEDO ÍNDICE RH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   DEDO ANILLO DE WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ MIDDLE \_ FINGER
-   DEDO ANILLO DE LH DE WINBIO \_ ANSI \_ 381 \_ POS \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> No intente validar el valor proporcionado para el *valor subfactor.* El Windows Biometrics Service validará el valor proporcionado antes de pasarlo a la implementación. Si el valor es **WINBIO \_ SUBTYPE \_ NO INFORMATION \_ o** **WINBIO \_ SUBTYPE \_ ANY**, valide cuando corresponda.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valor **ULONG** que contiene información adicional sobre el error al capturar una muestra biométrica. Si la captura se realiza correctamente, este parámetro se establece en cero. Se definen los siguientes valores para la captura de huellas digitales:

-   WINBIO \_ FP \_ TOO \_ HIGH
-   WINBIO \_ FP \_ TOO \_ LOW
-   WINBIO \_ FP \_ TOO \_ LEFT
-   WINBIO \_ FP \_ TOO \_ RIGHT
-   WINBIO \_ FP \_ TOO \_ FAST
-   WINBIO \_ FP \_ DEMASIADO \_ LENTO
-   WINBIO \_ FP DE BAJA \_ \_ CALIDAD
-   WINBIO \_ FP \_ DEMASIADO \_ SESGADO
-   WINBIO \_ FP \_ TOO \_ SHORT
-   ERROR DE COMBINACIÓN \_ DE FP \_ DE \_ WINBIO

</dd> </dl> </dd> <dt>

**Error**
</dt> <dd>

Estructura que identifica el éxito o el error de la operación que se está supervisando.

<dl> <dt>

**ErrorCode**
</dt> <dd>

**Valor HRESULT** que contiene S OK o un código de error resultante de los cálculos realizados por el \_ Windows Biometric Framework.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Llame a [**la función WinBioRegisterEventMonitor para**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) registrar una rutina de devolución de llamada para recibir notificaciones de eventos de Windows Biometric Framework. La devolución de llamada es una función personalizada que debe definir para la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





