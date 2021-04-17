---
description: A continuación se muestra una lista de códigos de error que TAPI puede devolver al invocar operaciones en líneas, direcciones o llamadas.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Constantes de LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691050"
---
# <a name="lineerr_-constants"></a>Constantes de LINEERR \_

A continuación se muestra una lista de códigos de error que TAPI puede devolver al invocar operaciones en líneas, direcciones o llamadas. Para obtener más información sobre cómo determinar cuál de estos códigos de error puede devolver una función determinada, vea las descripciones de funciones individuales.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



La dirección especificada está bloqueada para marcarse en la llamada especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



La dirección de llamada de destino tiene habilitado el bloqueo de llamadas.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ asignado**
</dt> <dd> <dl> <dt>



No se puede abrir la línea debido a una condición persistente, como la de un puerto serie abierto exclusivamente por otro proceso.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



El identificador de dispositivo o el identificador de dispositivo de línea especificado, como en un parámetro *dwDeviceID* , no es válido o está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**
</dt> <dd> <dl> <dt>



El miembro del modo de portador de [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) no es válido, el modo de portador especificado en **LINECALLPARAMS** no está disponible o el modo de portador de llamada no se puede cambiar al modo de portador especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**
</dt> <dd> <dl> <dt>



Se rechazó el modo de facturación de la llamada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**
</dt> <dd> <dl> <dt>



Todos los aspectos de la llamada en la dirección especificada están actualmente en uso.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**
</dt> <dd> <dl> <dt>



Se ha superado el número máximo de finalizaciones de llamadas pendientes.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**
</dt> <dd> <dl> <dt>



Se ha alcanzado el número máximo de entidades de una conferencia o el número de entidades solicitado no se puede satisfacer.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**
</dt> <dd> <dl> <dt>



El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**
</dt> <dd> <dl> <dt>



El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**
</dt> <dd> <dl> <dt>



Uso del modificador de marcado (:) no se admite. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ DESconectado**
</dt> <dd> <dl> <dt>



La llamada se ha desconectado. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,2 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



La aplicación solicitó una versión de TAPI o un intervalo de versiones que es incompatible con, o no es compatible con, la implementación de la API de telefonía y el proveedor de servicios correspondiente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



La aplicación solicitó un intervalo de versiones de la extensión que no es válido o no es compatible con el proveedor de servicios correspondiente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



TAPI no puede leer ni comprender correctamente el archivo de Telephon.ini debido a incoherencias internas o problemas de formato. Por ejemplo, la \[ \] sección ubicaciones, \[ tarjetas \] o \[ países \] del archivo Telephon.ini puede estar dañada o ser incoherente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ inuse**
</dt> <dd> <dl> <dt>



El dispositivo de línea está en uso y no se puede configurar actualmente, permitir que se agregue una entidad, permitir la respuesta de una llamada, permitir que se realice una llamada o permitir la transferencia de una llamada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**
</dt> <dd> <dl> <dt>



Una dirección especificada no es válida o no está permitida. Si no es válido, la dirección contiene caracteres o dígitos no válidos, o la dirección de destino contiene caracteres de control de marcado (W, @, $ o?) que no son compatibles con el proveedor de servicios. Si no se permite, la dirección especificada no está asignada a la línea especificada o no es válida para la redirección de direcciones.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**
</dt> <dd> <dl> <dt>



El identificador de dirección especificado no es válido o está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**
</dt> <dd> <dl> <dt>



El modo de dirección especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**
</dt> <dd> <dl> <dt>



El estado de la dirección especificada contiene uno o varios bits que no son [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**
</dt> <dd> <dl> <dt>



La aplicación hizo referencia a un tipo de dirección que no es válido. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 3,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



La actividad del agente especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



La aplicación que invoca esta operación es el destino de la entrega indirecta. Es decir, TAPI ha determinado que la aplicación que realiza la llamada es también la aplicación de mayor prioridad para el tipo de medio especificado. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



La información del grupo de agentes especificado no es válida o contiene errores. No se ha realizado la acción solicitada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



La aplicación hizo referencia a un grupo de agentes que no es válido. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



El identificador de agente especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



Se usó un identificador de agente no válido. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



El estado de sesión del agente no es válido. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,2 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



El estado del agente especificado no es válido o contiene errores. No se ha realizado ningún cambio en el estado del agente de la dirección especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



La aplicación hizo referencia a un estado del agente que no es válido. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



El identificador de la aplicación (como se especifica mediante un parámetro *hLineApp* ) o el identificador de registro de la aplicación no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



El nombre de aplicación especificado no es válido. Si la aplicación especifica un nombre de aplicación, se supone que la cadena no contiene ningún carácter que no se pueda mostrar y está terminada en cero.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**
</dt> <dd> <dl> <dt>



El modo de portador especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**
</dt> <dd> <dl> <dt>



La finalización especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**
</dt> <dd> <dl> <dt>



El identificador de llamada especificado no es válido. Por ejemplo, el identificador no es **null** , pero no pertenece a la línea especificada. En algunos casos, el identificador del dispositivo de llamada especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**
</dt> <dd> <dl> <dt>



Los parámetros de llamada especificados no son válidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**
</dt> <dd> <dl> <dt>



El parámetro de privilegio de llamada especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**
</dt> <dd> <dl> <dt>



El parámetro Select especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**
</dt> <dd> <dl> <dt>



El estado actual de una llamada no tiene un estado válido para la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**
</dt> <dd> <dl> <dt>



La lista de Estados de llamada especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**
</dt> <dd> <dl> <dt>



No se encontró el identificador de tarjeta permanente especificado en *dwCard* en ninguna entrada de la \[ \] sección de tarjetas del registro.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**
</dt> <dd> <dl> <dt>



El identificador de finalización no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**
</dt> <dd> <dl> <dt>



El identificador de llamada especificado para la llamada de conferencia no es válido o no es un identificador de una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**
</dt> <dd> <dl> <dt>



El identificador de llamada de consulta especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**
</dt> <dd> <dl> <dt>



El código de país o región especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



El dispositivo de línea no tiene ningún dispositivo asociado para la clase de dispositivo especificada o la línea especificada no admite la clase de dispositivo indicada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**
</dt> <dd> <dl> <dt>



El identificador del dispositivo de línea no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**
</dt> <dd> <dl> <dt>



Los parámetros de marcado no son válidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**
</dt> <dd> <dl> <dt>



La lista de dígitos especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**
</dt> <dd> <dl> <dt>



El modo de dígito especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**
</dt> <dd> <dl> <dt>



Los dígitos de terminación especificados no son válidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



El número de versión de la extensión del proveedor de servicios no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



El parámetro *dwFeature* no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



La aplicación invocó una característica que no está disponible en esta línea.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**
</dt> <dd> <dl> <dt>



El identificador de grupo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**
</dt> <dd> <dl> <dt>



La llamada, el dispositivo, el dispositivo de línea o el identificador de línea especificados no son válidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**
</dt> <dd> <dl> <dt>



No se puede cambiar la configuración del dispositivo en el estado de línea actual. La línea puede estar en uso por otra aplicación o un parámetro *dwLineStates* contiene uno o varios bits que no son [ \_ constantes de LINEDEVSTATE](linedevstate--constants.md). El valor de **LINEERR \_ INVALLINESTATE** también puede indicar que el dispositivo está desconectado o fuera de servicio. Estos Estados se indican mediante el establecimiento de los bits correspondientes a los valores *de \_ Inservice* *LINEDEVSTATUSFLAGS \_ conectados* y LINEDEVSTATUSFLAGS en 0 en el miembro **dwDevStatusFlags** de la estructura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) devuelta por la función [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**
</dt> <dd> <dl> <dt>



No se encontró el identificador de ubicación permanente especificado en *dwLocation* en ninguna entrada de la \[ sección locations del \] registro.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**
</dt> <dd> <dl> <dt>



La lista de medios especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**
</dt> <dd> <dl> <dt>



La lista de tipos de medios (modos) que se van a supervisar contiene información no válida, el parámetro de tipo de medio especificado no es válido o el proveedor de servicios no admite el tipo de medio especificado. Los tipos de medios admitidos en la línea se enumeran en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**
</dt> <dd> <dl> <dt>



El número proporcionado en *dwMessageID* está fuera del intervalo especificado por el miembro **dwNumCompletionMessages** en la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Un parámetro o estructura a la que apunta un parámetro contiene información no válida, un código de país o región no es válido, un identificador de ventana no es válido o el parámetro de lista de reenvío especificado contiene información no válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**
</dt> <dd> <dl> <dt>



El identificador de Park no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**
</dt> <dd> <dl> <dt>



El modo de estacionamiento especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



La contraseña especificada no es correcta y la acción solicitada no se ha llevado a cabo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



La aplicación usó una contraseña no válida. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Uno o varios de los parámetros de puntero especificados (como *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* y *lpToneList*) no son válidos o un puntero necesario a un parámetro de salida es **null**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**
</dt> <dd> <dl> <dt>



Se estableció una marca no válida o una combinación de marcas para el parámetro *dwPrivileges* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**
</dt> <dd> <dl> <dt>



La tasa especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**
</dt> <dd> <dl> <dt>



El indicador [**LINEREQUESTMODE**](linerequestmode--constants.md) no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**
</dt> <dd> <dl> <dt>



El identificador de terminal especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**
</dt> <dd> <dl> <dt>



El parámetro de modos de terminal especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**
</dt> <dd> <dl> <dt>



No se admiten los tiempos de espera o un valor está fuera del intervalo válido especificado en [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**
</dt> <dd> <dl> <dt>



El tono personalizado especificado no representa un tono válido o está formado por demasiadas frecuencias o la estructura de tono especificada no describe un tono válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**
</dt> <dd> <dl> <dt>



La lista de tonos especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**
</dt> <dd> <dl> <dt>



El parámetro de modo de tono especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**
</dt> <dd> <dl> <dt>



El parámetro de modo de transferencia especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**
</dt> <dd> <dl> <dt>



LINEMAPPER era el valor pasado en el parámetro *dwDeviceID* , pero no se encontró ninguna línea que coincida con los requisitos especificados en el parámetro *lpCallParams* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOconference**
</dt> <dd> <dl> <dt>



La llamada especificada no es un identificador de llamada de conferencia ni una llamada de participante.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ Device**
</dt> <dd> <dl> <dt>



El identificador de dispositivo especificado, que era válido previamente, ya no se acepta porque el dispositivo asociado se ha quitado del sistema desde la última vez que se inicializó TAPI. Como alternativa, el dispositivo de línea no tiene ningún dispositivo asociado para la clase de dispositivo dada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOdriver**
</dt> <dd> <dl> <dt>



No se pudo encontrar Tapiaddr.dll o el proveedor de servicios de teléfono para el dispositivo especificado encontró que uno de sus componentes falta o está dañado de forma que no se detectó en el momento de la inicialización. Se recomienda que el usuario Use el panel de control de telefonía para corregir el problema.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Memoria insuficiente para realizar la operación o no se puede bloquear la memoria.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Un proveedor de servicios de telefonía que no admite varias instancias se muestra más de una vez en \[ la \] sección proveedores del registro. La aplicación debe aconsejar al usuario que use el panel de control de telefonía para quitar el controlador duplicado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



No se permiten varias instancias de este proveedor de servicios.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOsolicitud**
</dt> <dd> <dl> <dt>



Actualmente no hay ninguna solicitud pendiente del modo indicado o la aplicación ya no es la aplicación de prioridad más alta para el modo de solicitud especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOurbanar**
</dt> <dd> <dl> <dt>



La aplicación no tiene privilegios de propietario en la llamada especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ no registrado**
</dt> <dd> <dl> <dt>



La aplicación no está registrada como destinatario de la solicitud para el modo de solicitud indicado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



No se pudo realizar la operación debido a un motivo desconocido o no especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



La operación no está disponible, como para el dispositivo especificado o la línea especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**
</dt> <dd> <dl> <dt>



Actualmente, el proveedor de servicios no tiene suficiente ancho de banda disponible para la velocidad especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialización de LINEERR \_**
</dt> <dd> <dl> <dt>



Si se ha solicitado la reinicialización de TAPI, por ejemplo, como resultado de agregar o quitar un proveedor de servicios de telefonía, se rechazarán las solicitudes de [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)o [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con este error hasta que la última aplicación cierre el uso de la API (con [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), momento en el que la nueva configuración se vuelve efectiva y las aplicaciones vuelven a ser de lineInitialize. 


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialización de LINEERR \_**
</dt> <dd> <dl> <dt>



La aplicación intentó inicializar TAPI dos veces.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Hay más solicitudes pendientes de las que el dispositivo puede controlar.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



Recursos insuficientes para completar la operación. Por ejemplo, no se puede abrir una línea debido a un sobrecompromiso dinámico de los recursos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



El miembro **dwTotalSize** de una estructura no especifica suficiente memoria para contener la parte fija de la estructura especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**
</dt> <dd> <dl> <dt>



No se encontró un destino para la entrega de llamada. Esto puede ocurrir si la aplicación con nombre no abre la misma línea con el \_ bit de propietario LINECALLPRIVILEGE en el parámetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen). O bien, en el caso de la entrega en modo multimedia, ninguna aplicación ha abierto la misma línea con el \_ bit de propietario LINECALLPRIVILEGE en el parámetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) y el tipo de medio especificado en el parámetro *dwMediaMode* se ha especificado en el parámetro *dwMediaModes* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**
</dt> <dd> <dl> <dt>



La aplicación que invoca esta operación es el destino de la entrega indirecta. Es decir, TAPI ha determinado que la aplicación que realiza la llamada es también la aplicación de mayor prioridad para el tipo de medio especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR no \_ inicializado**
</dt> <dd> <dl> <dt>



La operación se invocó antes de cualquier aplicación llamada [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**
</dt> <dd> <dl> <dt>



El usuario canceló la llamada. Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,2 o posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**
</dt> <dd> <dl> <dt>



La cadena que contiene información de usuario de usuario supera el número máximo de bytes especificado en el miembro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** o **dwUUISendUserUserInfoSize** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), o bien la cadena que contiene información de usuario de usuario es demasiado larga.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de 0xC0000000 a 0xFFFFFFFF están disponibles para las extensiones específicas del dispositivo. Los valores 0x80000000 a través de 0xBFFFFFFF están reservados, mientras que 0x00000000 a 0x7FFFFFFF se usan como identificadores de solicitud.

Si una aplicación obtiene un error devuelto que no controla específicamente (como un error definido por una extensión específica del dispositivo), debe tratar el error como LINEERR \_ OPERATIONFAILED (por un motivo no especificado).

Al invocar las \_ constantes LINEERR que son nuevas con TAPI 3,0, el archivo Tapierr.MC debe actualizarse con mensajes nuevos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




