---
description: Esta es la lista de códigos de error que la implementación puede devolver al invocar operaciones en dispositivos de teléfono. Consulte las descripciones de funciones individuales para determinar cuál de estos códigos de error puede devolver cada función.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Constantes de PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681291"
---
# <a name="phoneerr_-constants"></a>Constantes de PHONEERR \_

Esta es la lista de códigos de error que la implementación puede devolver al invocar operaciones en dispositivos de teléfono. Consulte las descripciones de funciones individuales para determinar cuál de estos códigos de error puede devolver cada función.

<dl> <dt>

<span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ asignado**
</dt> <dd> <dl> <dt>



El recurso especificado ya está asignado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



El identificador de dispositivo especificado no es válido o está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ DESconectado**
</dt> <dd> <dl> <dt>



La llamada se desconectó.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



La aplicación solicitó una versión de API o un intervalo de versiones que no se admiten en la implementación de la API de telefonía o en el proveedor de servicios correspondiente.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



La aplicación solicitó una versión de extensión o un intervalo de versiones que no es compatible con el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



Debido a incoherencias internas o problemas de formato en el archivo de Telephon.ini, TAPI no se puede leer ni comprender correctamente.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ inuse**
</dt> <dd> <dl> <dt>



El dispositivo está en uso actualmente. No se puede configurar el dispositivo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



El identificador de uso especificado o el identificador de registro de la aplicación no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



El nombre de aplicación especificado no es válido. Si la aplicación especifica un nombre de aplicación, se supone que la cadena no contiene ningún carácter no visualizable y está terminada en **null**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**
</dt> <dd> <dl> <dt>



El identificador de botón o lámpara especificado está fuera del intervalo o no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**
</dt> <dd> <dl> <dt>



El parámetro de modo de botón no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**
</dt> <dd> <dl> <dt>



El parámetro de Estados del botón no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**
</dt> <dd> <dl> <dt>



El identificador de datos especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



El teléfono especificado no admite la clase de dispositivo indicada.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



El número de versión de la extensión del proveedor de servicios no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



El parámetro de dispositivo conmutador no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**
</dt> <dd> <dl> <dt>



El parámetro de modo conmutador no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**
</dt> <dd> <dl> <dt>



El parámetro de modo de lámpara especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Un parámetro, como un valor de fila o columna o un identificador de ventana, no es válido o está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**
</dt> <dd> <dl> <dt>



El identificador de dispositivo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**
</dt> <dd> <dl> <dt>



El dispositivo telefónico no tiene un estado válido para la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Uno o varios de los parámetros de puntero especificados no son válidos.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**
</dt> <dd> <dl> <dt>



El parámetro *dwPrivilege* no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**
</dt> <dd> <dl> <dt>



El parámetro de modo de anillo no es válido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ Device**
</dt> <dd> <dl> <dt>



El identificador de dispositivo especificado, que era válido anteriormente, ya no se acepta porque el dispositivo asociado se ha quitado del sistema desde que TAPI se inicializó por última vez o está dañado de forma que no se detectó en la inicialización.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOdriver**
</dt> <dd> <dl> <dt>



El proveedor de servicios de teléfono para el dispositivo especificado encontró que uno de sus componentes falta o está dañado de forma que no se detectó en el momento de la inicialización. Se recomienda que el usuario Use el panel de control de telefonía para corregir el problema.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Memoria insuficiente para completar la operación solicitada o no se puede asignar o bloquear memoria.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_ NOurbanar**
</dt> <dd> <dl> <dt>



La aplicación no tiene privilegios de propietario en el dispositivo de teléfono especificado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



No se pudo realizar la operación por un motivo no especificado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



La operación no está disponible.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**reinicialización de PHONEERR \_**
</dt> <dd> <dl> <dt>



Si se ha solicitado la reinicialización de TAPI, por ejemplo, como resultado de agregar o quitar un proveedor de servicios de telefonía, se rechazarán las solicitudes [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) o [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con este error hasta que la última aplicación cierre el uso de la API (con [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), momento en el que la nueva configuración se vuelve efectiva y las aplicaciones vuelven a permitirse a **phoneInitialize** o **phoneInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Se ha superado el número máximo de solicitudes telefónicas pendientes.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



No se puede completar la operación debido a la sobreasignación de recursos.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



La estructura de Cap de teléfono especificada es demasiado pequeña.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR no \_ inicializado**
</dt> <dd> <dl> <dt>



La operación se invocó antes de cualquier aplicación llamada [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de 0xC0000000 a 0xFFFFFFFF están disponibles para las extensiones específicas del dispositivo; los valores 0x80000000 a 0xBFFFFFFF están reservados; y 0x00000000 a 0x7FFFFFFF se usan como identificadores de solicitud.

Si una aplicación obtiene un error devuelto que no controla específicamente (como un error definido por una extensión específica del dispositivo), debe tratar el error como PHONEERR \_ OPERATIONFAILED (por un motivo no especificado).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




