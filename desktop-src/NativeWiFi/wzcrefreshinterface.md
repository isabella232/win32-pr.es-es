---
description: Actualiza la información de interfaz para una interfaz LAN inalámbrica específica.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Función WZCRefreshInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361221"
---
# <a name="wzcrefreshinterface-function"></a>WZCRefreshInterface función)

\[**WZCRefreshInterface** no es compatible con Windows Vista y windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

La función **WZCRefreshInterface** actualiza la información de interfaz para una interfaz LAN inalámbrica específica.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrvAddr* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **null**, se llama al servicio de configuración inalámbrica cero en el equipo local.

Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ de\]
</dt> <dd>

Conjunto de campos que se van a actualizar junto con acciones de actualización específicas que se van a realizar. Se trata de una máscara de máscara que puede contener cualquier combinación de las marcas siguientes.



| Value                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**Intf \_ DESCr**</dt> <dt>0x00010000</dt> </dl>             | Actualice la descripción de la interfaz de una interfaz LAN inalámbrica.<br/> La descripción de la interfaz actualizada se puede recuperar mediante una llamada a la función [**WZCQueryInterface**](wzcqueryinterface.md) con el bit **\_ Descr de Intf** establecido en el parámetro *dwInFlags* . La descripción de la interfaz se devuelve en el miembro **wszDescr** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *PIntf* devuelto por la función **WZCQueryInterface** .<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**Intf \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | Actualice la información multimedia de NDIS para una interfaz de LAN inalámbrica.<br/> La información multimedia de NDIS actualizada se puede recuperar llamando a la función [**WZCQueryInterface**](wzcqueryinterface.md) con el conjunto de bits **Intf \_ NDISMEDIA** en el parámetro *dwInFlags* . La información multimedia de NDIS se devuelve en los miembros **ulMediaState**, **ulMediaType** y **ulPhysicalMediaType** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* devuelto por la función **WZCQueryInterface** .<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**Intf \_ Todos los \_ OID**</dt> <dt>0xFFF00000</dt> </dl>   | Actualice todos los OID de NDIS para una interfaz de LAN inalámbrica. Esta opción actualiza la mayoría de los datos de una interfaz LAN inalámbrica.<br/> La información actualizada se puede recuperar llamando a la función [**WZCQueryInterface**](wzcqueryinterface.md) .<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ entrada Intf**](intf-entry.md) que contiene la clave de la interfaz que se va a actualizar.

</dd> <dt>

*pdwOutFlags* \[ enuncia\]
</dt> <dd>

Un conjunto de campos que se actualizaron correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR de la \_ arena \_**</dt> </dl>     | Los bloques de control de almacenamiento se han destruido. Se devuelve este error si el servicio de configuración inalámbrica cero no ha inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**\_ \_ no \_ se encontró el archivo de error**</dt> </dl>   | El sistema no encuentra el archivo especificado. Se devuelve este error si el GUID del miembro **wszGuid** de la estructura [**de \_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* no coincidía con ninguna de las interfaces LAN inalámbricas del equipo local. <br/> |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl> | Un parámetro no es correcto. Se devuelve este error si el parámetro *pIntf* es **null**. Este error se devuelve si el miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* es **null**. <br/>                            |
| <dl> <dt>**Estado de RPC \_**</dt> </dl>               | Varios códigos de error.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* debe contener un GUID de interfaz para una interfaz LAN inalámbrica. Se puede recuperar una lista de interfaces de LAN inalámbrica mediante una llamada a la función [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

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

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**\_entrada Intf**](intf-entry.md)
</dt> </dl>

 

 




