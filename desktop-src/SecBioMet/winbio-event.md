---
title: Estructura de WINBIO_EVENT (Winbio \_ Types. h)
description: Contiene la información de estado que se envía a la rutina de devolución de llamada cuando se produce un aviso de evento.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- Plataforma de biometría de Windows API de WINBIO_EVENT Structure
- PWINBIO_EVENT de puntero de estructura Plataforma de biometría de Windows API
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666059"
---
# <a name="winbio_event-structure"></a>WINBIO ( \_ estructura de eventos)

La estructura de **\_ eventos WINBIO** contiene la información de estado que se envía a la rutina de devolución de llamada cuando se genera un aviso de eventos.

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



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Valor que especifica el tipo de aviso de eventos del proveedor de servicios generado. El único proveedor admitido actualmente es el sensor de huellas digitales. Este sensor admite las marcas siguientes.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP no \_ reclamado** (el sensor ha detectado un dedo deslizante que no fue solicitado por la aplicación o por la ventana que actualmente tiene el foco. El Plataforma de biometría de Windows llama a la función de devolución de llamada para indicar que se ha producido un deslizamiento de dedo pero no intenta identificar la huella digital).
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ El evento \_ FP no \_ reclamado \_ identifica** (el sensor ha detectado un dedo deslizante que no fue solicitado por la aplicación o por la ventana que actualmente tiene el foco. El Plataforma de biometría de Windows intenta identificar la huella digital y pasa el resultado de ese proceso a la función de devolución de llamada).
</dt> </dl> </dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

**Reclamación**
</dt> <dd>

Estructura devuelta para la captura de ejemplo biométrico.

<dl> <dt>

**UnitId**
</dt> <dd>

Unidad biométrica que generó el ejemplo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valor **ULong** que contiene información adicional relacionada con errores para capturar un ejemplo biométrico. Si una captura se realiza correctamente, este parámetro se establece en cero. Los siguientes valores se definen para la captura de huellas digitales:

-   WINBIO \_ FP \_ demasiado \_ alto
-   WINBIO \_ FP \_ demasiado \_ bajo
-   WINBIO \_ FP \_ demasiado a la \_ izquierda
-   WINBIO \_ FP \_ demasiado a la \_ derecha
-   WINBIO \_ FP \_ demasiado \_ rápido
-   WINBIO \_ FP \_ demasiado \_ lento
-   WINBIO \_ FP \_ de \_ calidad deficiente
-   WINBIO \_ FP \_ demasiado \_ sesgado
-   WINBIO \_ FP \_ demasiado \_ corto
-   \_error de \_ combinación de FP de WINBIO \_

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Estructura devuelta para la captura e identificación biométricas. La identificación determina si un ejemplo puede asociarse a una plantilla biométrica existente.

<dl> <dt>

**UnitId**
</dt> <dd>

Unidad biométrica que generó el ejemplo.

</dd> <dt>

**Identidad**
</dt> <dd>

Una estructura de [**\_ identidad WINBIO**](winbio-identity.md) que contiene el GUID o SID del usuario que proporciona el ejemplo biométrico.

</dd> <dt>

**Subfactor**
</dt> <dd>

Valor [**de \_ \_ subtipo biométrico WINBIO**](winbio-biometric-subtype-constants.md) que especifica el subfactor asociado a un ejemplo biométrico. Actualmente, Plataforma de biometría de Windows (WBF) solo admite la captura de huellas digitales y usa las siguientes constantes para representar la información de subtipo.

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
> No intente validar el valor proporcionado para el valor del *subfactor* . El servicio biométrico de Windows validará el valor proporcionado antes de pasarlo a su implementación. Si el valor es **WINBIO \_ SubType \_ no \_ Information** o **WINBIO \_ SubType \_ any**, valide cuando sea necesario.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valor **ULong** que contiene información adicional sobre el error para capturar un ejemplo biométrico. Si la captura se realiza correctamente, este parámetro se establece en cero. Los siguientes valores se definen para la captura de huellas digitales:

-   WINBIO \_ FP \_ demasiado \_ alto
-   WINBIO \_ FP \_ demasiado \_ bajo
-   WINBIO \_ FP \_ demasiado a la \_ izquierda
-   WINBIO \_ FP \_ demasiado a la \_ derecha
-   WINBIO \_ FP \_ demasiado \_ rápido
-   WINBIO \_ FP \_ demasiado \_ lento
-   WINBIO \_ FP \_ de \_ calidad deficiente
-   WINBIO \_ FP \_ demasiado \_ sesgado
-   WINBIO \_ FP \_ demasiado \_ corto
-   \_error de \_ combinación de FP de WINBIO \_

</dd> </dl> </dd> <dt>

**Error**
</dt> <dd>

Estructura que identifica el éxito o el error de la operación que se está supervisando.

<dl> <dt>

**ErrorCode**
</dt> <dd>

Valor **HRESULT** que contiene \_ un código de error o que es correcto debido a los cálculos realizados por el plataforma de biometría de Windows.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Llame a la función [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para registrar una rutina de devolución de llamada con el fin de recibir notificaciones de eventos del plataforma de biometría de Windows. La devolución de llamada es una función personalizada que debe definir para la aplicación.

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

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





