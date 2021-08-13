---
title: WINBIO_PRESENCE estructura (Winbio \_ types.h)
description: Contiene información sobre la presencia de un individuo cuya presencia se está supervisando.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE estructura Windows API de Marco biométrico
- PWINBIO_PRESENCE puntero de estructura Windows BIOMETRIC Framework API
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
ms.openlocfilehash: 2671faaee7bc277f9389d7c993e4d511dac03db459755b40bf3f659ff5256a56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909583"
---
# <a name="winbio_presence-structure"></a>Estructura WINBIO \_ PRESENCE

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

Factor biométrico que se usa para supervisar la presencia del individuo.

</dd> <dt>

**SubFactor**
</dt> <dd>

Calificador de subfactor biométrica para el factor biométrico que se usa para supervisar la presencia del individuo.

</dd> <dt>

**Estado**
</dt> <dd>

Estado del procedimiento de identificación de la persona.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Información adicional sobre el error al reconocer a un individuo, incluidos los comentarios que explican cómo corregir el error.

</dd> <dt>

**Identidad**
</dt> <dd>

La identidad del individuo cuya presencia se está supervisando, una vez que se ha identificado esa persona.

</dd> <dt>

**TrackingId**
</dt> <dd>

Entero generado por el adaptador e identifica de forma única a la persona. Se garantiza que el identificador de seguimiento que el adaptador asigna a un individuo determinado sea constante, siempre y cuando esa persona permanezca en el marco de la cámara.

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

La [**función EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) crea una matriz de estructuras **DE WINBIO \_ PRESENCE** y envía esta matriz al servicio biométrico. El servicio biométrico usa la matriz para actualizar su modelo interno de seres humanos cerca del equipo.

En función de los resultados de esta actualización, el servicio biométrico puede generar una estructura RESULT de [**WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para la función [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) para todos los clientes con monitores de presencia activa. EL **RESULTADO \_ DE WINBIO \_ ASYNC. El** miembro de operación de la estructura contiene **WINBIO \_ OPERATION MONITOR \_ \_ PRESENCE** y el **RESULTADO de WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** proporciona información adicional sobre el estado de la persona.

Cuando un individuo que el adaptador del motor asocia a un identificador de seguimiento determinado aparece en el flujo de entrada por primera vez, el servicio biométrico genera una estructura DE RESULTADOS [**DE WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) del lado cliente donde el resultado **de WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ ARRIVAL**. Esta estructura se envía a la función de devolución de llamada de la aplicación o a la cola de mensajes de la aplicación antes que cualquier otra estructura RESULT de **WINBIO \_ ASYNC \_** donde el **RESULTADO de WINBIO \_ \_ ASYNC. Parameters.MonitorPresence.PresenceArray incluye** una **estructura PRESENCE \_ de WINBIO** con el mismo valor para **WINBIO \_ PRESENCE. TrackingId**.

Las siguientes combinaciones de valores en la matriz **de estructuras DE \_ WINBIO PRESENCE** que el RESULTADO de **\_ WINBIO \_ ASYNC. El miembro Parameters.MonitorPresence.PresenceArray** indica tipos específicos de cambios en el estado de una persona.

-   Cuando un individuo está visible en el marco de la cámara, pero el motor sigue intentando identificar al individuo, los miembros de la estructura PRESENCE de **WINBIO \_** tienen los valores de la tabla siguiente.

    

    | Miembro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Entero que identifica al individuo en el motor. |
    | **Estado**        | **S \_ OK**                                                |
    | **Identity.Type** | **TIPO DE IDENTIFICADOR DE WINBIO \_ \_ \_ NULL**                               |

    

     

    En este caso, el servicio biométrico amplía el tiempo de expiración del individuo y no genera una estructura DE RESULTADOS [**de WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) del lado cliente para el identificador de seguimiento donde se encuentra el RESULTADO **de \_ WINBIO \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**.

    La primera vez que una estructura RESULT de [**WINBIO \_ \_ ASYNC**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) incluye la estructura PRESENCE de **WINBIO, \_** donde el miembro **Status** es **S \_ OK** y el miembro **Identity.Type** es **WINBIO ID TYPE \_ \_ \_ NULL** después de que una o varias estructuras DE RESULTADOS de **WINBIO \_ ASYNC \_** incluyesen una estructura PRESENCE de **WINBIO \_** con un miembro **Status** de **WINBIO E \_ BAD \_ \_ CAPTURE,** el monitor de presencia genera una única estructura RESULT de **WINBIO \_ ASYNC \_** para el identificador de seguimiento donde se encuentra el RESULTADO de **WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ TRACK**. Esta **estructura RESULT de \_ WINBIO ASYNC \_** donde se encuentra el RESULTADO DE **WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** es **WINBIO \_ CHANGE TYPE \_ \_ TRACK** informa al cliente de que se ha resuelto el problema que produjo el error **WINBIO E BAD \_ \_ \_ CAPTURE.** Para obtener más información sobre las circunstancias en las que una estructura **WINBIO \_ PRESENCE** tiene el miembro **Status** de **WINBIO \_ E BAD \_ \_ CAPTURE,** vea la descripción sobre cómo el adaptador del motor proporciona comentarios al usuario para corregir los errores de reconocimiento más adelante en estos comentarios.

-   Cuando un individuo está visible en el marco de la cámara, pero el motor sigue intentando identificar al individuo y desea proporcionar comentarios al usuario sobre cómo corregir un error de reconocimiento, los miembros de la estructura PRESENCE de **WINBIO \_** tienen los valores de la tabla siguiente.

    

    | Miembro                                                                                                      | Valor                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Entero que identifica al individuo en el motor.                      |
    | **Estado**                                                                                                  | **CAPTURA DE \_ WINBIO E \_ \_ BAD**                                                   |
    | **Identity.Type**                                                                                           | **TIPO DE IDENTIFICADOR DE WINBIO \_ \_ \_ NULL**                                                    |
    | **Properties.FacialFeatures.BoundingBox**, si el valor de **Factor** es **WINBIO \_ TYPE FACIAL \_ \_ FEATURES** | Ubicación de la cara del individuo dentro del marco de la cámara.           |
    | **Properties.Iris.BoundingBox**, si el valor de **Factor** es **WINBIO \_ TYPE \_ IRIS**                       | Ubicación del iris o iris del individuo dentro del marco de la cámara. |

    

     

    En este caso, el servicio biométrico amplía el tiempo de expiración de la persona y genera una estructura DE RESULTADOS [**de WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para el identificador de seguimiento donde se encuentra el RESULTADO **de WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ TRACK**.

-   Cuando un individuo está visible en el marco de la cámara y el adaptador del motor determina la identidad del individuo, los miembros de la estructura PRESENCE de **WINBIO \_** tienen los valores de la tabla siguiente.

    

    | Miembro                        | Valor                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Entero que identifica al individuo en el motor. |
    | **Estado**                    | **S \_ OK**                                                |
    | **Identity.Type**             | **SID DE \_ TIPO \_ DE IDENTIFICADOR \_ DE WINBIO**                                |
    | **Identity.Value.AccountSid** | Identificador de seguridad (SID) del individuo.         |

    

     

    En este caso, el servicio biométrico asocia el identificador de seguimiento con el SID de la persona y genera una estructura DE RESULTADOS [**de WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) del lado cliente para el identificador de seguimiento donde se encuentra el RESULTADO **de \_ WINBIO \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**. El servicio biométrico no genera estructuras adicionales de RESULTADO DE **WINBIO \_ ASYNC \_** del lado cliente para el identificador de seguimiento, a menos que el individuo salga del marco de la cámara.

-   Cuando un individuo está visible en el marco de la cámara, pero el adaptador del motor determina con seguridad que el individuo no está inscrito, los miembros de la estructura PRESENCE de **WINBIO \_** tienen los valores de la tabla siguiente.

    

    | Miembro            | Valor                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Entero que identifica al individuo en el motor. |
    | **Estado**        | **WINBIO \_ E \_ UNKNOWN \_ ID**                               |
    | **Identity.Type** | **TIPO DE IDENTIFICADOR DE WINBIO \_ \_ \_ NULL**                               |

    

     

    En este caso, el servicio biométrico asocia el identificador de seguimiento de la persona con una identidad de UNKNOWN y genera una estructura DE RESULTADOS [**DE WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) del lado cliente para el identificador de seguimiento donde se encuentra el resultado de **WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**. El servicio biométrico no genera estructuras adicionales de RESULTADO DE **WINBIO \_ ASYNC \_** del lado cliente para el identificador de seguimiento, a menos que el individuo salga del marco de la cámara.

Cuando un individuo que el adaptador del motor asocia a un identificador de seguimiento determinado sale del marco de la cámara y deja de aparecer en los valores devueltos por la función [**EngineAdapterIdentifyAll,**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) el identificador de seguimiento expira finalmente. Cuando el identificador de seguimiento expira, el servicio biométrico genera una estructura de resultados [**de WINBIO \_ ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) del lado cliente donde el resultado **de WINBIO \_ \_ ASYNC. El miembro Parameters.MonitorPresence.ChangeType** **es WINBIO \_ CHANGE TYPE \_ \_ DEPART**. El adaptador del motor puede impedir que el servicio biométrico genere esta estructura con el valor **\_ \_ \_ WINBIO CHANGE TYPE DEPART** mediante la inclusión de una estructura **WINBIO \_ PRESENCE** en la matriz que **devuelve EngineAdapterIdentifyAll,** donde **WINBIO \_ PRESENCE. El** miembro de estado **es S \_ OK** y **WINBIO \_ PRESENCE. El miembro Identity.Type** es **WINBIO \_ ID TYPE \_ \_ NULL** como se describió anteriormente en estos comentarios. Esta acción amplía el tiempo de expiración del identificador de seguimiento sin provocar ninguna actividad del lado cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RESULTADO \_ DE WINBIO ASYNC \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





