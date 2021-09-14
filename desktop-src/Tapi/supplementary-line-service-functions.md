---
description: Las funciones de servicio de línea adicionales se enumeran por categoría en los temas siguientes.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funciones de servicio de línea complementaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253412"
---
# <a name="supplementary-line-service-functions"></a>Funciones de servicio de línea complementaria

Las funciones de servicio de línea adicionales se enumeran por categoría en los temas siguientes. Una función se identifica como [*asincrónica*](a-tapgloss.md) si indica la finalización en un mensaje REPLY a la aplicación. Si la función siempre devuelve su resultado a la aplicación inmediatamente, la función se considera [*sincrónica.*](s-tapgloss.md)

A continuación se muestra una agrupación funcional de las funciones de servicio de línea adicionales:

-   [Agentes](#agents)
-   [Prioridad de la aplicación](#application-priority)
-   [Modo de portador y velocidad](#bearer-mode-and-rate)
-   [Llamada a accept y redirect](#call-accept-and-redirect)
-   [Finalización de llamadas](#call-completion)
-   [Conferencia de llamadas](#call-conference)
-   [Reenvío de llamadas](#call-forwarding)
-   [Retención de llamadas](#call-hold)
-   [Llamada a un aparcamiento](#call-park)
-   [Recogida de llamadas](#call-pickup)
-   [Llamada a reject](#call-reject)
-   [Transferencia de llamadas](#call-transfer)
-   [Supervisión y recopilación de dígitos](#digit-monitoring-and-gathering)
-   [Generación de dígitos y tonos de la banda](#generating-inband-digits-and-tones)
-   [Realización de llamadas](basic-telephony-services-reference.md)
-   [Control multimedia](#media-control)
-   [Supervisión de medios](#media-monitoring)
-   [Proxies](#proxies)
-   [Calidad de servicio](#quality-of-service)
-   [Envío de información a una entidad remota](#sending-information-to-remote-party)
-   [Administración de proveedores de servicios](#service-provider-management)
-   [Establecimiento de un terminal para conversaciones telefónicas](#setting-a-terminal-for-phone-conversations)
-   [Supervisión del tono](#tone-monitoring)

También hay varias [funciones de](#miscellaneous) servicio de línea complementarias.

## <a name="bearer-mode-and-rate"></a>Modo de portador y velocidad



| Función                                       | Descripción                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | Solicita un cambio en los parámetros de llamada de una llamada existente. Synchronous. |



 

## <a name="media-monitoring"></a>Supervisión de medios



| Función                                     | Descripción                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | Habilita o deshabilita la notificación en modo multimedia en una llamada especificada. Synchronous. |



 

## <a name="digit-monitoring-and-gathering"></a>Recopilación y supervisión de dígitos



| Función                                       | Descripción                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | Habilita o deshabilita la notificación de detección de dígitos en una llamada especificada. Synchronous. |
| [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | Realiza la recopilación en búfer de dígitos en una llamada. Synchronous.                  |



 

## <a name="tone-monitoring"></a>Supervisión del tono



| Función                                     | Descripción                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**lineMonitorMonitorMonitor**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | Especifica los tonos que se detectarán en una llamada especificada. Synchronous. |



 

## <a name="media-control"></a>Control multimedia



| Función                                           | Descripción                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**lineSetMediaControl**](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | Configura la secuencia multimedia de una llamada para el control multimedia. Synchronous.                                                        |
| [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | Establece los modos multimedia de la llamada especificada en su [**estructura LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) Synchronous. |



 

## <a name="generating-inband-digits-and-tones"></a>Generación de dígitos y tonos de banda



| Función                                         | Descripción                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | Genera dígitos de la banda en una llamada. Synchronous.               |
| [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | Genera un conjunto determinado de tonos inband en una llamada. Synchronous. |



 

## <a name="call-accept-and-redirect"></a>Llamada a Accept and Redirect



| Función                             | Descripción                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | Acepta una llamada ofrecida y comienza a alertar tanto al llamador (anillo) como a la entidad llamada (anillo). Asincrónica |
| [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | Redirige una llamada de oferta a otra dirección. Asincrónica                                              |



 

## <a name="call-reject"></a>Llamar a Reject



| Función                     | Descripción                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) | Desconecta una llamada o abandona un intento de llamada en curso. Asincrónica |



 

## <a name="call-hold"></a>Retención de llamadas



| Función                         | Descripción                                           |
|----------------------------------|-------------------------------------------------------|
| [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)     | Coloca la llamada especificada en un estado de retención. Asincrónica |
| [**lineUnhold**](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | Recupera una llamada retenido. Asincrónica                  |



 

## <a name="securing-calls"></a>Protección de llamadas



| Función                                 | Descripción                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**lineSecureCall**](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | Protege una llamada existente de interferencias por otros eventos, como los pitidos de espera de llamadas en las conexiones de datos. Asincrónica |



 

## <a name="call-transfer"></a>Transferencia de llamadas



| Función                                             | Descripción                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | Prepara una llamada especificada para la transferencia a otra dirección. Asincrónica                                       |
| [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | Transfiere una llamada que se ha configurado para transferirla a otra llamada o entra en una conferencia triple. Asincrónica |
| [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | Transfiere una llamada a otra parte. Asincrónica                                                               |
| [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | Intercambia la llamada activa con la llamada actualmente en espera de consulta. Asincrónica                              |



 

## <a name="call-conference"></a>Conferencia de llamadas



| Función                                                         | Descripción                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | Prepara una llamada determinada para la adición de otra parte. Asincrónica                                                                                                                               |
| [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | Se prepara para agregar una entidad a una llamada de conferencia existente colocando la llamada de conferencia en un estado de espera y creando una llamada de consulta que se puede agregar más adelante a la llamada de conferencia. Asincrónica |
| [**lineAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | Agrega una llamada de consulta a una llamada de conferencia existente. Asincrónica                                                                                                                               |
| [**lineRemoveFromConference**](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | Quita una entidad de una llamada de conferencia. Asincrónica                                                                                                                                                |



 

## <a name="call-park"></a>Call Park



| Función                         | Descripción                                          |
|----------------------------------|------------------------------------------------------|
| [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)     | Asalte una llamada determinada en otra dirección. Asincrónica |
| [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | Recupera una llamada estacionada. Asincrónica               |



 

## <a name="call-forwarding"></a>Reenvío de llamadas



| Función                           | Descripción                                             |
|------------------------------------|---------------------------------------------------------|
| [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) | Establece o cancela las solicitudes de reenvío de llamadas. Asincrónica |



 

## <a name="call-pickup"></a>Recogida de llamadas



| Función                         | Descripción                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) | Recoge una llamada que alerta en una dirección de destino especificada y devuelve un identificador de llamada para la llamada recogida [**(linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) también se puede usar para la llamada en espera). Asincrónica |



 

## <a name="sending-information-to-remote-party"></a>Envío de información a una entidad remota



| Función                                                   | Descripción                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**lineReleaseUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | Libera información de usuario-usuario, lo que permite que el sistema sobrescriba este almacenamiento con información nueva. Asincrónica |
| [**lineSendUserUserInfo**](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | Envía información de usuario-usuario a la parte remota en la llamada especificada. Asincrónica                                |



 

## <a name="call-completion"></a>Finalización de llamadas



| Función                                         | Descripción                                      |
|--------------------------------------------------|--------------------------------------------------|
| [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | Realiza una solicitud de finalización de llamadas. Asincrónica  |
| [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | Cancela una solicitud de finalización de llamada. Asincrónica |



 

## <a name="setting-a-terminal-for-phone-conversations"></a>Establecimiento de un terminal para Teléfono conversaciones



| Función                                   | Descripción                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | Especifica el dispositivo terminal al que se enruta la línea, los eventos de dirección o los eventos de flujo multimedia de llamada especificados. Asincrónica |



 

## <a name="application-priority"></a>Prioridad de la aplicación



| Función                                         | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**lineGetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | Recupera la información de prioridad de entrega o telefonía asistida para una aplicación. Synchronous. |
| [**lineSetAppPriority**](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | Establece la entrega o la prioridad de telefonía asistida para una aplicación. Synchronous.              |



 

## <a name="service-provider-management"></a>Administración de proveedores de servicios



| Función                                           | Descripción                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [**lineAddProvider**](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | Instala un proveedor de servicios de telefonía. Synchronous.                   |
| [**lineConfigProvider**](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | Muestra el cuadro de diálogo de configuración de un proveedor de servicios. Synchronous. |
| [**lineRemoveProvider**](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | Quita un proveedor de servicios de telefonía existente. Synchronous.          |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | Recupera una lista de proveedores de servicios instalados. Synchronous.         |



 

## <a name="agents"></a>Agentes



| Función                                                     | Descripción                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | Permite que la aplicación acceda a funciones específicas del controlador propietario del controlador del agente asociado a la dirección. Asincrónica |
| [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | Obtiene la lista de actividades de las que una aplicación selecciona las funciones que realiza un agente. Asincrónica                    |
| [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | Obtiene las funcionalidades relacionadas con el agente admitidas en el dispositivo de línea especificado. Asincrónica                                            |
| [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | Obtiene la lista de grupos de agentes en los que un agente puede iniciar sesión en el distribuidor de llamadas automáticas. Asincrónica                      |
| [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | Obtiene el estado relacionado con el agente en la dirección especificada. Asincrónica                                                                |
| [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | Establece el código de actividad del agente asociado a una dirección determinada. Asincrónica                                                        |
| [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | Establece los grupos de agentes en los que el agente ha iniciado sesión en una dirección determinada. Asincrónica                                              |
| [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | Establece el estado del agente asociado a una dirección determinada. Asincrónica                                                                |



 

## <a name="proxies"></a>Servidores proxy



| Función                                       | Descripción                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | Usado por un controlador de solicitudes de proxy registrado para generar mensajes TAPI. Synchronous.  |
| [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | Indica la finalización de una solicitud de proxy por parte de un controlador de proxy registrado. Synchronous. |



 

## <a name="quality-of-service"></a>Calidad de servicio



| Función                                                           | Descripción                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**lineSetCallQualityOfService**](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | Solicita un cambio de la calidad de los parámetros de servicio para una llamada existente. Asincrónica |



 

## <a name="miscellaneous"></a>Varios



| Función                                             | Descripción                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**lineSetCallData**](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | Establece el **miembro CallData** de la [**estructura LINECALLINFO.**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) Asincrónica |
| [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | Establece los sonidos que el usuario escucha cuando una llamada no se ha recibido o está en espera. Asincrónica               |
| [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | Establece el estado del dispositivo de línea. Asincrónica                                                            |



 

 

 



