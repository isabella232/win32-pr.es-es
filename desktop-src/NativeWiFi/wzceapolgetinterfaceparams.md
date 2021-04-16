---
description: Obtiene los parámetros de configuración de EAPOL para la interfaz LAN inalámbrica especificada.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Función WZCEapolGetInterfaceParams (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678302"
---
# <a name="wzceapolgetinterfaceparams-function"></a>WZCEapolGetInterfaceParams función)

\[**WZCEapolGetInterfaceParams** ya no es compatible con Windows Vista y windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

La función **WZCEapolGetInterfaceParams** obtiene los parámetros de configuración de EAPOL para la interfaz LAN inalámbrica especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrvAddr* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **null**, se llama al servicio de configuración inalámbrica cero en el equipo local.

Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*pwszGuid* \[ de\]
</dt> <dd>

GUID de la interfaz para la que se van a recuperar los datos.

</dd> <dt>

*dwSizeOfSSID* \[ de\]
</dt> <dd>

Tamaño del identificador de red para el que se van a recuperar los datos.

</dd> <dt>

*pbSSID* \[ de\]
</dt> <dd>

Puntero al identificador de red para el que se van a recuperar los datos.

</dd> <dt>

*pIntfParams* \[ in, out\]
</dt> <dd>

Un puntero a una estructura de parámetros [**\_ \_ Intf de EAPOL**](eapol-intf-params.md) que contiene parámetros de interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ un error si la operación se completa correctamente; de lo contrario, devuelve uno de los códigos de error del sistema de Windows.

## <a name="remarks"></a>Observaciones

Si **WZCEapolGetInterfaceParams** devuelve un error \_ , el llamador debe llamar a [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar los búferes internos asignados para los datos devueltos cuando ya no se necesite esta información.

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

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
