---
description: Proporciona información detallada para una interfaz de LAN inalámbrica administrada por el servicio de configuración inalámbrica rápida.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Función WZCQueryInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912521"
---
# <a name="wzcqueryinterface-function"></a>WZCQueryInterface función)

\[**WZCQueryInterface** ya no es compatible con Windows Vista y windows Server 2008. En su lugar, use la función [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) . Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md). \]

La función **WZCQueryInterface** proporciona información detallada para una interfaz de LAN inalámbrica administrada por el servicio de configuración inalámbrica rápida.

Proporciona información detallada para una interfaz determinada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrvAddr* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **null**, el servicio de configuración inalámbrica cero se consulta en el equipo local.

Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ de\]
</dt> <dd>

Los campos que se van a consultar. Se trata de una máscara de máscara que puede contener cualquier combinación de las marcas siguientes.



| Value                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**Intf \_ DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | Devuelve el valor del miembro **dwDynFlags** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**Intf \_ DESCr**</dt> <dt>0x00010000</dt> </dl>                      | Devuelve el valor del miembro **wszDescr** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**Intf \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | Devuelva los valores de los miembros **ulMediaState**, **ulMediaType** y **ulPhysicalMediaType** en la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**Intf \_ PREFLIST**</dt> <dt>0x00040000</dt> </dl>             | Devuelve la lista de redes preferida en el miembro **rdStSSIDList** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**Intf \_ CAPACIDADES**</dt> <dt>0x00080000</dt> </dl> | Devuelva los valores de los miembros **dwCapabilities** y **rdNicCapabilities** en la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**Intf \_ INFRAMODE**</dt> <dt>0x00200000</dt> </dl>          | Devuelve el valor del miembro **nInfraMode** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/> El miembro **nInfraMode** solo es válido en algunos Estados de contexto de interfaz.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**Intf \_ AUTHMODE**</dt> <dt>0x00400000</dt> </dl>             | Devuelve el valor del miembro **nAuthMode** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* . <br/> El miembro **nAuthMode** solo es válido en algunos Estados de contexto de interfaz.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**Intf \_ WEPSTATUS**</dt> <dt>0x00800000</dt> </dl>          | Devuelve el valor del miembro **nWepStatus** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* . <br/> El miembro **nWepStatus** solo es válido en algunos Estados de contexto de interfaz.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**Intf \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Devuelve el valor del miembro **rdSSID** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/> El miembro **rdSSID** solo es válido en algunos Estados de contexto de interfaz.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**Intf \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Devuelve el valor del miembro **rdBSSID** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/> El miembro **rdBSSID** solo es válido en algunos Estados de contexto de interfaz.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**Intf \_ BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | Devuelve la lista visible de redes en el miembro **rdBSSIDList** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .<br/> El miembro **rdBSSIDList** solo es válido en algunos Estados de contexto de interfaz.<br/> |



 

</dd> <dt>

*pIntf* \[ in, out\]
</dt> <dd>

En la entrada, puntero a la clave de la interfaz que se va a consultar. En la salida, puntero a los datos de la interfaz solicitada. Este parámetro es un puntero a una estructura de [**\_ entrada Intf**](intf-entry.md) .

</dd> <dt>

*pdwOutFlags* \[ enuncia\]
</dt> <dd>

Un conjunto de campos recuperados correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                               | Descripción                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR de la \_ arena \_**</dt> </dl>      | Los bloques de control de almacenamiento se han destruido. Se devuelve este error si el servicio de configuración inalámbrica cero no ha inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**\_ \_ no \_ se encontró el archivo de error**</dt> </dl>    | El sistema no encuentra el archivo especificado. Se devuelve este error si el GUID del miembro **wszGuid** de la estructura [**de \_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* no coincidía con ninguna de las interfaces LAN inalámbricas del equipo local. <br/> |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>  | Un parámetro no es correcto. Se devuelve este error si el parámetro *pIntf* es **null**. Este error se devuelve si el miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* es **null**. <br/>                            |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl> | No hay suficiente memoria disponible para procesar esta solicitud y asignar memoria para los resultados de la consulta.<br/>                                                                                                                                                                       |
| <dl> <dt>**Estado de RPC \_**</dt> </dl>                | Varios códigos de error.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* debe contener un GUID de interfaz para una interfaz LAN inalámbrica. Se puede recuperar una lista de interfaces de LAN inalámbrica mediante una llamada a la función [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

Los siguientes miembros de la estructura de [**\_ entrada Intf**](intf-entry.md) a la que apunta *pIntf* deben establecerse en 0 antes de una llamada a la función **WZCQueryInterface** : **RdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** y **rdCtrlData**.

El servicio de configuración inalámbrica rápida no automotically actualizar el estado de los medios, incluso cuando se reciben eventos de medios conectados y desconectados. Una aplicación debe forzar una actualización del estado de los medios mediante una llamada a la función [**WZCRefreshInterface**](wzcrefreshinterface.md) antes de llamar a la función **WZCQueryInterface** si se va a solicitar el estado de medios NDIS (el \_ bit de Intf NDISMEDIA se establecerá en el parámetro *dwInFlags* ).

Cuando el parámetro *dwInFlags* contiene **Intf \_ BSSIDLIST**, la función **WZCQueryInterface** no establece *dwOutFlags* con **Intf \_ BSSIDLIST** si la lista de redes visible está vacía. Cuando el parámetro *dwInFlags* contiene **Intf \_ SSID**, la función **WZCQueryInterface** no establece *DWOUTFLAGS* con **Intf \_ SSID** si no hay ningún SSID disponible.

Si la función **WZCQueryInterface** devuelve el error \_ Success, el llamador debe llamar a la función [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) con el parámetro *pIntf* para liberar los búferes internos asignados a los datos devueltos cuando ya no se necesite esta información. Esto libera los búferes que usan los miembros **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** y **rdCtrlData** de la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .

> [!Note]  
> El archivo de encabezado *wzcsapi. h* y el archivo de biblioteca de importación *wzcsapi. lib* no están disponibles en el Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                         |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_entrada Intf**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
