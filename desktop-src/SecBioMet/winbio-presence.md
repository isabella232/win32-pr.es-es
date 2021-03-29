---
title: Estructura de WINBIO_PRESENCE (Winbio \_ Types. h)
description: Contiene información sobre la presencia de un individuo cuya presencia se está supervisando.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- Plataforma de biometría de Windows API de WINBIO_PRESENCE Structure
- PWINBIO_PRESENCE de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a917f09f419ce8dd5eb59c9c277293261bffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150341"
---
# <a name="winbio_presence-structure"></a>Estructura de presencia de WINBIO \_

Contiene información sobre la presencia de un individuo cuya presencia se está supervisando.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_PRESENCE {
  WINBIO_BIOMETRIC_TYPE      Factor;
  WINBIO_BIOMETRIC_SUBTYPE   SubFactor;
  HRESULT                    Status;
  WINBIO_REJECT_DETAIL       RejectDetail;
  WINBIO_IDENTITY            Identity;
  ULONGLONG                  TrackingId;
  WINBIO_PROTECTION_TICKET   Ticket;
  WINBIO_PRESENCE_PROPERTIES Properties;
} WINBIO_PRESENCE, *PWINBIO_PRESENCE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Factor**
</dt> <dd>

Factor biométrico que se usa para supervisar la presencia de la persona.

</dd> <dt>

**Subfactor**
</dt> <dd>

El calificador de subfactor biométrico para el factor biométrico que se usa para supervisar la presencia de la persona.

</dd> <dt>

**Estado**
</dt> <dd>

El estado del procedimiento de identificación para el individuo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Información adicional sobre el error al reconocer un individuo, incluidos los comentarios que explican cómo corregir el error.

</dd> <dt>

**Identidad**
</dt> <dd>

La identidad del individuo cuya presencia se está supervisando, una vez que se ha identificado esa persona.

</dd> <dt>

**TrackingId**
</dt> <dd>

Entero generado por el adaptador y que identifica de forma única el individuo. Se garantiza que el identificador de seguimiento que asigna el adaptador a una persona determinada es constante siempre que esa persona permanezca en el marco de la cámara.

</dd> <dt>

**Ticket**
</dt> <dd>

Reservado. El adaptador establece en 0.

</dd> <dt>

**Propiedades**
</dt> <dd>

Información específica del factor sobre la posición de un individuo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) crea una matriz de estructuras de **\_ presencia de WINBIO** y envía esta matriz al servicio biométrico. El servicio biométrico usa la matriz para actualizar su modelo interno de seres humanos cerca del equipo.

En función de los resultados de esta actualización, el servicio biométrico puede generar una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para la función [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) para cualquier cliente con monitores de presencia activos. **Resultado de WINBIO \_ Async \_ .** El miembro Operation de la estructura contiene la **\_ presencia del \_ monitor \_ de operación WINBIO** y el **\_ resultado WINBIO Async \_ . El miembro Parameters. MonitorPresence. ChangeType** proporciona información adicional sobre el estado de la persona.

Cuando un individuo que el adaptador de motor asocia con un identificador de seguimiento determinado aparece en el flujo de entrada por primera vez, el servicio biométrico genera una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) de cliente donde el **\_ resultado asincrónico de WINBIO \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ cambiar \_ tipo de \_ llegada**. Esta estructura se envía a la función de devolución de llamada de la aplicación o a la cola de mensajes de aplicación antes de cualquier otra estructura de **\_ \_ resultados asincrónicos de WINBIO** donde el **resultado de WINBIO \_ asíncrono \_ . Parameters. MonitorPresence. PresenceArray** incluye una estructura de **\_ presencia WINBIO** con el mismo valor para la **\_ presencia WINBIO. TrackingId**.

Las siguientes combinaciones de valores de la matriz de estructuras de **\_ presencia de WINBIO** que el **resultado de WINBIO \_ Async \_ . El miembro Parameters. MonitorPresence. PresenceArray** indica determinados tipos de cambios en el estado de un individuo.

-   Cuando una persona es visible en el fotograma de la cámara, pero el motor sigue intentando identificar a la persona, los miembros de la estructura de **\_ presencia WINBIO** tienen los valores de la tabla siguiente.

    

    | Miembro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Entero que identifica el individuo en el motor. |
    | **Estado**        | **S \_ correcto**                                                |
    | **Identity. Type** | **WINBIO \_ ID \_ Type \_ null**                               |

    

     

    En este caso, el servicio biométrico extiende el tiempo de expiración para el individuo y no genera una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) del lado cliente para el identificador de seguimiento donde el **resultado de WINBIO \_ Async \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ Change \_ Type \_ Recognize**.

    La primera vez que una estructura de [**\_ \_ resultados Async de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) incluye una estructura de **\_ presencia de WINBIO** en la que el miembro de **Estado** es **S \_ OK** y el miembro **Identity. Type** es **WINBIO \_ ID \_ Type \_ null** después de que una o varias estructuras de **\_ \_ resultados Async WINBIO** incluyen **una estructura \_ \_ de** **\_ presencia de WINBIO** con un miembro **status** de **WINBIO \_ E \_ \_ incorrectas** **\_ \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ Change \_ Type \_ Track**. Esta estructura de **\_ \_ resultado WINBIO Async** donde el **resultado de WINBIO \_ Async \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ Change \_ Type \_ Track** informa al cliente de que se ha resuelto el problema que causó el error de **\_ \_ \_ captura incorrecta de WINBIO E** . Para obtener más información sobre las circunstancias en las que una estructura de **\_ presencia de WINBIO** tiene un miembro de **Estado** de la **\_ \_ \_ captura incorrecta de WINBIO E**, vea la descripción de cómo el adaptador de motor proporciona comentarios al usuario para corregir los errores de reconocimiento más adelante en estas notas.

-   Cuando una persona es visible en el fotograma de la cámara, pero el motor todavía intenta identificar el individuo y desea proporcionar comentarios al usuario sobre cómo corregir un error de reconocimiento, los miembros de la estructura **de \_ presencia WINBIO** tienen los valores de la tabla siguiente.

    

    | Miembro                                                                                                      | Valor                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Entero que identifica el individuo en el motor.                      |
    | **Estado**                                                                                                  | **WINBIO \_ \_ captura incorrecta \_**                                                   |
    | **Identity. Type**                                                                                           | **WINBIO \_ ID \_ Type \_ null**                                                    |
    | **Properties. FacialFeatures. BoundingBox**, si el valor de **factor** es **WINBIO \_ Type \_ facial \_ Features** | La ubicación de la superficie del individuo dentro del marco de la cámara.           |
    | **Properties. iris. BoundingBox**, si el valor de **factor** es **WINBIO \_ tipo \_ iris**                       | La ubicación del iris o iris del individuo dentro del marco de la cámara. |

    

     

    En este caso, el servicio biométrico extiende el tiempo de expiración de para el individuo y genera una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para el identificador de seguimiento donde el **resultado de WINBIO \_ Async \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ Change \_ Type \_ Track**.

-   Cuando una persona está visible en el fotograma de la cámara y el adaptador de motor determina la identidad de la persona, los miembros de la estructura de **\_ presencia WINBIO** tienen los valores de la tabla siguiente.

    

    | Miembro                        | Valor                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Entero que identifica el individuo en el motor. |
    | **Estado**                    | **S \_ correcto**                                                |
    | **Identity. Type**             | **identificador de WINBIO de \_ tipo ID. \_ \_**                                |
    | **Identity. Value. AccountSid** | El identificador de seguridad (SID) del individuo.         |

    

     

    En este caso, el servicio biométrico asocia el identificador de seguimiento con el SID del individuo y genera una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) de cliente para el identificador de seguimiento donde el **resultado de WINBIO \_ Async \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ Change \_ Type \_ Recognize**. El servicio biométrico no genera estructuras de **\_ \_ resultados asincrónicos de WINBIO** de cliente adicionales para el identificador de seguimiento, a menos que el individuo abandone el marco de la cámara.

-   Cuando una persona es visible en el fotograma de la cámara, pero el adaptador de motor determina que el usuario no está inscrito, los miembros de la estructura de **\_ presencia WINBIO** tienen los valores de la tabla siguiente.

    

    | Miembro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Entero que identifica el individuo en el motor. |
    | **Estado**        | **WINBIO \_ E \_ \_ identificador desconocido**                               |
    | **Identity. Type** | **WINBIO \_ ID \_ Type \_ null**                               |

    

     

    En este caso, el servicio biométrico asocia el identificador de seguimiento de la persona con una identidad desconocida y genera una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) de cliente para el identificador de seguimiento donde el **\_ resultado asincrónico de WINBIO \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ Change \_ Type \_ Recognize**. El servicio biométrico no genera estructuras de **\_ \_ resultados asincrónicos de WINBIO** de cliente adicionales para el identificador de seguimiento, a menos que el individuo abandone el marco de la cámara.

Cuando una persona que el adaptador de motor asocia con un identificador de seguimiento concreto deja el fotograma de la cámara y deja de aparecer en los valores que devuelve la función [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) , el identificador de seguimiento expira finalmente. Cuando el identificador de seguimiento expira, el servicio biométrico genera una estructura de [**\_ \_ resultados asincrónicos de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) de cliente en la que el **resultado de WINBIO \_ Async \_ . El miembro Parameters. MonitorPresence. ChangeType** es **WINBIO \_ cambiar \_ tipo \_ de cambio**. El adaptador de motor puede impedir que el servicio biométrico genere esta estructura con el valor de deshacer el **tipo de \_ cambio \_ \_ WINBIO** incluyendo una estructura de **\_ presencia WINBIO** en la matriz que **EngineAdapterIdentifyAll** devuelve, donde la **\_ presencia WINBIO.** El miembro de estado es **\_ Aceptar** y **la \_ presencia WINBIO. El miembro Identity. Type** es **WINBIO \_ ID \_ Type \_ null** , tal y como se describió anteriormente en estas notas. Esta acción amplía la hora de expiración del identificador de seguimiento sin producir ninguna actividad del lado cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_resultado asincrónico de WINBIO \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





