---
description: Actualiza la información de la interfaz para una interfaz LAN inalámbrica específica.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Función WZCRefreshInterface (Wzcsapi.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169382"
---
# <a name="wzcrefreshinterface-function"></a>Función WZCRefreshInterface

\[**WZCRefreshInterface** no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [la API Wi-Fi nativa,](native-wifi-reference.md)que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **función WZCRefreshInterface** actualiza la información de interfaz para una interfaz LAN inalámbrica específica.

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

*pSrvAddr* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **NULL,** se llama al servicio configuración inalámbrica cero en el equipo local.

Si el *parámetro pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*dwInFlags* \[ En\]
</dt> <dd>

Conjunto de campos que se actualizarán junto con acciones de actualización específicas que se deben realizar. Se trata de una máscara de bits que puede contener cualquier combinación de las marcas siguientes.



| Value                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ Descr**</dt> <dt>0x00010000</dt> </dl>             | Actualice la descripción de la interfaz para una interfaz LAN inalámbrica.<br/> La descripción de la interfaz actualizada se puede recuperar llamando a la función [**WZCQueryInterface**](wzcqueryinterface.md) con el bit **\_ INTF DESCR** establecido en el *parámetro dwInFlags.* La descripción de la interfaz se devuelve en el miembro **wszDescr** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf* devuelto por la función **WZCQueryInterface.**<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | Actualice la información multimedia de NDIS para una interfaz LAN inalámbrica.<br/> La información de medios de NDIS actualizada se puede recuperar llamando a la función [**WZCQueryInterface**](wzcqueryinterface.md) con el bit **\_ INTF NDISMEDIA** establecido en el *parámetro dwInFlags.* La información multimedia de NDIS se devuelve en los miembros **ulMediaState**, **ulMediaType** y **ulPhysicalMediaType** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf* devuelto por la función **WZCQueryInterface.**<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ TODOS \_ los OIDS**</dt> <dt>0xFFF00000</dt> </dl>   | Actualice todos los NDIS para una interfaz LAN inalámbrica. Esta opción actualiza la mayoría de los datos de una interfaz LAN inalámbrica.<br/> La información actualizada se puede recuperar llamando a la [**función WZCQueryInterface.**](wzcqueryinterface.md)<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ En\]
</dt> <dd>

Puntero a una [**estructura INTF \_ ENTRY**](intf-entry.md) que contiene la clave de la interfaz que se va a actualizar.

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Conjunto de campos que se actualizaron correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ DE ERROR DE LA \_ PAPELERA**</dt> </dl>     | Los bloques de control de almacenamiento se destruyeron. Este error se devuelve si el servicio configuración inalámbrica cero no ha inicializado objetos internos.<br/>                                                                                                                      |
| <dl> <dt>**ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO**</dt> </dl>   | El sistema no encuentra el archivo especificado. Este error se devuelve si el GUID del miembro **wszGuid** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el parámetro *pIntf* no coincide con ninguna de las interfaces laN inalámbricas del equipo local. <br/> |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl> | Un parámetro es incorrecto. Este error se devuelve si el *parámetro pIntf* es **NULL.** Este error se devuelve si el **miembro wszGuid** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el *parámetro pIntf* es **NULL.** <br/>                            |
| <dl> <dt>**ESTADO \_ DE RPC**</dt> </dl>               | Varios códigos de error.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El **miembro wszGuid** de la estructura [**INTF \_ ENTRY**](intf-entry.md) a la que apunta el parámetro *pIntf* debe contener un GUID de interfaz para una interfaz LAN inalámbrica. Se puede recuperar una lista de interfaces LAN inalámbricas mediante una llamada a la [**función WZCEnumInterfaces.**](wzcenuminterfaces.md)

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

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**ENTRADA \_ INTF**](intf-entry.md)
</dt> </dl>

 

 




