---
description: Proporciona información detallada para una interfaz LAN inalámbrica administrada por el servicio Configuración inalámbrica cero.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Función WZCQueryInterface (Wzcsapi.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169386"
---
# <a name="wzcqueryinterface-function"></a>Función WZCQueryInterface

\[**WZCQueryInterface** ya no se admite a partir de Windows Vista y Windows Server 2008. Use la [**función WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) en su lugar. Para obtener más información, vea [Acerca de la API Wi-Fi nativa.](about-the-native-wifi-api.md) \]

La **función WZCQueryInterface proporciona** información detallada para una interfaz LAN inalámbrica administrada por el servicio Configuración inalámbrica cero.

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

*pSrvAddr* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **NULL,** se consulta el servicio configuración inalámbrica cero en el equipo local.

Si el *parámetro pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ En\]
</dt> <dd>

Campos que se consultarán. Se trata de una máscara de bits que puede contener cualquier combinación de las marcas siguientes.



| Value                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | Devuelve el valor del **miembro dwDynFlags** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ DESCR**</dt> <dt>0x00010000</dt> </dl>                      | Devuelve el valor del **miembro wszDescr** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | Devuelve los valores de los miembros **ulMediaState**, **ulMediaType** y **ulPhysicalMediaType** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta *el parámetro pIntf.*<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ PreFLIST**</dt> <dt>0x00040000</dt> </dl>             | Devuelve la lista preferida de redes en el **miembro rdStSSIDList** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ FUNCIONALIDADES**</dt> <dt>0x00080000</dt> </dl> | Devuelve los valores de los **miembros dwCapabilities** y **rdNicCapabilities** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_ Inframode**</dt> <dt>0x00200000</dt> </dl>          | Devuelve el valor del **miembro nInfraMode** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/> El **miembro nInfraMode** solo es válido en algunos estados de contexto de interfaz.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ AUTHMODE**</dt> <dt>0x00400000</dt> </dl>             | Devuelve el valor del **miembro nAuthMode** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.* <br/> El **miembro nAuthMode** solo es válido en algunos estados de contexto de interfaz.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ WePSTATUS**</dt> <dt>0x00800000</dt> </dl>          | Devuelve el valor del **miembro nWepStatus** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.* <br/> El **miembro nWepStatus** solo es válido en algunos estados de contexto de interfaz.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Devuelve el valor del miembro **rdSSID** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/> El **miembro rdSSID** solo es válido en algunos estados de contexto de interfaz.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Devuelve el valor del **miembro rdBSSID** en la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/> El **miembro rdBSSID** solo es válido en algunos estados de contexto de interfaz.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | Devuelve la lista visible de redes en el **miembro rdBSSIDList** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*<br/> El **miembro rdBSSIDList** solo es válido en algunos estados de contexto de interfaz.<br/> |



 

</dd> <dt>

*pIntf* \[ in, out\]
</dt> <dd>

En la entrada, puntero a la clave de la interfaz que se consulta. En la salida, puntero a los datos de interfaz solicitados. Este parámetro es un puntero a una [**estructura INTF \_ ENTRY.**](intf-entry.md)

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Conjunto de campos recuperados correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                               | Descripción                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ DE ERROR DE LA \_ PAPELERA**</dt> </dl>      | Los bloques de control de almacenamiento se destruyeron. Este error se devuelve si el servicio configuración inalámbrica cero no ha inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO**</dt> </dl>    | El sistema no encuentra el archivo especificado. Este error se devuelve si el GUID del miembro **wszGuid** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el parámetro *pIntf* no coincide con ninguna de las interfaces laN inalámbricas del equipo local. <br/> |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>  | Un parámetro es incorrecto. Este error se devuelve si el *parámetro pIntf* es **NULL.** Este error se devuelve si el **miembro wszGuid** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf* es **NULL.** <br/>                            |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl> | No hay suficiente memoria disponible para procesar esta solicitud y asignar memoria para los resultados de la consulta.<br/>                                                                                                                                                                       |
| <dl> <dt>**ESTADO \_ DE RPC**</dt> </dl>                | Varios códigos de error.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El **miembro wszGuid** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el parámetro *pIntf* debe contener un GUID de interfaz para una interfaz LAN inalámbrica. Se puede recuperar una lista de interfaces LAN inalámbricas mediante una llamada a la [**función WZCEnumInterfaces.**](wzcenuminterfaces.md)

Los siguientes miembros de la estructura [**INTF \_ ENTRY**](intf-entry.md) a los que apunta *pIntf* deben establecerse en 0 antes de llamar a la función **WZCQueryInterface:** **rdSSID,** **rdBSSID,** **rdBSSIDList,** **rdStSSIDList** y **rdCtrlData**.

El servicio configuración inalámbrica cero no actualiza automáticamente el estado de los medios, incluso cuando se reciben eventos conectados y desconectados de los medios. Una aplicación debe forzar una actualización del estado multimedia llamando a la función [**WZCRefreshInterface**](wzcrefreshinterface.md) antes de llamar a la función **WZCQueryInterface** si se va a solicitar el estado multimedia de NDIS (el bit NDISMEDIA de INTF se establecerá en el \_ parámetro *dwInFlags).*

Cuando el *parámetro dwInFlags* contiene **INTF \_ BSSIDLIST,** la función **WZCQueryInterface** no establece *dwOutFlags* con **INTF \_ BSSIDLIST** si la lista visible de redes está vacía. Cuando el *parámetro dwInFlags* contiene **INTF \_ SSID,** la función **WZCQueryInterface** no establece *dwOutFlags* con **INTF \_ SSID** si no hay ningún SSID disponible.

Si la función **WZCQueryInterface** devuelve ERROR SUCCESS, el autor de la llamada debe llamar a la función LocalFree con el parámetro \_ *pIntf* para liberar los búferes internos asignados para los datos devueltos una vez que esta información ya no sea necesaria. [](/windows/win32/api/winbase/nf-winbase-localfree) Esto libera los búferes usados por los miembros **rdSSID,** **rdBSSID,** **rdBSSIDList,** **rdStSSIDList** y **rdCtrlData** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf.*

> [!Note]  
> El *archivo de encabezado Wzcsapi.h* y el archivo de biblioteca de importación *Wzcsapi.lib* no están disponibles en Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                         |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ENTRADA \_ INTF**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
